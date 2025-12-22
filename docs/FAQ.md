# ❓ Sık Sorulan Sorular (FAQ)

<div align="center">

[![FAQ](https://img.shields.io/badge/FAQ-Sık_Sorulan_Sorular-blue?style=for-the-badge)]()

</div>

---

## 📌 Genel Sorular

### Git ve GitHub aynı şey mi?

**Hayır!**

| Git | GitHub |
|:----|:-------|
| Versiyon kontrol sistemi | Bulut tabanlı hosting platformu |
| Bilgisayarınızda çalışır | İnternette çalışır |
| Linus Torvalds tarafından geliştirildi (2005) | GitHub Inc. tarafından geliştirildi (2008) |
| Ücretsiz ve açık kaynak | Ücretsiz + Premium planlar |

> 💡 **Analoji:** Git bir müzik formatıdır (MP3 gibi), GitHub ise müzik paylaşım platformudur (Spotify gibi).

---

### GitHub ücretsiz mi?

**Evet, temel özellikler ücretsiz!**

Ücretsiz plan şunları içerir:
- ✅ Sınırsız public repository
- ✅ Sınırsız private repository (3 collaborator'a kadar)
- ✅ GitHub Actions (2,000 dakika/ay)
- ✅ GitHub Pages
- ✅ GitHub Copilot (öğrenciler için ücretsiz)

---

### GitHub Student Pack nasıl alınır?

1. [education.github.com/pack](https://education.github.com/pack) adresine gidin
2. "Get your pack" butonuna tıklayın
3. GitHub hesabınızla giriş yapın
4. Okul e-postanızı (.edu.tr) doğrulayın
   - Veya öğrenci belgesi yükleyin
5. 1-7 gün içinde onay bekleyin

---

## 🔧 Teknik Sorular

### "Permission denied" hatası alıyorum

**Olası çözümler:**

1. **SSH key kontrolü:**
   ```bash
   ssh -T git@github.com
   ```

2. **Credential yenileme:**
   ```bash
   git config --global credential.helper store
   ```

3. **HTTPS yerine SSH kullanın:**
   ```bash
   git remote set-url origin git@github.com:USER/REPO.git
   ```

---

### "fatal: not a git repository" hatası

Bu hata, Git komutlarını Git repository olmayan bir klasörde çalıştırdığınızda oluşur.

**Çözüm:**
```bash
# Doğru klasöre gidin
cd proje-klasoru

# Veya yeni repo başlatın
git init
```

---

### Merge conflict nasıl çözülür?

1. **Conflict'li dosyaları görün:**
   ```bash
   git status
   ```

2. **Dosyayı açın ve işaretleri düzenleyin:**
   ```
   <<<<<<< HEAD
   Sizin değişikliğiniz
   =======
   Gelen değişiklik
   >>>>>>> branch-name
   ```

3. **İşaretleri silin, istediğiniz kodu bırakın**

4. **Değişiklikleri kaydedin:**
   ```bash
   git add .
   git commit -m "merge: conflict çözüldü"
   ```

---

### Yanlışlıkla commit ettim, nasıl geri alırım?

**Son commit'i geri almak için:**

```bash
# Değişiklikleri koruyarak (staged olarak)
git reset --soft HEAD~1

# Değişiklikleri koruyarak (unstaged olarak)
git reset --mixed HEAD~1

# Değişiklikleri tamamen silmek için (DİKKAT!)
git reset --hard HEAD~1
```

**Push edilmiş commit için (güvenli):**
```bash
git revert HEAD
```

---

### Branch silindikten sonra kurtarılabilir mi?

**Evet, reflog ile kurtarılabilir:**

```bash
# Reflog'a bak
git reflog

# Silinen branch'ın son commit'ini bul
# abc1234 HEAD@{5}: commit: son commit

# Kurtarma
git checkout -b kurtarilan-branch abc1234
```

---

### .gitignore çalışmıyor, neden?

**Muhtemelen dosyalar zaten tracked.**

```bash
# Cache'i temizle
git rm -r --cached .

# Tekrar ekle
git add .

# Commit
git commit -m "chore: .gitignore güncellendi"
```

---

## 📚 Kavram Soruları

### Fork ve Clone arasındaki fark nedir?

| | Fork | Clone |
|:|:-----|:------|
| **Konum** | GitHub'da (kendi hesabınızda) | Bilgisayarınızda |
| **Amaç** | Başkasının projesine katkı | Projeyi indirme |
| **Bağlantı** | Orijinal repo ile ilişkili | Sadece remote bağlantısı |

---

### Rebase ve Merge arasındaki fark nedir?

| | Merge | Rebase |
|:|:------|:-------|
| **Geçmiş** | Merge commit oluşturur | Linear geçmiş oluşturur |
| **Karmaşıklık** | Basit | Daha karmaşık |
| **Güvenlik** | Geçmişi değiştirmez | Geçmişi yeniden yazar |
| **Kullanım** | Takım çalışmasında | Bireysel branch temizliğinde |

> ⚠️ **Altın Kural:** Push edilmiş commit'leri asla rebase yapmayın!

---

### Conventional Commits neden kullanmalıyım?

**Avantajlar:**
- 📖 Okunabilir commit geçmişi
- 🔍 Kolay arama ve filtreleme
- 📝 Otomatik changelog oluşturma
- 🤖 CI/CD entegrasyonu
- 🏷️ Semantic versioning uyumu

---

### main ve master arasındaki fark nedir?

**Fonksiyonel fark yok**, sadece isim farklı.

- **master:** Eski varsayılan isim
- **main:** 2020'den beri yeni varsayılan isim

```bash
# master'ı main olarak yeniden adlandırma
git branch -m master main
git push -u origin main
```

---

## 🎓 Öğrenme Soruları

### Hangi GUI aracını kullanmalıyım?

| Araç | Önerilen İçin |
|:-----|:-------------|
| **GitHub Desktop** | Yeni başlayanlar |
| **GitKraken** | Görsel öğrenmek isteyenler |
| **VS Code** | Zaten VS Code kullananlar |
| **Terminal** | İleri seviye kullanıcılar |

---

### Hangi sırayla öğrenmeliyim?

```
1️⃣ Git temel komutlar (init, add, commit, push, pull)
2️⃣ Branch yönetimi (checkout, merge)
3️⃣ GitHub (PR, Issues)
4️⃣ Takım çalışması (Fork, Code Review)
5️⃣ İleri komutlar (rebase, stash, cherry-pick)
6️⃣ Otomasyon (GitHub Actions)
```

---

## 🔗 Daha Fazla Yardım

- **Sorularınız için:** [GitHub Discussions](https://github.com/Furk4nBulut/Github-Workshop/discussions)
- **Hata bildirmek için:** [GitHub Issues](https://github.com/Furk4nBulut/Github-Workshop/issues)
- **Resmi Dokümantasyon:** [docs.github.com](https://docs.github.com)
- **Git Book (Türkçe):** [git-scm.com/book/tr](https://git-scm.com/book/tr)

---

<div align="center">

**[🏠 Ana Sayfa](../README.md)**

</div>
