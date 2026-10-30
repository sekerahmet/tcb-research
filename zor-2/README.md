# TR deneyi 2: belgeden programa, kendi denetiminle

TR, yapay zekâ ajanlarının yazması için tasarlanan yeni bir programlama dilidir. Bu deneyde dili yalnız tek sayfalık bir başvurudan öğrenip bir program yazıyorsun. Programı TR'nin kendi aracıyla denetleyip çalıştırıyorsun.

## Sana (yapay zekâya) talimat

1. Bu klasördeki [`basvuru.md`](basvuru.md) dosyasını baştan sona oku. Dilin kuralları ve kimlikleri yalnız oradadır.
2. [`gorev.md`](gorev.md) dosyasındaki programı TR'de yaz ve `zor.tr` adıyla kaydet.
3. Programı aşağıdaki araçla denetle ve çalıştır. Hata ya da uyarı varsa, ya da çıktı görevin istediği biçime uymuyorsa, **yalnız aracın iletisine ve çıktısına dayanarak** düzelt. En çok 3 düzeltme yapabilirsin.
4. Yanıtında şunları ver. Araç çıktılarını **ham hâliyle**, kendi sözlerinle özetlemeden kopyala:
   - `sha256sum tr` ve `./tr version` çıktısı;
   - her deneme için (`t0`, `t1`, ...) o denemenin programı, `check --json` çıktısının satırları, `run`'ın çıktısı ve çıkış kodu, neyi neden değiştirdiğin (bir cümle);
   - son programın tamamı, tek bir kod bloğunda;
   - okuduğun kaynakların listesi (dosya ya da adres).

Kurallar:
- Dilin kuralları için yalnız `basvuru.md`'yi ve aracın iletilerini kullan. Başka bir depoya, belgeye ya da web aramasına bakma.
- TR programını Python'a ya da başka bir dile çevirip çalıştırma; yalnız `tr` aracını kullan.
- Görevin cevabını başka bir yolla (Python, elle) hesaplayıp programın çıktısını ona göre ayarlama. Çıktının doğruluğuna yalnız programın kendi hesabı karar verir.
- Aracı çalıştıramadıysan "çalıştırdım" deme; ne olduğunu olduğu gibi yaz.

## Aracı edinme ve çalıştırma

Araç tek bir Linux ikilisidir (x86-64, ~12 MB). Kod çalıştırabildiğin bir Linux ortamında (sandbox, kod yorumlayıcısı):

```bash
curl -L -o tr https://github.com/sekerahmet/tcb-research/releases/download/zor-2/tr-linux-amd64
chmod +x tr
sha256sum tr   # 996117a78ea83705531264a3619ac8277f51438cd3046c7ef82203c0b43a68b4 olmalı
```

Ortamın internete çıkamıyorsa ikili sana dosya olarak yüklenmiş olabilir; o zaman yalnız `chmod +x` yap.

Denetleme ve çalıştırma:

```bash
TR_LANG=en ./tr check --json zor.tr   # çalıştırmadan denetler; her ileti bir JSON satırı
TR_LANG=en ./tr run zor.tr            # denetler ve çalıştırır
```

- Çıkış kodu 0 ise hata yoktur. Uyarılar da yazılır; onları da düzelt.
- `TR_LANG=en` iletileri İngilizce verir; program çıktısı dilden bağımsızdır.

Ortamında kod çalıştıramıyorsan bunu açıkça söyle; programı dikkatle, tek denemede yaz.
