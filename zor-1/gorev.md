# Zor görev: katman hattı ve eğitim olaylarının özeti

Programı tek bir kod bloğu olarak ver. Yalnız verilen başvurudaki dili kullan; açıklama yazma, yalnız kod. Girdiler programın içinde sabittir. Çıktıyı tam olarak istenen biçimde `TR_print` ile yaz.

**1. Katman hattı.**
- Bir arayüz tanımla: ondalık bir sayı alıp ondalık bir sayı veren tek bir metot.
- Bu arayüzü karşılayan üç yapı yaz:
  - **ölçek**: sayıyı bir katsayıyla çarpar;
  - **kaydırma**: sayıya bir değer ekler;
  - **kırpma**: sayıyı bir alt ve bir üst sınırın arasına sıkıştırır.
- Hattı, bu arayüz tipinde öğeleri olan tek bir liste olarak kur, sırayla:
  1. katsayısı 2 olan ölçek;
  2. değeri -1 olan kaydırma;
  3. sınırları 0 ve 5 olan kırpma.
- Girdiler: 0.25, 1.0, 2.5, 4.0. Her girdiyi hattın katmanlarından sırayla geçir.
- Dört sonucu tek satırda, aralarında birer boşlukla yazdır.

**2. Eğitim olayları.**
- Bir eğitimin olaylarını tek bir durumlu tiple yaz. Üç durum var:
  - **adım**: ondalık bir kayıp taşır;
  - **atlama**: hiçbir şey taşımaz;
  - **doğrulama**: tam sayı bir puan taşır.
- Olay listesi alan bir fonksiyon yaz. Fonksiyon olayları eşlemeyle işler ve üç değeri tek bir demet olarak döndürür:
  1. adımların ortalama kaybı (adım yoksa 0);
  2. atlama sayısı;
  3. en yüksek doğrulama puanı. Bu değer, doğrulama yoksa yokluk olan isteğe bağlı bir tam sayıdır.
- Her olay listesi için tek satır yazdır: `ortalama <ortalama> atlanan <sayı> en_iyi <puan>`. Puan yoksa `<puan>` yerine `yok` yaz.
- Sırayla üç liste:
  - adım 2.0, adım 1.5, atlama, doğrulama 70, adım 1.0, atlama, adım 0.5, doğrulama 82, doğrulama 78;
  - adım 3.0, atlama;
  - boş liste.
