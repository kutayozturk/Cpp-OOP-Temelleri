## Class'lar (Sınıflar)
Sınıflar ve yapılar biraz aynıdır ancak yine de bazı farklılıkları vardır. Örneğin, yapılarda veri saklayamayız, bu da her şeyin halka açık olduğu ve kolayca erişilebildiği anlamına gelir ki bu da yapının önemli bir dezavantajıdır çünkü veri güvenliğinin önemli olduğu yerlerde yapılar kullanılamaz. Yapıların bir diğer dezavantajı ise onlara fonksiyon ekleyemememizdir.

Sınıflar, kullanıcı tanımlı veri türleridir ve nesneleri oluşturmak için bir şablondur. Sınıflar, sınıf üyeleri olarak da adlandırılan değişkenler ve işlevlerden oluşur.

C++'da bir sınıf tanımlamak için class anahtar sözcüğünü kullanırız.

C++'da bir sınıfın sözdizimi şöyledir:

```
class class_name
{
    //body of the class
};
```
 

## Objects (Nesneler)
Nesneler bir sınıfın örnekleridir. Bir nesne yaratmak için, sadece sınıf adını ve ardından nesnenin adını belirtmemiz gerekir. Nesneler, sınıf tanımına bağlı olan sınıf niteliklerine ve yöntemlerine erişebilir. Nesneler tarafından kullanılmalarına izin vermek için izinlerinin daha iyi belirlenebilmesi için bu özniteliklerin ve yöntemlerin erişim değiştiricilerine yerleştirilmesi önerilir.

 

C++'da bir nesneyi tanımlamanın sözdizimi şöyledir:
```
class class_name
{
    //body of the class
};

int main()
{
    class_name object_name; //object
}
```
