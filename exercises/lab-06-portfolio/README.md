# 🧪 Lab 6: Profesyonel Portfolyo Oluşturma

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-Orta-yellow?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-60_dk-blue?style=for-the-badge)]()

*GitHub profilinizi profesyonel bir vitrine dönüştürün*

</div>

---

## 🎯 Öğrenme Hedefleri

- [x] GitHub Profile README oluşturabileceksiniz
- [x] İstatistik widget'ları ekleyebileceksiniz
- [x] GitHub Pages ile site yayınlayabileceksiniz
- [x] Profilinizi optimize edebileceksiniz

---

## 📝 Bölüm 1: Profile README

### Adım 1: Özel Repo Oluşturma

1. GitHub'da **New repository** tıklayın
2. Repository adı = **Kullanıcı adınız** (örn: `furkandev`)
3. ✅ **Public** seçin
4. ✅ **Add a README file** işaretleyin
5. **Create repository** tıklayın

> 💡 "furkandev/furkandev is a ✨ special ✨ repository" mesajını görmelisiniz!

### Adım 2: README Düzenleme

README.md'yi düzenleyin:

```markdown
<div align="center">

# 👋 Merhaba, Ben [Adınız]!

### 💻 [Ünvanınız] | 📍 Şehir, Türkiye

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/KULLANICI)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KULLANICI)

</div>

---

## 🚀 Hakkımda

- 🔭 Şu anda **[Şirket/Okul]**'da çalışıyorum/okuyorum
- 🌱 **[Teknoloji]** öğreniyorum
- 💬 **[Konu]** hakkında soru sorabilirsiniz
- 📫 Bana ulaşın: **email@example.com**

---

## 🛠️ Teknolojiler

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 📊 GitHub İstatistiklerim

![Stats](https://github-readme-stats.vercel.app/api?username=KULLANICI&show_icons=true&theme=radical)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=KULLANICI&layout=compact&theme=radical)

---

![Profile Views](https://komarev.com/ghpvc/?username=KULLANICI&color=blueviolet)
```

### Adım 3: Commit ve Görüntüle

```bash
git add README.md
git commit -m "feat: profile README oluşturuldu"
git push
```

**Profilinize gidin ve README'yi görün!**

---

## 📝 Bölüm 2: Widget'lar

### GitHub Stats

```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=KULLANICI&show_icons=true&theme=radical)
```

**Temalar:** `radical`, `tokyonight`, `dracula`, `dark`, `gruvbox`

### Top Languages

```markdown
![Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=KULLANICI&layout=compact&theme=radical)
```

### Streak Stats

```markdown
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=KULLANICI&theme=radical)
```

### Profile Views

```markdown
![Views](https://komarev.com/ghpvc/?username=KULLANICI&color=blueviolet)
```

### Trophies

```markdown
![Trophies](https://github-profile-trophy.vercel.app/?username=KULLANICI&theme=radical&row=1)
```

---

## 📝 Bölüm 3: GitHub Pages

### Adım 4: Portfolyo Reposu

1. Yeni repo oluşturun: `kullanici.github.io`
2. Clone edin:
   ```bash
   git clone https://github.com/KULLANICI/KULLANICI.github.io.git
   cd KULLANICI.github.io
   ```

### Adım 5: Basit Portfolyo

`index.html` oluşturun:

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolyom</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }
        .container {
            text-align: center;
            padding: 2rem;
        }
        h1 { font-size: 3rem; margin-bottom: 1rem; }
        p { font-size: 1.2rem; opacity: 0.9; margin-bottom: 2rem; }
        .links a {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            color: white;
            text-decoration: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            margin: 0.5rem;
            transition: transform 0.3s;
        }
        .links a:hover { transform: scale(1.05); }
    </style>
</head>
<body>
    <div class="container">
        <h1>👋 Merhaba!</h1>
        <p>Ben [Adınız], [Ünvanınız]</p>
        <div class="links">
            <a href="https://github.com/KULLANICI">GitHub</a>
            <a href="https://linkedin.com/in/KULLANICI">LinkedIn</a>
            <a href="mailto:email@example.com">Email</a>
        </div>
    </div>
</body>
</html>
```

### Adım 6: Yayınla

```bash
git add .
git commit -m "feat: portfolyo sitesi oluşturuldu"
git push
```

**Birkaç dakika bekleyin, sonra `https://KULLANICI.github.io` adresini ziyaret edin!**

---

## 📝 Bölüm 4: Profil Optimizasyonu

### Adım 7: Profil Düzenleme

1. GitHub profilinize gidin
2. **Edit profile** tıklayın
3. Doldurun:
   - **Name:** Tam adınız
   - **Bio:** Kısa tanıtım (160 karakter)
   - **Company:** Şirket/Okul
   - **Location:** Şehir, Ülke
   - **Website:** Portfolyo URL'niz
   - **Social:** Twitter, LinkedIn

### Adım 8: En İyi Repo'ları Pinleyin

1. Profilinizde **Customize your pins** tıklayın
2. En iyi 6 repo'nuzu seçin
3. **Save pins** tıklayın

---

## ✅ Kontrol Listesi

- [ ] Profile README oluşturuldu
- [ ] İstatistik widget'ları eklendi
- [ ] Badge'ler eklendi
- [ ] GitHub Pages sitesi yayınlandı
- [ ] Profil bilgileri güncellendi
- [ ] En iyi repolar pinlendi

---

## 🎯 Bonus: Gelişmiş Widget'lar

### Activity Graph

```markdown
![Graph](https://github-readme-activity-graph.vercel.app/graph?username=KULLANICI&theme=react-dark)
```

### Typing Animation

```markdown
[![Typing SVG](https://readme-typing-svg.demolab.com?lines=Full+Stack+Developer;Open+Source+Contributor)](https://git.io/typing-svg)
```

### Random Dev Quote

```markdown
![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)
```

---

## 🎉 Tebrikler!

GitHub Workshop eğitimini tamamladınız!

### 📝 Öğrendikleriniz:

- ✅ Git temel komutları ve workflow
- ✅ Branch stratejileri ve merge
- ✅ Fork, Clone ve PR süreci
- ✅ Organization ve takım çalışması
- ✅ GitHub Actions ile otomasyon
- ✅ Profesyonel portfolyo oluşturma

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

**🎓 Eğitimi tamamladığınız için tebrikler!**

</div>
