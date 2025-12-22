# 🚀 Proje Adı

<div align="center">

[![Version](https://img.shields.io/badge/version-1.0.0-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=for-the-badge)]()

**Projenin kısa ve çekici açıklaması**

[Demo](https://demo.com) · [Dokümantasyon](https://docs.com) · [Hata Bildir](../../issues) · [Özellik Öner](../../issues)

</div>

---

## 📸 Ekran Görüntüleri

<div align="center">
<img src="screenshot.png" alt="Proje Ekran Görüntüsü" width="80%">
</div>

---

## ✨ Özellikler

- ✅ Özellik 1 - Kısa açıklama
- ✅ Özellik 2 - Kısa açıklama
- ✅ Özellik 3 - Kısa açıklama
- ✅ Özellik 4 - Kısa açıklama

---

## 🛠️ Teknolojiler

<div align="center">

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

</div>

---

## 📋 Gereksinimler

- Node.js 18+
- npm veya yarn
- MongoDB

---

## 🚀 Kurulum

### 1. Repo'yu Klonlayın

```bash
git clone https://github.com/KULLANICI/PROJE.git
cd PROJE
```

### 2. Bağımlılıkları Yükleyin

```bash
npm install
# veya
yarn install
```

### 3. Ortam Değişkenlerini Ayarlayın

```bash
cp .env.example .env
# .env dosyasını düzenleyin
```

### 4. Uygulamayı Başlatın

```bash
npm run dev
# veya
yarn dev
```

Tarayıcınızda `http://localhost:3000` adresini açın.

---

## 📖 Kullanım

### Temel Kullanım

```javascript
import { Component } from 'proje';

const result = Component.metod();
console.log(result);
```

### API Örneği

```bash
# GET isteği
curl http://localhost:3000/api/resource

# POST isteği
curl -X POST http://localhost:3000/api/resource \
  -H "Content-Type: application/json" \
  -d '{"key": "value"}'
```

---

## 📁 Proje Yapısı

```
proje/
├── src/
│   ├── components/     # React bileşenleri
│   ├── pages/          # Sayfa bileşenleri
│   ├── services/       # API servisleri
│   ├── utils/          # Yardımcı fonksiyonlar
│   └── App.js          # Ana uygulama
├── public/             # Statik dosyalar
├── tests/              # Test dosyaları
├── .env.example        # Örnek env dosyası
├── package.json
└── README.md
```

---

## ⚙️ Yapılandırma

| Değişken | Açıklama | Varsayılan |
|:---------|:---------|:-----------|
| `PORT` | Sunucu portu | `3000` |
| `DATABASE_URL` | Veritabanı bağlantısı | - |
| `API_KEY` | API anahtarı | - |
| `DEBUG` | Debug modu | `false` |

---

## 🧪 Testler

```bash
# Tüm testleri çalıştır
npm test

# Coverage ile
npm run test:coverage

# Watch modunda
npm run test:watch
```

---

## 📝 API Dokümantasyonu

### GET /api/resource

Tüm kaynakları listeler.

**Yanıt:**

```json
{
  "success": true,
  "data": [
    { "id": 1, "name": "Örnek" }
  ]
}
```

### POST /api/resource

Yeni kaynak oluşturur.

**İstek Gövdesi:**

```json
{
  "name": "Yeni Kaynak"
}
```

---

## 🗺️ Yol Haritası

- [x] Temel özellikler
- [x] Kullanıcı kimlik doğrulama
- [ ] Dashboard
- [ ] Mobil uygulama
- [ ] Çoklu dil desteği

Tam listeyi görmek için [açık issue'lara](../../issues) bakın.

---

## 🤝 Katkıda Bulunma

Katkılarınızı memnuniyetle karşılıyoruz!

1. Projeyi fork edin
2. Feature branch oluşturun (`git checkout -b feature/YeniOzellik`)
3. Değişikliklerinizi commit edin (`git commit -m 'feat: yeni özellik eklendi'`)
4. Branch'ınızı push edin (`git push origin feature/YeniOzellik`)
5. Pull Request açın

Detaylar için [CONTRIBUTING.md](CONTRIBUTING.md) dosyasına bakın.

---

## 👥 Yazarlar

- **Adınız** - *Başlangıç çalışması* - [@kullanici](https://github.com/kullanici)

Katkıda bulunanların listesi için [contributors](../../graphs/contributors) sayfasına bakın.

---

## 📄 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır - detaylar için [LICENSE](LICENSE) dosyasına bakın.

---

## 🙏 Teşekkürler

- [Kaynak 1](https://link.com) - Neden kullanıldı
- [Kaynak 2](https://link.com) - Neden kullanıldı
- Tüm katkıda bulunanlar

---

<div align="center">

**⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın!**

[![GitHub Stars](https://img.shields.io/github/stars/KULLANICI/PROJE?style=social)](../../stargazers)

</div>
