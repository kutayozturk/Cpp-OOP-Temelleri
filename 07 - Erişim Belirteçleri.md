### C++'da Genel Erişim Belirteçleri
Genel erişim değiştiricisi altında bildirilen tüm değişkenler ve işlevler herkes tarafından kullanılabilir olacaktır. Hem sınıf içinden hem de sınıf dışından erişilebilirler. Nokta (.) operatörü, programda genel veri üyelerine doğrudan erişmek için kullanılır.

### C++'da Özel Erişim Belirteçleri
Özel erişim değiştiricisi altında bildirilen tüm değişkenler ve işlevler yalnızca sınıf içinde kullanılabilir. Sınıf dışında herhangi bir nesne veya işlev tarafından kullanılmasına izin verilmez.

### C++'da Korumalı Erişim Belirteçleri
Korumalı erişim değiştiricileri, özel erişim değiştiricilerine benzer, ancak korumalı erişim değiştiricilerine türetilmiş sınıfta erişilebilirken, özel erişim değiştiricilerine türetilmiş sınıfta erişilemez. 

**Aşağıda, erişim değiştiricilerin genel, özel ve korumalı türetildiğindeki davranışını gösteren bir tablo gösterilmektedir.**


|   | Genel Türetme  |  Özel Türetme | Korumalı Türetme | 
| -------- | ------------- | -------- |  -------- |
| Özel Üyeler | Miras alınmadı | Miras alınmadı | Miras alınmadı |
| Korumalı Üyeler | Korumalı | Özel | Korumalı |
| Kamu Üyeler | Paylaşımlı | Özel | Korumalı |


- Sınıf, genel modda miras alınmışsa, özel üyeleri alt sınıftan miras alınamaz.
- Sınıf genel modda miras alınırsa, korunan üyeleri korunur ve bunlara alt sınıftan erişilebilir.
- Sınıf, genel modda miras alınmışsa, genel üyeleri geneldir ve alt sınıfın içinden ve sınıfın dışından erişilebilir.
- Sınıf özel modda miras alınırsa, özel üyeleri alt sınıftan miras alınamaz.
- Sınıf özel modda miras alınırsa, korunan üyeleri özeldir ve alt sınıftan erişilemez.
- Sınıf özel modda miras alınmışsa, genel üyeleri özeldir ve alt sınıftan erişilemez.
- Sınıf korumalı modda miras alınırsa, özel üyeleri alt sınıftan miras alınamaz.
- Sınıf, korumalı modda miras alınırsa, korumalı üyeleri korunur ve bunlara alt sınıftan erişilebilir.
- Sınıf korumalı modda miras alınırsa, genel üyeleri korunur ve alt sınıftan erişilebilir.
