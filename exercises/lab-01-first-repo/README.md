# 🧪 Lab 1: İlk GitHub Repository'nizi Oluşturun

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-Başlangıç-green?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-30_dk-blue?style=for-the-badge)]()

*Sıfırdan bir GitHub repository'si oluşturmayı öğrenin*

</div>

---

## 🎯 Öğrenme Hedefleri

Bu lab'ı tamamladığınızda:

- [x] Git ile yeni bir proje başlatabileceksiniz
- [x] Dosya oluşturup commit yapabileceksiniz
- [x] GitHub'da repository oluşturabileceksiniz
- [x] Yerel değişiklikleri GitHub'a gönderebileceksiniz

---

## 📋 Ön Gereksinimler

- ✅ Git kurulu (kontrol: `git --version`)
- ✅ GitHub hesabı oluşturulmuş
- ✅ Git yapılandırması yapılmış:
  ```bash
  git config --global user.name "Adınız"
  git config --global user.email "email@example.com"
  ```

---

## 📝 Adımlar

### Adım 1: Proje Klasörü Oluşturma

Terminal veya komut satırını açın ve şu komutları çalıştırın:

```bash
# Masaüstünde yeni klasör oluşturun
cd ~/Desktop
mkdir benim-ilk-projem
cd benim-ilk-projem
```

### Adım 2: Git Repository Başlatma

```bash
# Git'i başlatın
git init

# Çıktı:
# Initialized empty Git repository in .../benim-ilk-projem/.git/
```

> 💡 **Not:** Bu komut `.git` adında gizli bir klasör oluşturur. Bu klasör projenizin tüm versiyon geçmişini içerir.

### Adım 3: README Dosyası Oluşturma

```bash
# README.md dosyası oluşturun
echo "# Benim İlk Projem" > README.md
echo "" >> README.md
echo "Bu proje GitHub öğrenme sürecimde oluşturduğum ilk projedir." >> README.md
echo "" >> README.md
echo "## 📝 Öğrendiklerim" >> README.md
echo "" >> README.md
echo "- Git temel komutları" >> README.md
echo "- GitHub repository oluşturma" >> README.md
echo "- Commit yapma" >> README.md
```

### Adım 4: Durumu Kontrol Etme

```bash
git status

# Çıktı:
# On branch main
# No commits yet
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#         README.md
```

### Adım 5: Değişiklikleri Stage'e Alma

```bash
# README.md'yi stage'e ekleyin
git add README.md

# Veya tüm değişiklikleri eklemek için:
git add .
```

### Adım 6: İlk Commit

```bash
git commit -m "feat: ilk commit - README eklendi"

# Çıktı:
# [main (root-commit) abc1234] feat: ilk commit - README eklendi
#  1 file changed, 7 insertions(+)
#  create mode 100644 README.md
```

### Adım 7: GitHub'da Repository Oluşturma

1. [github.com](https://github.com) adresine gidin
2. Sağ üstteki **+** butonuna tıklayın
3. **New repository** seçin
4. Repository adını yazın: `benim-ilk-projem`
5. **Public** seçili kalsın
6. ⚠️ "Add a README file" seçeneğini **işaretlemeyin**
7. **Create repository** butonuna tıklayın

### Adım 8: Uzak Repository Ekleme

GitHub'dan aldığınız URL'i kullanarak:

```bash
# Uzak repo ekleyin (URL'i kendi repo'nuzla değiştirin)
git remote add origin https://github.com/KULLANICI-ADINIZ/benim-ilk-projem.git

# Branch adını main yapın
git branch -M main

# İlk push
git push -u origin main
```

### Adım 9: GitHub'da Kontrol

1. GitHub'da repo'nuza gidin
2. README.md dosyasının göründüğünü doğrulayın
3. Commit geçmişine bakın

---

## ✅ Kontrol Listesi

Aşağıdaki adımları tamamladınız mı?

- [ ] Yerel klasör oluşturuldu
- [ ] `git init` çalıştırıldı
- [ ] README.md oluşturuldu
- [ ] `git add` ile değişiklikler eklendi
- [ ] `git commit` ile commit yapıldı
- [ ] GitHub'da repo oluşturuldu
- [ ] `git remote add` ile bağlantı kuruldu
- [ ] `git push` ile gönderildi
- [ ] GitHub'da görüntülendi

---

## 🎯 Bonus Görevler

### Bonus 1: Ek Dosya Ekleyin

```bash
# .gitignore dosyası ekleyin
echo "node_modules/" > .gitignore
echo ".env" >> .gitignore
echo ".DS_Store" >> .gitignore

git add .gitignore
git commit -m "chore: .gitignore eklendi"
git push
```

### Bonus 2: README'yi Güncelleyin

```bash
# README'ye yeni bölüm ekleyin
echo "" >> README.md
echo "## 🛠️ Teknolojiler" >> README.md
echo "" >> README.md
echo "- Git" >> README.md
echo "- GitHub" >> README.md

git add README.md
git commit -m "docs: README'ye teknolojiler bölümü eklendi"
git push
```

### Bonus 3: Commit Geçmişini Görüntüleyin

```bash
# Commit geçmişi
git log --oneline

# Detaylı geçmiş
git log --oneline --graph --all
```

---

## 🚨 Yaygın Hatalar ve Çözümleri

### Hata 1: "fatal: not a git repository"
```bash
# Çözüm: Doğru klasörde olduğunuzdan emin olun
cd benim-ilk-projem
git init
```

### Hata 2: "failed to push some refs"
```bash
# Çözüm: Önce pull yapın
git pull --rebase origin main
git push
```

### Hata 3: "remote origin already exists"
```bash
# Çözüm: Mevcut remote'u silin ve tekrar ekleyin
git remote remove origin
git remote add origin https://github.com/USER/repo.git
```

---

## 📚 Öğrenilen Komutlar

| Komut | Açıklama |
|:------|:---------|
| `git init` | Yeni Git repository başlatır |
| `git status` | Mevcut durumu gösterir |
| `git add` | Değişiklikleri stage'e ekler |
| `git commit -m` | Değişiklikleri kaydeder |
| `git remote add` | Uzak repository bağlantısı ekler |
| `git push` | Değişiklikleri uzak repoya gönderir |
| `git log` | Commit geçmişini gösterir |

---

## ➡️ Sonraki Lab

Tebrikler! İlk GitHub repository'nizi oluşturdunuz! 🎉

**[Lab 2: Branch Yönetimi →](../lab-02-branching)**

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

</div>
