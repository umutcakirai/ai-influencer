# n8n ile Instagram Otomasyonu Kurulumu

## Instagram Hesabını Profesyonel Hesaba Dönüştürme

> [!IMPORTANT]
> Instagram hesabınızı profesyonel hesaba (işletme veya içerik üretici) dönüştürmek, hesabınızı herkese açık hale getirecektir.

Instagram uygulamasında, hesabınızı profesyonel hesaba dönüştürmek için şu adımları izleyin:

1. Ayarları açın ve **Hesap türü ve araçlar** seçeneğini seçin
2. **Profesyonel hesaba geç** seçeneğine tıklayın
3. **İleri** butonuna tıklayın
4. Oluşturmak istediğiniz hesap türünü seçin (İşletme veya İçerik Üretici)
5. Hesabınızı tanımlayan doğru kategoriyi seçin
6. Seçiminizi onaylayın

---

## n8n ile Kullanım İçin Kimlik Bilgileri Oluşturma

### 1. Facebook Sayfası Oluşturma

1. [https://www.facebook.com/pages/create](https://www.facebook.com/pages/create) adresine giderek yeni bir Facebook sayfası oluşturun
2. Gerekli parametreleri (isim, kategori) doldurun ve sayfayı oluşturun
3. Sayfa adına hareket ettiğinizden emin olun - herhangi bir nedenle aktif değilse, menüden seçin

### 2. Instagram Hesabını Facebook Sayfasına Bağlama

1. Sol taraftaki sayfanızın adına tıklayın
2. Menüden **Ayarlar** seçeneğini seçin
3. Aşağı kaydırarak **İzinler** bölümüne gidin ve **Bağlı hesaplar** seçeneğini seçin
4. **Instagram** seçeneğini seçin
5. **Hesap bağla** butonuna tıklayın ve Instagram hesabınızla giriş yapın
6. **Bağlan** butonuna tıklayın
7. **Onayla** butonuna tıklayın
8. **Devam Et** butonuna tıklayın
9. İşlem tamamlandı!

### 3. Facebook Uygulaması Oluşturma

1. [https://developers.facebook.com/apps](https://developers.facebook.com/apps) adresine gidin ve **Uygulama Oluştur** butonuna tıklayın
2. **Diğer** kullanım senaryosunu seçin ve **İleri** butonuna tıklayın
3. **İşletme** uygulama türünü seçin
4. İnceleyin ve **Uygulama Oluştur** butonuna tıklayın
5. Uygulamanıza **Instagram** ürününü ekleyin
6. Yapılandırmanıza gerek yok, olduğu gibi bırakın

### 4. Erişim Token'ı Oluşturma

1. Araçlar menüsünden **Graph API Explorer** seçeneğini seçin
2. Meta uygulamasının az önce oluşturduğunuz uygulama olduğundan emin olun
3. İzinler panelinde, aşağıdaki izinleri ekleyin:
   - `pages_show_list`
   - `business_management`
   - `instagram_basic`
   - `instagram_content_publish`
   - `pages_read_engagement`

4. **Erişim Token'ı Oluştur** butonuna tıklayın

5. Erişim vermek istediğiniz Facebook sayfasını, işletme hesabını ve Instagram hesabını seçmeniz istenecektir. Hepsini seçin. Bu işlem sırasında, bağladığınız **Instagram hesap kimliğini** not alın, daha sonra ihtiyacınız olacak.

6. Erişim token'ını kopyalayın ve [Facebook token hata ayıklama aracına](https://developers.facebook.com/tools/debug/accesstoken) gidin
   - Erişim token'ını yapıştırın ve **Hata Ayıkla** butonuna tıklayın
   - Sayfanın en altına kaydırın ve **Erişim Token'ını Uzat** butonuna tıklayın
   - Uzun ömürlü erişim token'ını kopyalayın

7. **Graph API Explorer**'a geri dönün ve:
   - Erişim token'ını erişim token alanına yapıştırın
   - Graph yoluna `me/accounts` ekleyin
   - **Gönder** butonuna tıklayın
   - Sonuçlarda, asla sona ermeyecek uzun ömürlü sayfa erişim token'ını içeren `access_token` alanını bulacaksınız
   - Bunu kopyalayın

8. **(İsteğe bağlı)** Token'ın süresini doğrulamak istiyorsanız, [Facebook token hata ayıklama aracına](https://developers.facebook.com/tools/debug/accesstoken) yapıştırabilirsiniz

9. **(İsteğe bağlı)** Instagram Business Hesabının kimliğini de alabilirsiniz:
   - Graph API explorer'da sayfanın kimliğine tıklayın
   - Kimlikten sonra `?fields=instagram_business_account` ekleyin
   - **Gönder** butonuna tıklayın

---

## Sonuç

**Yukarıdaki her şeyi yaptıysanız, iki şeye sahip olacaksınız:**

1. ✅ Instagram hesabınızı yönetmek için süresi dolmayacak bir **sayfa token'ı**
   - Bu token'ı n8n'de Facebook Graph node'unu kurmak için kullanacaksınız

2. ✅ **Instagram Business hesap kimliği**
   - Bu kimliği n8n workflow'undaki `Configure` node'unda ayarlayacaksınız

---

## n8n'de Kullanım

Artık n8n workflow'unuzda:
- Facebook Graph API node'unda sayfa token'ınızı kullanabilirsiniz
- Configure node'unda Instagram Business hesap kimliğinizi ayarlayabilirsiniz

**Tebrikler! Instagram otomasyonunuz artık hazır!** 🎉
