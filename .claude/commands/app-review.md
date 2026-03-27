# App Review Oluşturucu

Bu proje, App Store ve Google Play'deki uygulamaları incelemek icin kullaniliyor. Yeni bir app review olusturmak icin asagidaki adimlari takip et.

## Kullanici'dan Bilgi Al

Kullanicidan asagidaki bilgileri iste (eger argumanlarda verilmediyse):

1. **App adi** (tam isim)
2. **App size** (mb cinsinden)
3. **App url** (store linki - birden fazla olabilir)
4. **Developer** (GitHub, LinkedIn veya Instagram linki)
5. **Platform** (iOS / Android / Flutter / Cross-platform)
6. **Screenshot URL** (GitHub asset linki veya baska bir image URL)
7. **Repository URL** (opsiyonel - sadece open source ise)

## Dosya Olusturma

### 1. Detail Dosyasi

`detail/{app-adi-kebab-case}.md` dosyasini asagidaki template ile olustur:

```markdown
# {App Adi}

<img height="400" alt="{App Adi} App" src="{screenshot_url}" />

- **App adi:** {Tam isim}
- **App size:** {boyut}mb
- **App url:** [{store_url}]
- **Developer:** [{developer_url}]
- **Platform:** {iOS / Android / Flutter / Cross-platform}

## Genel Gorus
- {Kullanicinin verdigi genel gorusler}

## Teknik Gorus
- {Kullanicinin verdigi teknik gorusler}
```

**Opsiyonel alanlar** (gerektiginde ekle):
- Birden fazla store linki varsa ayri satirlarda yaz:
  - `- **App url Google Play:** [{url}]`
  - `- **App url App Store:** [{url}]`
- Open source ise:
  - `- **Repository:** [{repo_url}]`
  - Basliga `[Open source]` etiketi ekle: `# {App Adi} [Open source]`

### 2. README Guncelleme

`README.md` dosyasindaki `## Uygulamalar` bolumunun altindaki listenin **sonuna** yeni satir ekle:

```markdown
- [{App Adi}](detail/{dosya-adi}.md)
```

## Kurallar

- Genel Gorus ve Teknik Gorus her zaman bullet list (`-`) formatinda olmali
- img tag her zaman `height="400"` olmali
- Dosya adi kebab-case olmali (ornek: `cartoon-weather.md`)
- Metadata alanlari her zaman ayni sirada olmali: App adi > App size > App url > Developer > Platform
- Eger kullanici goruslerini Turkce yazarsa Turkce kalsin, ceviri yapma
- Review icerigi kullanicinin kendi gorusleridir, icerik uretme veya degistirme

$ARGUMENTS
