# ⚡ Git Komutları Cheat Sheet

<div align="center">

[![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)]()

*Günlük kullanım için Git komutları hızlı referansı*

</div>

---

## 🚀 Başlangıç

| Komut | Açıklama |
|:------|:---------|
| `git init` | Mevcut klasörde yeni Git repository başlatır |
| `git clone <url>` | Uzak repository'yi yerel bilgisayara kopyalar |
| `git clone <url> <klasör>` | Belirtilen klasöre klonlar |

---

## ⚙️ Yapılandırma

```bash
# Kullanıcı bilgileri
git config --global user.name "Adınız"
git config --global user.email "email@example.com"

# Ayarları görüntüle
git config --list

# Editör ayarı
git config --global core.editor "code --wait"

# Varsayılan branch adı
git config --global init.defaultBranch main
```

---

## 📝 Temel İş Akışı

### Durum ve Farklar

| Komut | Açıklama |
|:------|:---------|
| `git status` | Çalışma dizininin durumunu gösterir |
| `git status -s` | Kısa format |
| `git diff` | Staged olmayan değişiklikleri gösterir |
| `git diff --staged` | Staged değişiklikleri gösterir |
| `git diff HEAD` | Son commit'ten bu yana tüm değişiklikler |

### Stage (Add)

| Komut | Açıklama |
|:------|:---------|
| `git add <dosya>` | Belirli dosyayı stage'e ekler |
| `git add .` | Tüm değişiklikleri ekler |
| `git add *.js` | Pattern ile eşleşenleri ekler |
| `git add -p` | İnteraktif ekleme (parça parça) |
| `git reset HEAD <dosya>` | Dosyayı unstage eder |

### Commit

| Komut | Açıklama |
|:------|:---------|
| `git commit -m "mesaj"` | Mesaj ile commit |
| `git commit` | Editörde mesaj yazma |
| `git commit -am "mesaj"` | Add + Commit (sadece tracked) |
| `git commit --amend` | Son commit'i düzenle |
| `git commit --amend -m "yeni mesaj"` | Mesajı değiştir |

---

## 🌿 Branch Yönetimi

### Branch İşlemleri

| Komut | Açıklama |
|:------|:---------|
| `git branch` | Yerel branch'ları listele |
| `git branch -a` | Tüm branch'ları listele |
| `git branch -r` | Uzak branch'ları listele |
| `git branch <isim>` | Yeni branch oluştur |
| `git branch -d <isim>` | Branch sil (merged) |
| `git branch -D <isim>` | Branch sil (force) |
| `git branch -m <yeni>` | Branch yeniden adlandır |

### Geçiş (Checkout / Switch)

| Komut | Açıklama |
|:------|:---------|
| `git checkout <branch>` | Branch'a geç |
| `git checkout -b <isim>` | Oluştur ve geç |
| `git switch <branch>` | Branch'a geç (modern) |
| `git switch -c <isim>` | Oluştur ve geç (modern) |
| `git checkout -` | Önceki branch'a dön |

### Merge

| Komut | Açıklama |
|:------|:---------|
| `git merge <branch>` | Branch'ı birleştir |
| `git merge --no-ff <branch>` | Her zaman merge commit oluştur |
| `git merge --squash <branch>` | Squash merge |
| `git merge --abort` | Merge'ü iptal et |

---

## 🔄 Uzak Repository (Remote)

### Remote Yönetimi

| Komut | Açıklama |
|:------|:---------|
| `git remote -v` | Remote'ları listele |
| `git remote add <isim> <url>` | Remote ekle |
| `git remote remove <isim>` | Remote sil |
| `git remote rename <eski> <yeni>` | Remote yeniden adlandır |
| `git remote set-url <isim> <url>` | URL değiştir |

### Senkronizasyon

| Komut | Açıklama |
|:------|:---------|
| `git fetch` | Değişiklikleri indir (merge etme) |
| `git fetch <remote>` | Belirli remote'dan fetch |
| `git pull` | Fetch + Merge |
| `git pull --rebase` | Fetch + Rebase |
| `git push` | Değişiklikleri gönder |
| `git push -u origin <branch>` | Upstream ayarla ve push |
| `git push --force` | Zorla push (dikkat!) |
| `git push --tags` | Tüm tag'leri gönder |

---

## 📜 Geçmiş ve Log

| Komut | Açıklama |
|:------|:---------|
| `git log` | Commit geçmişi |
| `git log --oneline` | Tek satır format |
| `git log --graph` | Görsel graph |
| `git log --all` | Tüm branch'lar |
| `git log -n 5` | Son 5 commit |
| `git log --author="Ad"` | Yazara göre filtrele |
| `git log --since="2024-01-01"` | Tarihten sonra |
| `git log --grep="feat"` | Mesajda arama |
| `git log <dosya>` | Dosya geçmişi |
| `git show <commit>` | Commit detayı |
| `git blame <dosya>` | Satır bazlı yazar bilgisi |

---

## ↩️ Geri Alma

### Değişiklikleri Geri Alma

| Komut | Açıklama |
|:------|:---------|
| `git checkout -- <dosya>` | Dosya değişikliğini geri al |
| `git restore <dosya>` | Dosya değişikliğini geri al (modern) |
| `git restore --staged <dosya>` | Unstage (modern) |

### Reset

| Komut | Açıklama |
|:------|:---------|
| `git reset --soft HEAD~1` | Son commit'i geri al (değişiklikler staged) |
| `git reset --mixed HEAD~1` | Son commit'i geri al (değişiklikler unstaged) |
| `git reset --hard HEAD~1` | Son commit'i tamamen sil |
| `git reset --hard <commit>` | Belirli commit'e dön |

### Revert

| Komut | Açıklama |
|:------|:---------|
| `git revert <commit>` | Commit'i geri alan yeni commit oluştur |
| `git revert --no-commit <commit>` | Commit oluşturmadan revert |

---

## 📦 Stash (Geçici Saklama)

| Komut | Açıklama |
|:------|:---------|
| `git stash` | Değişiklikleri sakla |
| `git stash save "mesaj"` | Mesaj ile sakla |
| `git stash list` | Stash listesi |
| `git stash pop` | Son stash'ı geri al ve sil |
| `git stash apply` | Son stash'ı geri al (silme) |
| `git stash apply stash@{n}` | Belirli stash'ı uygula |
| `git stash drop stash@{n}` | Stash sil |
| `git stash clear` | Tüm stash'ları sil |
| `git stash show -p` | Stash içeriğini göster |

---

## 🔀 Rebase

| Komut | Açıklama |
|:------|:---------|
| `git rebase <branch>` | Branch üzerine rebase |
| `git rebase -i HEAD~n` | İnteraktif rebase (son n commit) |
| `git rebase --continue` | Conflict çözdükten sonra devam |
| `git rebase --abort` | Rebase'i iptal et |
| `git rebase --skip` | Mevcut commit'i atla |

### İnteraktif Rebase Komutları

```
pick   (p) - commit'i kullan
reword (r) - commit'i kullan, mesajı düzenle
edit   (e) - commit'i kullan, durarak düzenle
squash (s) - önceki ile birleştir
fixup  (f) - squash ama mesajı at
drop   (d) - commit'i sil
```

---

## 🍒 Cherry-Pick

| Komut | Açıklama |
|:------|:---------|
| `git cherry-pick <commit>` | Commit'i mevcut branch'a uygula |
| `git cherry-pick --no-commit <commit>` | Commit oluşturmadan uygula |
| `git cherry-pick <commit1> <commit2>` | Birden fazla commit |
| `git cherry-pick --abort` | İptal et |

---

## 🏷️ Tag

| Komut | Açıklama |
|:------|:---------|
| `git tag` | Tag'leri listele |
| `git tag <isim>` | Lightweight tag |
| `git tag -a <isim> -m "mesaj"` | Annotated tag |
| `git tag -a <isim> <commit>` | Belirli commit'e tag |
| `git show <tag>` | Tag detayı |
| `git push origin <tag>` | Tag'i push et |
| `git push origin --tags` | Tüm tag'leri push et |
| `git tag -d <isim>` | Yerel tag sil |
| `git push origin --delete <tag>` | Uzak tag sil |

---

## 🔍 Arama ve Debug

| Komut | Açıklama |
|:------|:---------|
| `git grep "text"` | Çalışma dizininde ara |
| `git log -S "text"` | Commit'lerde değişiklik ara |
| `git bisect start` | Binary search ile bug bulma |
| `git bisect good <commit>` | İyi commit işaretle |
| `git bisect bad <commit>` | Kötü commit işaretle |

---

## ⚡ Kısayollar (Alias)

```bash
# Önerilen alias'lar
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.last 'log -1 HEAD'
git config --global alias.lg 'log --oneline --graph --all'
```

---

## 📚 Faydalı Kaynaklar

- [Git Resmi Dokümantasyon](https://git-scm.com/doc)
- [Git Book (Türkçe)](https://git-scm.com/book/tr)
- [GitHub Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

<div align="center">

**[🏠 Ana Sayfa](../README.md)**

</div>
