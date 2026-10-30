# Zor görev 2: küçük bir parçalayıcı

Programı `zor.tr` dosyasına yaz. Yalnız verilen başvurudaki dili kullan; açıklama yazma, yalnız kod. Girdiler programın içinde sabittir. Çıktıyı tam olarak istenen biçimde `TR_print` ile yaz.

Eğitim metni: `"kedi masada kedi koltukta köpek bahçede kedi uyur"`. Sözcükler tek boşlukla ayrılır.

**1. Sözlük.**
- Parçalayıcıyı bir **yapı** olarak yaz. Yapının bir alanı sözlüktür: her sözcüğe bir tam sayı kimlik verir.
- Sözlüğü, eğitim metnini alan ayrı bir fonksiyon kurar. İlk görülen sözcük 1 alır, sonraki yeni sözcük 2, ve böyle sürer. 0 kimliği "bilinmeyen" içindir.
- `boyut <sayı>` yazdır: sözlükteki sözcük sayısı, bilinmeyen dahil.

**2. Sıklık.**
- Eğitim metnindeki her sözcüğün kaç kez geçtiğini say.
- En sık üç sözcüğü, her biri ayrı satırda `<sözcük> <sayı>` biçiminde yazdır.
- Sıralama sayıya göre büyükten küçüğe olur. Eşitlikte TR'nin metin karşılaştırmasıyla küçük olan önce gelir.

**3. Kodlama ve çözme.**
- Yapının iki metodu olsun:
  - **kodla:** bir metni sözcüklerine böler ve kimlik listesi verir. Sözlükte olmayan sözcük 0 olur.
  - **çöz:** bir kimlik listesini, sözcükleri tek boşlukla birleştirerek metne çevirir. Sözlükte olmayan kimlik `<?>` olur.
- `"köpek bahçede uyuyor kedi"` metnini kodla ve `kodla <k1> <k2> ...` yazdır: kimlikler tek boşlukla.
- `[6, 1, 9]` listesini çöz ve `çöz <metin>` yazdır.

**4. Dolgulu parti.**
- Üç cümleyi kodla: `"kedi uyur"`, `"köpek bahçede kedi uyur"`, `"masada"`.
- Her satırı en uzun satırın boyuna kadar sonuna 0 ekleyerek doldur.
- Her satırı, kimlikleri tek boşlukla ayırarak ayrı satırda yazdır.
- Son satıra `dolgu <oran>` yazdır: eklenen 0'ların bütün hücrelere oranı, 3 basamağa yuvarlanmış.
