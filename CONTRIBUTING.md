# 🤝 Katkıda Bulunma Rehberi

GitHub Workshop eğitim materyallerine katkıda bulunmak istediğiniz için teşekkür ederiz! Bu rehber, katkı sürecini açıklar.

---

## 📋 İçindekiler

- [Nasıl Katkıda Bulunabilirim?](#nasıl-katkıda-bulunabilirim)
- [Geliştirme Ortamı](#geliştirme-ortamı)
- [Commit Mesajları](#commit-mesajları)
- [Pull Request Süreci](#pull-request-süreci)
- [Kod Standartları](#kod-standartları)
- [İletişim](#iletişim)

---

## 🎯 Nasıl Katkıda Bulunabilirim?

### 📝 İçerik Katkıları

| Tür | Açıklama |
|:----|:---------|
| 📚 **Yeni Konu** | Müfredata yeni konular ekleyin |
| ✏️ **Düzeltme** | Yazım hataları, yanlış bilgiler |
| 📖 **Açıklama** | Mevcut konuları genişletin |
| 🎨 **Görsel** | Diyagramlar, ekran görüntüleri |
| 💻 **Örnek Kod** | Pratik alıştırmalar, örnekler |
| 🌍 **Çeviri** | İngilizce çeviri desteği |

### 🐛 Hata Bildirimi

Bir hata bulduysanız:

1. [Issues](https://github.com/Furk4nBulut/Github-Workshop/issues) sayfasını kontrol edin
2. Benzer bir issue yoksa yeni issue açın
3. Detaylı açıklama yazın:
   - Ne bekliyordunuz?
   - Ne oldu?
   - Nasıl tekrarlanabilir?

### 💡 Özellik Önerisi

Yeni bir özellik önermek için:

1. [Discussions](https://github.com/Furk4nBulut/Github-Workshop/discussions) sayfasında tartışma başlatın
2. Önerinizi detaylı açıklayın
3. Topluluk geri bildirimi bekleyin

---

## 🛠️ Geliştirme Ortamı

### Repo'yu Klonlama

```bash
# Fork yapın (GitHub'da)

# Fork'unuzu klonlayın
git clone https://github.com/KULLANICI-ADINIZ/Github-Workshop.git
cd Github-Workshop

# Upstream ekleyin
git remote add upstream https://github.com/Furk4nBulut/Github-Workshop.git

# Branch oluşturun
git checkout -b feature/yeni-ozellik
```

### Güncel Tutma

```bash
# Upstream'den güncellemeleri çekin
git fetch upstream
git checkout main
git merge upstream/main
```

---

## 📝 Commit Mesajları

[Conventional Commits](https://www.conventionalcommits.org) standardını kullanıyoruz:

### Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Tipler

| Tip | Açıklama | Örnek |
|:----|:---------|:------|
| `feat` | Yeni özellik | `feat: modül 7 eklendi` |
| `fix` | Hata düzeltme | `fix: yazım hatası düzeltildi` |
| `docs` | Dokümantasyon | `docs: README güncellendi` |
| `style` | Format düzeltme | `style: boşluklar düzenlendi` |
| `refactor` | Kod yeniden yapılandırma | `refactor: örnekler sadeleştirildi` |
| `test` | Test ekleme | `test: lab alıştırması eklendi` |
| `chore` | Bakım işleri | `chore: bağımlılıklar güncellendi` |

### Örnekler

```bash
# İyi ✅
git commit -m "docs: Modül 2'ye Markdown örnekleri eklendi"
git commit -m "fix: Lab 3'teki yanlış komut düzeltildi"
git commit -m "feat(wiki): GitHub Actions bölümü eklendi"

# Kötü ❌
git commit -m "güncelleme"
git commit -m "düzeltmeler"
git commit -m "yeni şeyler"
```

---

## 🔀 Pull Request Süreci

### 1. Branch Oluşturma

```bash
# İsimlendirme formatı: <tip>/<kısa-açıklama>
git checkout -b docs/markdown-ornekleri
git checkout -b fix/lab3-komut-hatasi
git checkout -b feat/modul7-security
```

### 2. Değişiklik Yapma

- Küçük, odaklı değişiklikler yapın
- Her PR tek bir konu içersin
- Mevcut formatı takip edin

### 3. Commit ve Push

```bash
git add .
git commit -m "docs: Markdown bölümüne yeni örnekler eklendi"
git push origin docs/markdown-ornekleri
```

### 4. PR Açma

1. GitHub'da "Compare & pull request" tıklayın
2. PR şablonunu doldurun:
   - Açıklayıcı başlık
   - Yapılan değişiklikler
   - İlgili issue (varsa)
3. "Create pull request" tıklayın

### PR Şablonu

```markdown
## 📋 Açıklama
Bu PR ile ne yaptığınızı açıklayın.

## 🔧 Değişiklikler
- Değişiklik 1
- Değişiklik 2

## ✅ Kontrol Listesi
- [ ] Conventional Commits kullandım
- [ ] Mevcut formatı takip ettim
- [ ] Yazım kontrolü yaptım
- [ ] Linkleri test ettim

## 🔗 İlgili Issues
Closes #XX
```

### 5. Review Süreci

- Geri bildirimleri dikkate alın
- İstenen değişiklikleri yapın
- Sabırlı olun, review zaman alabilir

---

## 📏 Kod Standartları

### Markdown Formatı

```markdown
# Başlık 1 (sayfa başında tek adet)
## Başlık 2
### Başlık 3

**Kalın** metin için çift yıldız
*İtalik* metin için tek yıldız
`Kod` için backtick

- Sırasız liste
1. Sıralı liste

> Önemli notlar için alıntı bloğu

| Tablo | Başlık |
|:------|:-------|
| Veri  | Veri   |
```

### Dosya İsimlendirme

```
✅ İyi:
kebab-case-isim.md
module-01-giris.md
lab-02-branching.md

❌ Kötü:
CamelCase.md
spaces in name.md
türkçe-karakter.md
```

### Klasör Yapısı

```
docs/            → Dokümantasyon
exercises/       → Pratik alıştırmalar
templates/       → Şablonlar
cheatsheets/     → Hızlı referanslar
assets/          → Görseller ve kaynaklar
```

### Türkçe Karakter Kullanımı

- Dosya ve klasör isimlerinde Türkçe karakter kullanmayın
- İçerikte Türkçe karakter serbestçe kullanılabilir
- URL'lerde encode edilmiş karakterlere dikkat edin

---

## 🎨 Görsel Standartları

### Diyagramlar

- Tercihen ASCII art veya Mermaid
- PNG/SVG formatında görseller
- Açık ve koyu tema uyumlu

### Ekran Görüntüleri

- Güncel UI versiyonları
- Gizli bilgi içermemeli
- Açıklayıcı alt metin eklenmeli

### Badge'ler

- Shields.io kullanın
- Tutarlı stil: `flat-square` veya `for-the-badge`
- Anlamlı renk seçimi

---

## 🏷️ Issue ve PR Etiketleri

| Etiket | Açıklama |
|:-------|:---------|
| `documentation` | Dokümantasyon değişiklikleri |
| `enhancement` | Yeni özellik veya iyileştirme |
| `bug` | Hata düzeltme |
| `good first issue` | Yeni katılımcılar için uygun |
| `help wanted` | Yardım aranıyor |
| `question` | Soru veya tartışma |

---

## 📞 İletişim

- **Sorular:** [GitHub Discussions](https://github.com/Furk4nBulut/Github-Workshop/discussions)
- **Hatalar:** [GitHub Issues](https://github.com/Furk4nBulut/Github-Workshop/issues)
- **Genel:** [Furkan Bulut](https://github.com/Furk4nBulut)

---

## 🙏 Teşekkürler

Katkıda bulunan herkes [Contributors](https://github.com/Furk4nBulut/Github-Workshop/graphs/contributors) sayfasında listelenir.

---

<div align="center">

**Her katkı, ne kadar küçük olursa olsun, değerlidir!** 🌟

</div>
