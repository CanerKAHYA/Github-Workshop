# 🧪 Lab 5: GitHub Actions ile Otomasyon

<div align="center">

[![Difficulty](https://img.shields.io/badge/Zorluk-İleri-red?style=for-the-badge)]()
[![Duration](https://img.shields.io/badge/Süre-45_dk-blue?style=for-the-badge)]()

*CI/CD pipeline oluşturup otomatik test ve deploy yapın*

</div>

---

## 🎯 Öğrenme Hedefleri

- [x] GitHub Actions temel kavramlarını öğreneceksiniz
- [x] Basit bir CI workflow oluşturabileceksiniz
- [x] Workflow'ları tetikleyip sonuçları görebileceksiniz

---

## 📝 Bölüm 1: İlk Workflow

### Adım 1: Klasör Yapısı

Repo'nuzda şu yapıyı oluşturun:

```bash
mkdir -p .github/workflows
```

### Adım 2: Hello World Workflow

`.github/workflows/hello.yml` dosyası oluşturun:

```yaml
name: Hello World

on:
  push:
    branches: [main]
  workflow_dispatch:  # Manuel tetikleme

jobs:
  greet:
    runs-on: ubuntu-latest
    
    steps:
      - name: 👋 Say Hello
        run: echo "Merhaba GitHub Actions!"
      
      - name: 📅 Show Date
        run: date
      
      - name: 💻 System Info
        run: |
          echo "OS: $(uname -s)"
          echo "User: $(whoami)"
          echo "Directory: $(pwd)"
```

### Adım 3: Push ve İzle

```bash
git add .github/
git commit -m "ci: ilk GitHub Actions workflow eklendi"
git push
```

**Actions sekmesinde workflow'un çalıştığını görün!**

---

## 📝 Bölüm 2: CI Workflow

### Adım 4: Node.js Projesi Oluşturma

```bash
# package.json oluşturun
npm init -y

# Test script ekleyin
cat > test.js << 'EOF'
console.log("Test başladı...");

function topla(a, b) {
  return a + b;
}

// Basit test
if (topla(2, 3) === 5) {
  console.log("✅ Test geçti!");
  process.exit(0);
} else {
  console.log("❌ Test başarısız!");
  process.exit(1);
}
EOF
```

package.json'a test script ekleyin:

```json
{
  "scripts": {
    "test": "node test.js"
  }
}
```

### Adım 5: CI Workflow

`.github/workflows/ci.yml` oluşturun:

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    
    steps:
      - name: 📥 Checkout code
        uses: actions/checkout@v4
      
      - name: 📦 Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'
      
      - name: 📦 Install dependencies
        run: npm install
      
      - name: 🧪 Run tests
        run: npm test
```

### Adım 6: Push ve Kontrol

```bash
git add .
git commit -m "ci: Node.js CI workflow eklendi"
git push
```

---

## 📝 Bölüm 3: PR Workflow

### Adım 7: Pull Request Kontrolü

Yeni branch oluşturup PR açın:

```bash
git checkout -b feature/new-test

# test.js'e yeni test ekleyin
cat >> test.js << 'EOF'

// Yeni test
function carp(a, b) {
  return a * b;
}

if (carp(3, 4) === 12) {
  console.log("✅ Çarpma testi geçti!");
} else {
  console.log("❌ Çarpma testi başarısız!");
  process.exit(1);
}
EOF

git add .
git commit -m "test: çarpma testi eklendi"
git push -u origin feature/new-test
```

**GitHub'da PR açın ve CI'ın otomatik çalıştığını görün!**

---

## 📝 Bölüm 4: Status Badge

### Adım 8: README'ye Badge Ekleme

README.md'ye ekleyin:

```markdown
![CI](https://github.com/KULLANICI/REPO/actions/workflows/ci.yml/badge.svg)
```

---

## 📝 Bonus: Scheduled Workflow

Her gün çalışan workflow:

```yaml
name: Daily Check

on:
  schedule:
    - cron: '0 9 * * *'  # Her gün saat 09:00 UTC

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - run: echo "Günlük kontrol tamamlandı!"
```

---

## ✅ Kontrol Listesi

- [ ] Hello World workflow oluşturuldu
- [ ] CI workflow oluşturuldu
- [ ] Push ile workflow tetiklendi
- [ ] PR ile workflow çalıştırıldı
- [ ] Status badge eklendi

---

## 📊 Workflow Yapısı

```yaml
name: Workflow Adı        # İsim

on:                       # Tetikleyiciler
  push:
  pull_request:
  schedule:
  workflow_dispatch:

jobs:                     # İşler
  job-name:
    runs-on: ubuntu-latest
    steps:                # Adımlar
      - name: Adım adı
        uses: action/name@v1  # Hazır action
        with:
          param: value
      - name: Başka adım
        run: komut          # Shell komutu
```

---

## ➡️ Sonraki Lab

**[Lab 6: Portfolyo Oluşturma →](../lab-06-portfolio)**

---

<div align="center">

**[🏠 Ana Sayfa](../../README.md)** · **[📚 Tüm Lab'lar](../)**

</div>
