# 🧪 Lab 2: Branch Yönetimi ve Merge

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-Orta-yellow?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-45_dk-blue?style=for-the-badge)]()

*Branch oluşturma, geçiş yapma ve birleştirme işlemlerini öğrenin*

</div>

---

## 🎯 Öğrenme Hedefleri

Bu lab'ı tamamladığınızda:

- [x] Branch neden kullanıldığını anlayacaksınız
- [x] Yeni branch oluşturabileceksiniz
- [x] Branch'lar arası geçiş yapabileceksiniz
- [x] Branch'ları merge edebileceksiniz
- [x] Merge conflict çözebileceksiniz

---

## 📋 Ön Gereksinimler

- ✅ Lab 1 tamamlanmış
- ✅ Çalışan bir GitHub repository'niz var

---

## 📝 Bölüm 1: Branch Oluşturma

### Adım 1: Mevcut Branch'ları Görme

```bash
# Mevcut repo'nuza gidin
cd benim-ilk-projem

# Branch'ları listeleyin
git branch

# Çıktı:
# * main
```

> 💡 Yıldız (*) aktif branch'ı gösterir.

### Adım 2: Yeni Branch Oluşturma

```bash
# feature-hello adında yeni branch oluşturun
git branch feature-hello

# Branch'ları tekrar listeleyin
git branch

# Çıktı:
# feature-hello
# * main
```

### Adım 3: Branch'a Geçiş

```bash
# feature-hello branch'ına geçin
git checkout feature-hello

# Veya modern yöntem:
git switch feature-hello

# Çıktı:
# Switched to branch 'feature-hello'
```

### Adım 4: Tek Komutta Oluştur ve Geç

```bash
# Yeni branch oluştur ve geç
git checkout -b feature-world

# Veya:
git switch -c feature-world
```

---

## 📝 Bölüm 2: Branch'ta Çalışma

### Adım 5: feature-hello Branch'ında Değişiklik

```bash
# feature-hello branch'ına geçin
git checkout feature-hello

# Yeni dosya oluşturun
echo "Merhaba Dünya!" > hello.txt

# Commit yapın
git add hello.txt
git commit -m "feat: hello.txt dosyası eklendi"
```

### Adım 6: main Branch'ında Değişiklik

```bash
# main'e dönün
git checkout main

# hello.txt'nin olmadığını kontrol edin
ls
# Çıktı: README.md (hello.txt yok!)

# Farklı bir değişiklik yapın
echo "" >> README.md
echo "## 📅 Son Güncelleme" >> README.md
echo "Lab 2 tamamlandı." >> README.md

git add README.md
git commit -m "docs: README güncellendi"
```

---

## 📝 Bölüm 3: Branch Birleştirme (Merge)

### Adım 7: feature-hello'yu main'e merge

```bash
# main branch'ında olduğunuzdan emin olun
git checkout main

# feature-hello'yu merge edin
git merge feature-hello

# Çıktı:
# Merge made by the 'recursive' strategy.
# hello.txt | 1 +
# 1 file changed, 1 insertion(+)
# create mode 100644 hello.txt
```

### Adım 8: Sonucu Kontrol Edin

```bash
# Dosyaları listeleyin
ls
# Çıktı: README.md hello.txt

# Commit geçmişini görün
git log --oneline --graph --all
```

---

## 📝 Bölüm 4: Merge Conflict Simülasyonu

### Adım 9: Conflict Senaryosu Oluşturma

```bash
# Yeni branch oluşturun
git checkout -b feature-color

# greeting.txt oluşturun
echo "Renk: Mavi" > greeting.txt
git add greeting.txt
git commit -m "feat: greeting.txt - mavi renk"

# main'e dönün
git checkout main

# Aynı dosyayı farklı içerikle oluşturun
echo "Renk: Kırmızı" > greeting.txt
git add greeting.txt
git commit -m "feat: greeting.txt - kırmızı renk"
```

### Adım 10: Conflict Oluşturma

```bash
# feature-color'u merge etmeyi deneyin
git merge feature-color

# Çıktı:
# CONFLICT (add/add): Merge conflict in greeting.txt
# Automatic merge failed; fix conflicts and then commit the result.
```

### Adım 11: Conflict Görüntüleme

```bash
# Durumu kontrol edin
git status

# greeting.txt içeriğini görün
cat greeting.txt

# Çıktı:
# <<<<<<< HEAD
# Renk: Kırmızı
# =======
# Renk: Mavi
# >>>>>>> feature-color
```

### Adım 12: Conflict Çözme

```bash
# Dosyayı düzenleyin - conflict işaretlerini temizleyin
# İstediğiniz değeri yazın:
echo "Renk: Mor (Mavi + Kırmızı)" > greeting.txt

# Çözümü stage'e alın
git add greeting.txt

# Merge commit yapın
git commit -m "merge: feature-color birleştirildi, renk mor olarak belirlendi"
```

---

## 📝 Bölüm 5: Temizlik

### Adım 13: Birleştirilmiş Branch'ları Silme

```bash
# Merge edilmiş branch'ları silin
git branch -d feature-hello
git branch -d feature-color

# Branch listesini kontrol edin
git branch
# Çıktı: * main
```

### Adım 14: Değişiklikleri Push Etme

```bash
# Tüm değişiklikleri GitHub'a gönderin
git push origin main
```

---

## ✅ Kontrol Listesi

- [ ] Yeni branch oluşturuldu
- [ ] Branch'lar arası geçiş yapıldı
- [ ] Feature branch'ta değişiklik yapıldı
- [ ] Branch main'e merge edildi
- [ ] Merge conflict oluşturuldu
- [ ] Conflict çözüldü
- [ ] Eski branch'lar silindi
- [ ] Değişiklikler push edildi

---

## 📊 Branch Stratejileri

### Git Flow
```
main ─────────────────────●─────────────●
                         ╱               ╲
develop ───●───●───●───●───●───●───●───●───●
            ╲               ╱
feature      ╲─────●───●──╱
```

### GitHub Flow (Önerilen)
```
main ───────────────────────●───────────────●
                           ╱                 ╲
feature/login ────●───●───●                   ╲
                                               ╲
feature/dashboard ──────────────●───●───●──────●
```

---

## 📚 Öğrenilen Komutlar

| Komut | Açıklama |
|:------|:---------|
| `git branch` | Branch'ları listeler |
| `git branch <isim>` | Yeni branch oluşturur |
| `git checkout <branch>` | Branch'a geçer |
| `git checkout -b <isim>` | Oluştur ve geç |
| `git switch <branch>` | Branch'a geçer (modern) |
| `git switch -c <isim>` | Oluştur ve geç (modern) |
| `git merge <branch>` | Branch'ı birleştirir |
| `git branch -d <isim>` | Branch'ı siler |

---

## 🎯 Bonus Görevler

### Bonus 1: Branch İsimlendirme Pratiği
```bash
# Farklı tipte branch'lar oluşturun
git branch feature/user-auth
git branch bugfix/login-error
git branch hotfix/security-patch
git branch docs/update-readme
```

### Bonus 2: Görsel Log
```bash
git log --oneline --graph --all --decorate
```

---

## ➡️ Sonraki Lab

**[Lab 3: Fork ve Collaboration →](../lab-03-collaboration)**

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

</div>
