# 🧪 Lab 3: Fork ve Açık Kaynak Katkısı

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-Orta-yellow?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-30_dk-blue?style=for-the-badge)]()

*Fork yaparak açık kaynak projelere katkıda bulunmayı öğrenin*

</div>

---

## 🎯 Öğrenme Hedefleri

Bu lab'ı tamamladığınızda:

- [x] Fork ve Clone arasındaki farkı anlayacaksınız
- [x] Bir repository'yi fork edebileceksiniz
- [x] Upstream ile sync yapabileceksiniz
- [x] Pull Request açabileceksiniz

---

## 📝 Adımlar

### Adım 1: Bu Repository'yi Fork Edin

1. GitHub'da [Github-Workshop](https://github.com/Furk4nBulut/Github-Workshop) repository'sine gidin
2. Sağ üstteki **Fork** butonuna tıklayın
3. Fork'un kendi hesabınıza oluşturulmasını bekleyin

### Adım 2: Fork'unuzu Clone Edin

```bash
# Fork'unuzu klonlayın (USER yerine kendi kullanıcı adınızı yazın)
git clone https://github.com/USER/Github-Workshop.git
cd Github-Workshop
```

### Adım 3: Upstream Ekleyin

```bash
# Orijinal repo'yu upstream olarak ekleyin
git remote add upstream https://github.com/Furk4nBulut/Github-Workshop.git

# Remote'ları kontrol edin
git remote -v

# Çıktı:
# origin    https://github.com/USER/Github-Workshop.git (fetch)
# origin    https://github.com/USER/Github-Workshop.git (push)
# upstream  https://github.com/Furk4nBulut/Github-Workshop.git (fetch)
# upstream  https://github.com/Furk4nBulut/Github-Workshop.git (push)
```

### Adım 4: Feature Branch Oluşturun

```bash
git checkout -b add-my-name
```

### Adım 5: CONTRIBUTORS.md'ye İsminizi Ekleyin

Aşağıdaki dosyayı açın veya oluşturun ve isminizi ekleyin:

```bash
# CONTRIBUTORS.md dosyasını düzenleyin
# Eğer yoksa oluşturun:
echo "# 🤝 Katkıda Bulunanlar" > CONTRIBUTORS.md
echo "" >> CONTRIBUTORS.md
echo "Bu eğitime katkıda bulunan herkese teşekkürler!" >> CONTRIBUTORS.md
echo "" >> CONTRIBUTORS.md
echo "## Katılımcılar" >> CONTRIBUTORS.md
echo "" >> CONTRIBUTORS.md
echo "- [Sizin Adınız](https://github.com/KULLANICI_ADINIZ)" >> CONTRIBUTORS.md
```

### Adım 6: Commit ve Push

```bash
git add CONTRIBUTORS.md
git commit -m "docs: CONTRIBUTORS.md'ye ismimi ekledim"
git push origin add-my-name
```

### Adım 7: Pull Request Açın

1. GitHub'da fork'unuza gidin
2. "Compare & pull request" butonuna tıklayın
3. PR açıklamasını doldurun
4. "Create pull request" tıklayın

---

## 📊 Fork Workflow Diyagramı

```
┌─────────────────────────────────────────────────────────────────────┐
│                     FORK & PR WORKFLOW                               │
│                                                                      │
│   Original Repo          Your Fork           Your Computer          │
│   (Furk4nBulut)          (GitHub)            (Local)                │
│                                                                      │
│   ┌─────────┐    FORK    ┌─────────┐   CLONE   ┌─────────┐         │
│   │ Upstream│ ─────────▶ │ Origin  │ ────────▶ │  Local  │         │
│   └─────────┘            └─────────┘            └─────────┘         │
│        ▲                      ▲                      │              │
│        │                      │                      │              │
│        │    Pull Request      │        Push          │              │
│        └──────────────────────┴──────────────────────┘              │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 🔄 Fork'u Güncel Tutma

```bash
# Upstream'den değişiklikleri çekin
git fetch upstream

# main branch'a geçin
git checkout main

# Upstream ile merge edin
git merge upstream/main

# Fork'unuza push edin
git push origin main
```

---

## ✅ Kontrol Listesi

- [ ] Repository fork edildi
- [ ] Fork clone edildi
- [ ] Upstream eklendi
- [ ] Feature branch oluşturuldu
- [ ] Değişiklik yapıldı
- [ ] Commit yapıldı
- [ ] Push edildi
- [ ] Pull Request açıldı

---

## ➡️ Sonraki Lab

**[Lab 4: Takım Çalışması →](../lab-04-team-work)**

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

</div>
