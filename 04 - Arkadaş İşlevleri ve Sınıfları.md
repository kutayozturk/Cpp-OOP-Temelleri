Arkadaş fonksiyonları, sınıf içinde tanımlı olmasalar bile, sınıf üyelerinin özel verilerine erişme hakkına sahip olan fonksiyonlardır. Friend fonksiyonunun prototipinin yazılması gerekmektedir. 

Bir sınıf içinde bir arkadaş işlevi bildirmek, o işlevi sınıfın bir üyesi yapmaz.

## Arkadaş İşlevinin Özellikleri
- Sınıfın kapsamında değil, sınıfın bir üyesi olmadığı anlamına gelir.
- Sınıfın kapsamında olmadığı için o sınıfın nesnesinden çağrılamaz.
- İster genel ister özel erişim değiştiricisi altında olsun, sınıf içinde herhangi bir yerde bildirilebilir, herhangi bir fark yaratmaz
- Üyelere doğrudan adlarıyla erişemez, herhangi bir üyeye erişmek için (nesne_adı.üye_adı) gerekir.
 

Bir sınıf içinde bir arkadaş işlevi bildirmek için sözdizimi şöyledir:
```
class class_name
{
    friend return_type function_name(arguments);
};
 
return_type class_name::function_name(arguments)
{
    //body of the function
}
``` 

## C++ Arkadaş Sınıfları
Arkadaş sınıfları, tanımlandıkları sınıfın özel üyelerine erişim izni olan sınıflardır. Burada dikkat edilmesi gereken en önemli nokta, sınıf başka bir sınıfın arkadaşı olursa, o sınıfın tüm private üyelerine erişebilir.

Bir sınıf içinde bir arkadaş sınıfı bildirmek için sözdizimi şöyledir:
```
class class_name
{
    friend class friend_class_name;
};
```
