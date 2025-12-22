# 📝 Markdown Söz Dizimi Cheat Sheet

<div align="center">

[![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)]()

*README ve dokümantasyon yazımı için Markdown referansı*

</div>

---

## 📌 Başlıklar

```markdown
# Başlık 1
## Başlık 2
### Başlık 3
#### Başlık 4
##### Başlık 5
###### Başlık 6
```

---

## ✏️ Metin Biçimlendirme

| Styl | Söz Dizimi | Sonuç |
|:-----|:-----------|:------|
| Kalın | `**kalın**` | **kalın** |
| İtalik | `*italik*` | *italik* |
| Kalın + İtalik | `***her ikisi***` | ***her ikisi*** |
| Üstü Çizili | `~~çizili~~` | ~~çizili~~ |
| Kod | `` `kod` `` | `kod` |

---

## 📋 Listeler

### Sırasız Liste

```markdown
- Öğe 1
- Öğe 2
  - Alt öğe a
  - Alt öğe b
- Öğe 3

* Alternatif
+ Alternatif
```

### Sıralı Liste

```markdown
1. İlk
2. İkinci
3. Üçüncü
   1. Alt madde
   2. Alt madde
```

### Görev Listesi

```markdown
- [x] Tamamlandı
- [ ] Yapılacak
- [ ] Beklemede
```

**Sonuç:**
- [x] Tamamlandı
- [ ] Yapılacak
- [ ] Beklemede

---

## 🔗 Linkler

```markdown
[Link Metni](https://example.com)

[Başlığa Link](#başlık-adı)

[Referans stili link][1]

[1]: https://example.com

<https://example.com>

<email@example.com>
```

---

## 🖼️ Resimler

```markdown
![Alt Metin](resim.png)

![Alt Metin](resim.png "İsteğe bağlı başlık")

[![Tıklanabilir Resim](resim.png)](https://link.com)
```

---

## 💻 Kod Blokları

### Satır İçi Kod

```markdown
Bu bir `inline code` örneğidir.
```

### Kod Bloğu

````markdown
```javascript
function merhaba() {
    console.log("Merhaba!");
}
```
````

### Desteklenen Diller

```
javascript, python, java, c, cpp, csharp, ruby, go, rust,
html, css, json, yaml, bash, sql, markdown, diff, ...
```

### Diff Bloğu

````markdown
```diff
- Silinen satır
+ Eklenen satır
  Değişmeyen satır
```
````

---

## 📊 Tablolar

```markdown
| Sol Hizalı | Ortalı | Sağ Hizalı |
|:-----------|:------:|-----------:|
| Veri       | Veri   | Veri       |
| Daha fazla | Daha   | Daha       |
```

**Sonuç:**

| Sol Hizalı | Ortalı | Sağ Hizalı |
|:-----------|:------:|-----------:|
| Veri       | Veri   | Veri       |
| Daha fazla | Daha   | Daha       |

---

## 💬 Alıntılar

```markdown
> Bu bir alıntıdır.
>
> Birden fazla paragraf olabilir.

> İç içe
>> Alıntı
>>> Yapılabilir
```

---

## 📢 GitHub Alerts (Uyarı Kutuları)

```markdown
> [!NOTE]
> Bu bir not kutusudur.

> [!TIP]
> Faydalı bir ipucu.

> [!IMPORTANT]
> Önemli bilgi.

> [!WARNING]
> Dikkat edilmesi gereken durum.

> [!CAUTION]
> Kritik uyarı.
```

---

## ➖ Yatay Çizgi

```markdown
---

***

___
```

---

## 😀 Emoji

```markdown
:smile: :rocket: :star: :bug: :sparkles:
:fire: :heart: :thumbsup: :warning: :memo:
```

**Sonuç:** 😄 🚀 ⭐ 🐛 ✨ 🔥 ❤️ 👍 ⚠️ 📝

---

## 🏷️ Badge'ler (Shields.io)

```markdown
![Static Badge](https://img.shields.io/badge/label-message-color)

[![GitHub Stars](https://img.shields.io/github/stars/user/repo)](link)

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
```

### Yaygın Badge Stilleri

- `flat`
- `flat-square`
- `plastic`
- `for-the-badge`
- `social`

---

## 📐 HTML Kullanımı

GitHub Markdown, bazı HTML tag'lerini destekler:

```html
<div align="center">
  Ortalanmış içerik
</div>

<details>
<summary>Tıklayınca açılır</summary>
Gizli içerik burada.
</details>

<kbd>Ctrl</kbd> + <kbd>C</kbd>

<sub>Alt simge</sub> ve <sup>Üst simge</sup>
```

---

## 📏 Özel GitHub Özellikleri

### Mention

```markdown
@kullaniciadi
@org/takim
```

### Issue/PR Referans

```markdown
#123
user/repo#123
```

### Commit Referans

```markdown
abc1234
user/repo@abc1234
```

### Dosya Referans

```markdown
[README](README.md)
[Satır 10](file.js#L10)
[Satır 10-20](file.js#L10-L20)
```

---

## 📋 README Şablonu

```markdown
# 🚀 Proje Adı

Kısa açıklama.

## 📌 Özellikler

- ✅ Özellik 1
- ✅ Özellik 2

## 🛠️ Kurulum

\`\`\`bash
npm install
npm start
\`\`\`

## 📖 Kullanım

\`\`\`javascript
import { fonksiyon } from 'paket';
\`\`\`

## 🤝 Katkıda Bulunma

PR'lar kabul edilir!

## 📄 Lisans

MIT
```

---

## 🔧 Kaçış Karakterleri

Özel karakterleri göstermek için `\` kullanın:

```markdown
\* yıldız
\# hashtag
\[ köşeli parantez
\` backtick
```

---

## 📚 Faydalı Kaynaklar

- [GitHub Markdown Guide](https://docs.github.com/en/get-started/writing-on-github)
- [Markdown Guide](https://www.markdownguide.org)
- [Dillinger (Online Editor)](https://dillinger.io)

---

<div align="center">

**[🏠 Ana Sayfa](../README.md)**

</div>
