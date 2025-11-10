# AI Influencer

Bu ücretsiz n8n workflow'u ile kendi AI influencer'ınızı oluşturun. fal.ai'nin Veo 3.1 ve nanobanana modellerini kullanarak görsel ve açıklamalar üretir, ardından bunları Instagram'a otomatik olarak paylaşır.

## 📚 Toplulukta alimlar kapanacak, tek seferlik odeme ile omur boyu erisiminiz oluyor!
https://www.skool.com/umutcakirai-9288

## Ücretsiz n8n JSON Workflow'ları

- [ana workflow](ai-influencer.json)
- [gorsel uretme workflow](video-uretme.json)
- [video uretme workflow](gorsel-uretme.json)

## Kurulum Talimatları

### n8n veritabanınızda bu tabloları oluşturun

- **influencer**
  - name (string)
  - bio (string)
  - image (string)
  - instagram_business_id (string)

- **influencer_weekly_plans**
  - influencer_id (string)
  - week (string)
  - plan (string)

- **influencer_posts**
  - influencer_id (string)
  - post_summary (string)

## Ek Kaynaklar

- [Instagram Business hesabınızı n8n'e bağlama rehberi](guide-instagram.md)
- [Fal.ai API anahtarları](https://fal.ai/dashboard/keys)

## Nasıl Çalışır?

1. **Haftalık Plan Oluşturma**: Sistem her hafta influencer'ınız için içerik planı oluşturur
2. **Görsel Üretimi**: fal.ai modelleri kullanarak yüksek kaliteli görseller üretir
3. **Otomatik Paylaşım**: Üretilen içeriği otomatik olarak Instagram'da paylaşır

## Gereksinimler

- Bir n8n hesabı
- fal.ai API anahtarı
- Instagram Business hesabı
- Facebook Page (Instagram'a bağlı)

## Kurulum Adımları

1. Yukarıdaki JSON dosyalarını n8n'e import edin
2. Veritabanı tablolarını oluşturun
3. [Instagram bağlama rehberini](guide-instagram.md) takip edin
4. fal.ai API anahtarınızı ekleyin
5. Workflow'u test edin ve başlatın!

## Kurulum Videosu

Videoyu buradan izleyebilirsiniz https://youtu.be/m_aeCKQZWdY
