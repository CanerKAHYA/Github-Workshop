# 📝 Conventional Commits Cheat Sheet

<div align="center">

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-FE5196?style=for-the-badge&logo=conventionalcommits&logoColor=white)]()

*Standart commit mesajları için hızlı referans*

</div>

---

## 📋 Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Örnek

```
feat(auth): kullanıcı login sayfası eklendi

OAuth2 entegrasyonu ile Google ve GitHub ile giriş desteği sağlandı.
JWT token tabanlı oturum yönetimi implement edildi.

Closes #42
```

---

## 🏷️ Commit Tipleri

| Tip | Emoji | Açıklama | Örnek |
|:----|:-----:|:---------|:------|
| `feat` | ✨ | Yeni özellik | `feat: arama fonksiyonu eklendi` |
| `fix` | 🐛 | Hata düzeltme | `fix: login hatası düzeltildi` |
| `docs` | 📚 | Dokümantasyon | `docs: README güncellendi` |
| `style` | 💄 | Kod formatı (mantık değişmez) | `style: boşluklar düzenlendi` |
| `refactor` | ♻️ | Kod yeniden düzenleme | `refactor: db service optimize edildi` |
| `test` | 🧪 | Test | `test: login testleri eklendi` |
| `chore` | 🔧 | Bakım işleri | `chore: bağımlılıklar güncellendi` |
| `perf` | ⚡ | Performans | `perf: sorgu optimizasyonu` |
| `ci` | 🔄 | CI/CD | `ci: GitHub Actions eklendi` |
| `build` | 📦 | Build sistemi | `build: webpack güncellendi` |
| `revert` | ⏪ | Geri alma | `revert: feat: arama fonksiyonu` |

---

## 🎯 Scope (Kapsam)

Değişikliğin hangi bölümü etkilediğini belirtir:

```bash
feat(auth): login sayfası eklendi
fix(ui): buton renkleri düzeltildi
docs(api): endpoint dökümantasyonu güncellendi
refactor(database): connection pooling eklendi
test(user): kullanıcı servis testleri eklendi
```

### Yaygın Scope Örnekleri

```
auth, api, ui, db, core, config, deps, docs, test, ci, build
```

---

## ⚠️ Breaking Changes

Geriye dönük uyumluluğu bozan değişiklikler:

### Yöntem 1: Ünlem İşareti

```bash
feat!: API response formatı değiştirildi
fix!: veritabanı şeması değiştirildi
```

### Yöntem 2: Footer

```bash
feat: API response formatı değiştirildi

BREAKING CHANGE: Response artık array yerine object döndürüyor.
Mevcut istemciler güncellenmeli.
```

---

## 📌 Footer Kullanımı

```bash
git commit -m "fix: kullanıcı silinemiyor hatası düzeltildi

Veritabanı foreign key constraint hatası çözüldü.

Fixes #123
Closes #124
Related-to #125
Co-authored-by: Ali <ali@email.com>"
```

### Footer Anahtar Kelimeleri

| Anahtar | Açıklama |
|:--------|:---------|
| `Fixes #123` | Issue'yu kapatır |
| `Closes #123` | Issue'yu kapatır |
| `Resolves #123` | Issue'yu kapatır |
| `Ref #123` | Referans verir (kapatmaz) |
| `Related-to #123` | İlişkili issue |
| `Co-authored-by: Name <email>` | Ortak yazar |

---

## ✅ İyi Örnekler

```bash
# ✅ Anlaşılır ve standart
feat: kullanıcı profil sayfası eklendi
fix: şifre sıfırlama e-postası gönderilmiyor hatası düzeltildi
docs: API kullanım örnekleri eklendi
refactor: authentication servisi basitleştirildi
test: payment modülü entegrasyon testleri eklendi
chore: eslint kuralları güncellendi
```

---

## ❌ Kötü Örnekler

```bash
# ❌ Açıklayıcı değil
fix: düzeltme
update: güncelleme
asdasd
...

# ❌ Büyük harf ile başlıyor
Feat: yeni özellik

# ❌ Nokta ile bitiyor
feat: yeni özellik eklendi.

# ❌ Çok uzun başlık
feat: bu commit mesajı çok uzun olduğu için okunması zor ve standarda uygun değil çünkü 50 karakteri aşıyor
```

---

## 📏 Kurallar

### Başlık (Subject Line)

- ✅ Küçük harf ile başla
- ✅ Emir kipi kullan (ekle, düzelt, değil eklendi, düzeltildi)
- ✅ 50 karakter veya daha az
- ✅ Nokta ile bitirme
- ✅ "Bu commit..." ile başlayacak şekilde yaz

### Body

- ✅ Boş satır ile ayır
- ✅ 72 karakterde wrap
- ✅ Ne ve neden açıkla (nasıl değil)
- ✅ Birden fazla paragraf olabilir

### Footer

- ✅ Boş satır ile ayır
- ✅ Issue referansları
- ✅ Breaking change notları

---

## 🔧 Araçlar

### Commitlint

```bash
# Kurulum
npm install --save-dev @commitlint/cli @commitlint/config-conventional

# commitlint.config.js
echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js

# Husky ile kullanım
npx husky add .husky/commit-msg 'npx commitlint --edit ${1}'
```

### Commitizen

```bash
# Kurulum
npm install -g commitizen cz-conventional-changelog

# Yapılandırma (.czrc dosyası)
echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc

# Kullanım
git cz
# veya
cz
```

### Gitmoji

```bash
# Kurulum
npm install -g gitmoji-cli

# İnteraktif commit
gitmoji -c
```

---

## 📊 Neden Kullanmalı?

| Avantaj | Açıklama |
|:--------|:---------|
| 📖 **Okunabilirlik** | Commit geçmişi kolay okunur |
| 🔍 **Aranabilirlik** | Tipine göre filtreleme |
| 📝 **Changelog** | Otomatik changelog oluşturma |
| 🏷️ **Versiyonlama** | SemVer ile uyumlu |
| 🤖 **Otomasyon** | CI/CD süreçlerinde kullanım |

---

## 📚 Kaynaklar

- [Conventional Commits](https://www.conventionalcommits.org)
- [Angular Commit Guidelines](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#commit)
- [Commitlint](https://commitlint.js.org)
- [Commitizen](https://commitizen.github.io/cz-cli/)

---

<div align="center">

**[🏠 Ana Sayfa](../README.md)**

</div>
