# C++'da Nesnelere Bellek Ayırma
Her ikisi de aynı sınıftan olsalar bile, sınıfın değişkenlerine ve işlevlerine bellek tahsis edilme şekli farklıdır. Bellek, yalnızca nesne oluşturulduğunda sınıfın değişkenlerine tahsis edilir.

Sınıf bildirildiğinde bellek değişkenlere tahsis edilmez. Aynı zamanda, tek değişkenler farklı nesneler için farklı değerlere sahip olabilir, bu nedenle her nesne sınıfın tüm değişkenlerinin ayrı bir kopyasına sahiptir. Ancak bellek, sınıf bildirildiğinde işleve yalnızca bir kez tahsis edilir. Bu nedenle, nesnelerin işlevlerin ayrı ayrı kopyaları yoktur, her nesne arasında yalnızca bir kopya paylaşılır.

## C++'da Statik Veri Üyeleri
Statik bir veri üyesi oluşturulduğunda, sınıfın tüm nesneleri arasında paylaşılan veri üyesinin yalnızca tek bir kopyası vardır. Statik olarak belirtilmedikçe, genellikle her nesnenin özniteliklerin ayrı bir kopyası vardır.

Statik üyeler, sınıfın herhangi bir nesnesi tarafından tanımlanmaz. Kapsam çözümleme işleci kullanılarak herhangi bir işlevin dışında özel olarak tanımlanırlar.

Statik değişkenlerin nasıl tanımlandığına bir örnek
```
class Employee
{
 
public:
    static int count; //returns number of employees
    string eName;
 
    void setName(string name)
    {
        eName = name;
        count++;
    }
};

int Employee::count = 0; //defining the value of count
```

## C++'da Statik Yöntemler
Statik bir yöntem oluşturulduğunda, herhangi bir nesneden ve sınıftan bağımsız hale gelirler. Statik yöntemler yalnızca statik veri üyelerine ve statik yöntemlere erişebilir. Statik yöntemlere yalnızca kapsam çözümleme operatörü kullanılarak erişilebilir. Bir programda statik yöntemlerin nasıl kullanıldığına dair bir örnek gösterilmiştir.  
```
#include <iostream>
using namespace std;
 
class Employee
{
 
public:
    static int count; //static variable
    string eName;
 
    void setName(string name)
    {
        eName = name;
        count++;
    }
 
    static int getCount()//static method
    {
        return count;
    }
};
 
int Employee::count = 0; //defining the value of count
 
int main()
{
    Employee Harry;
    Harry.setName("Harry");
    cout << Employee::getCount() << endl;
}
```
Çıktı
```
1
```
