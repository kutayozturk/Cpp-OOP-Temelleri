## C++'da polimorfizm
Poli, birkaç anlamına gelir ve morfizm biçim anlamına gelir. Polimorfizm, birkaç formu olan bir şeydir veya bunu tek isim ve çoklu formlar olarak da söyleyebiliriz. İki tür polimorfizm vardır:
- Derleme zamanı polimorfizmi
- Çalışma zamanı polimorfizmi
 
## Derleme Zamanı Polimorfizmi
Derleme zamanı polimorfizminde hangi fonksiyonun çalışacağı zaten bilinmektedir. Derleme zamanı polimorfizmi ayrıca erken bağlama olarak da adlandırılır; bu, zaten işlev çağrısına bağlı olduğunuz ve bu işlevin çalışacağını bildiğiniz anlamına gelir.

İki tür derleme zamanı polimorfizmi vardır:

- İşlev Aşırı Yüklemesi
Bu, birden fazla fonksiyon oluşturmamızı sağlayan bir özelliktir ve fonksiyonların isimleri aynıdır ancak parametrelerinin farklı olması gerekir. Bir programda işlev aşırı yüklemesi uygulandığında ve işlev çağrıları yapıldığında, derleyici hangi işlevlerin yürütüleceğini bilir.

- Operatör Aşırı Yüklemesi

Bu, bazı belirli görevler için çalışan operatörleri tanımlamamızı sağlayan bir özelliktir. + operatörünü kullanarak iki diziyi birleştirerek toplayabilir ve aynı anda aritmetik olarak iki sayısal değer ekleyebiliriz. Bu, operatörün aşırı yüklenmesidir.

## Çalışma Zamanı Polimorfizmi
Çalışma zamanı polimorfizmi ile derleyicinin kod yürütüldüğünde ne olacağı hakkında hiçbir fikri yoktur. Çalışma zamanı polimorfizmi aynı zamanda geç bağlama olarak da adlandırılır. Çalışma zamanı polimorfizmi, işlev çağrılarına çalışma zamanında karar verildiği için yavaş kabul edilir. Çalışma zamanı polimorfizmi, sanal işlevlerden elde edilebilir.

## C++'da Sanal İşlevler
Bir sanal anahtar sözcük kullanılarak bildirilen temel sınıftaki bir üye işleve sanal işlev denir. Türetilmiş sınıfta yeniden tanımlanabilirler. Üst sınıfta bulunan ancak alt sınıfta yeniden tanımlanan bir işleve sanal işlev denir.

Bir fonksiyonun sanal olabilmesi için statik olmaması gerekir.
