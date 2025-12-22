# 🧪 Lab 4: Takım Çalışması ve Proje Yönetimi

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-Orta-yellow?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-45_dk-blue?style=for-the-badge)]()

*GitHub Organization, Issues ve Projects ile takım çalışması yapın*

</div>

---

## 🎯 Öğrenme Hedefleri

- [x] GitHub Organization oluşturabileceksiniz
- [x] Takım üyelerini yönetebileceksiniz
- [x] Issue açıp takip edebileceksiniz
- [x] Project board ile görev yönetimi yapabileceksiniz

---

## 📝 Bölüm 1: Organization Oluşturma

### Adım 1: Yeni Organization

1. GitHub'da sağ üstteki **+** menüsüne tıklayın
2. **New organization** seçin
3. **Free** planı seçin
4. Organization adını girin: `test-org-KULLANICI`
5. Email adresinizi girin
6. **Create organization** tıklayın

### Adım 2: Organization Ayarları

1. Organization sayfasına gidin
2. **Settings** sekmesine gidin
3. Profile bölümünde:
   - Açıklama ekleyin
   - Avatar yükleyin

---

## 📝 Bölüm 2: Repo ve Takım Yönetimi

### Adım 3: Organization'a Repo Ekle

```bash
# Yeni repo oluşturun (GitHub'da)
# Repo adı: takim-projesi
# Visibility: Public
# README ile initialize edin
```

### Adım 4: Takım Oluşturma

1. **Teams** sekmesine gidin
2. **New team** tıklayın
3. Team adı: `developers`
4. Açıklama ekleyin
5. **Create team** tıklayın
6. Üye davet edin (kendinizi de ekleyebilirsiniz)

---

## 📝 Bölüm 3: Issues ile Proje Takibi

### Adım 5: Issue Oluşturma

1. Repo'da **Issues** sekmesine gidin
2. **New issue** tıklayın
3. Şu bilgileri girin:

**Title:** `feat: Kullanıcı login sayfası`

**Body:**
```markdown
## 📋 Açıklama
Kullanıcıların sisteme giriş yapabilmesi için login sayfası oluşturulmalı.

## ✅ Yapılacaklar
- [ ] Login form oluştur
- [ ] Validasyon ekle
- [ ] API entegrasyonu
- [ ] Hata mesajları

## 🎨 Mockup
[Varsa ekran tasarımı ekle]
```

4. Labels ekleyin: `enhancement`, `priority: high`
5. Assign: Kendinize atayın
6. **Submit new issue** tıklayın

### Adım 6: Daha Fazla Issue Ekleyin

Aşağıdaki issue'ları da oluşturun:

| # | Başlık | Label |
|:--|:-------|:------|
| 2 | `bug: Navbar mobilde görünmüyor` | `bug` |
| 3 | `docs: README güncellenmeli` | `documentation` |
| 4 | `feat: Dashboard sayfası` | `enhancement` |

---

## 📝 Bölüm 4: Projects (Kanban Board)

### Adım 7: Project Oluşturma

1. **Projects** sekmesine gidin
2. **New project** tıklayın
3. **Board** template seçin
4. Proje adı: `Sprint 1`
5. **Create project** tıklayın

### Adım 8: Sütunları Düzenleme

Varsayılan sütunlar:
- Todo
- In Progress
- Done

Ekstra sütun ekleyin:
- **Review** (In Progress ve Done arasına)

### Adım 9: Issue'ları Board'a Ekleyin

1. **Add item** veya **+** butonuna tıklayın
2. Oluşturduğunuz issue'ları ekleyin
3. Issue'ları sürükleyerek sütunlar arası taşıyın

### Adım 10: Otomasyon Kuralları

1. **...** menüsünden **Workflows** seçin
2. **Auto-add to project** aktifleştirin
3. **Auto-close completed** aktifleştirin

---

## 📝 Bölüm 5: Simülasyon

### Senaryo: Sprint Çalışması

1. **Issue #1'i "In Progress"e taşıyın**
2. **Branch oluşturun:**
   ```bash
   git checkout -b feature/login-page
   ```
3. **Değişiklik yapın ve commit edin:**
   ```bash
   echo "Login page placeholder" > login.html
   git add .
   git commit -m "feat: login sayfası eklendi

   Closes #1"
   ```
4. **Push ve PR açın**
5. **PR merge olunca Issue #1 otomatik kapanır**
6. **Board'da "Done"a taşınır**

---

## ✅ Kontrol Listesi

- [ ] Organization oluşturuldu
- [ ] Takım oluşturuldu ve üye eklendi
- [ ] En az 3 issue açıldı
- [ ] Project board oluşturuldu
- [ ] Issue'lar board'a eklendi
- [ ] Bir issue kapatıldı (commit ile)

---

## 📚 Öğrenilen Kavramlar

| Kavram | Açıklama |
|:-------|:---------|
| Organization | Birden fazla kişinin çalışabildiği kurumsal yapı |
| Teams | Organizasyon içinde yetki grupları |
| Issues | Görev, hata, özellik takibi |
| Labels | Issue kategorileri |
| Projects | Kanban tarzı proje yönetimi |
| Milestones | Sürüm hedefleri |

---

## ➡️ Sonraki Lab

**[Lab 5: GitHub Actions →](../lab-05-automation)**

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

</div>
