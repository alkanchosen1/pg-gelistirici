## PostgreSQL Geliştirici Dökümantasyonu

### 1. Projeyi Düzenleme

1. Projeyi düzenlemek için öncelikle repository'nin **fork** edilmesi gerekmektedir.

2. Repository fork edildikten sonra istenilen kısımlar aşağıdaki kısımlara göre düzenlenir
   ve açıklayıcı bir commit mesajı ile **commit** yapılır.
   
3. Commit yapıldıktan sonra repository'e dönülür ve açıklayıcı bir mesaj ile **pull request** açılır.

4. Pull request açıldıktan sonra proje yöneticileri duruma göre değişikliği ekler veya geri çevirir.

### 2. Yeni Sayfa Ekleme
Dökümantasyonda bulunan sayfalar markdown formatında ```/pages/mydoc``` klasöründe bulunmaktadır. 
Yeni sayfa eklemek isteyen kullanıcılar öncelikle bu klasörde yeni bir markdown dosyası
oluşturmalıdır. Bu dosyanın isim formatı şu şekildedir:

```
dosya_ismi.md      Örnek:veri_tipleri.md
```

Markdown, okunması ve yazması kolay bir düz metin formatıdır. Bu markdown dosyaları
HTML'e dönüştürülerek web sayfasına konulmaktadır. Markdown hakkında daha fazla
bilgiye şu sayfada ulaşılabilir: [Mastering Markdown](https://guides.github.com/features/mastering-markdown/).

Markdown dosyası oluşturulup kaydedildikten sonra soldaki panele
eklenmesi gerekmektedir. Bunun için ```_data\sidebars\mydoc_sidebar.yml``` dosyasına
gidilir. Bu dosyanın özel bir formatı vardır ve bu formata uymak **zorunludur**. Eğer bir
indentation hatası bulunursa konsolda hata mesajı verilir ve web sitesi çalışmayı durdurur.
Her bir alt bölmeye geçildiğinde üsttekine göre bir boşluk bırakılır ve istenilen sayfa eklenir. Örnek:

```
  - title: Giriş
    output: web, pdf
    folderitems:

    - title: Support
      url: /mydoc_support.html
      output: web, pdf

    - title: Deneme
      url: /deneme.html
      output: web, pdf

  - title: Veri Tipleri
    output: web, pdf
    folderitems:

    - title: Sayısal Veri Tipleri
      url: /mydoc_sayisal_veri_tipleri.html
      output: web, pdf

    - title: Metinsel Veri Tipleri
      url: /mydoc_metinsel_veri_tipleri.html
      output: web, pdf
```

İstenilen sayfanın panelde gözükecek adı (title) belirlenir.

URL kısmına markdown dosyasının ismi (.md hariç) sonuna .html uzantısı, başına / eklenerek yazılır. Örnek:
```
veri_tipleri.md --> /veri_tipleri.html
```

Output kısmına ise web, pdf yazılır ve oluşturulan metin, dosyanın istenilen kısmına eklenir. Örnek:
```
- title: Veri Tipleri
  url: /veri_tipleri.html
  output: web, pdf
```

### 3. Sayfa Düzenleme

