Yapıcı, sınıfla aynı ada sahip özel bir üye işlevdir. Yapıcının bir dönüş türü yoktur. Yapıcılar, sınıflarının nesnelerini başlatmak için kullanılır. Yapıcılar, bir nesne oluşturulduğunda otomatik olarak çağrılır.
 
### C++'da Oluşturucuların Özellikleri
- Sınıfın genel bölümünde bir yapıcı bildirilmelidir.
- Nesne oluşturulduğunda otomatik olarak çağrılır.
- Değer döndüremezler ve dönüş türleri yoktur.
- Varsayılan bağımsız değişkenlere sahip olabilir.
 
Bir yapıcının nasıl kullanıldığına bir örnek,
```
#include <iostream>
using namespace std;
 
class Employee
{
 
public:
    static int count; //returns number of employees
    string eName;
 
    //Constructor
    Employee()
    {
        count++; //increases employee count every time an object is defined
    }
 
    void setName(string name)
    {
        eName = name;
    }
 
    static int getCount()
    {
        return count;
    }
};
 
int Employee::count = 0; //defining the value of count
 
int main()
{
    Employee Harry1;
    Employee Harry2;
    Employee Harry3;
    cout << Employee::getCount() << endl;
}
```
Çıktı:
```
3
```
### C++'da Parametreli ve Varsayılan Oluşturucular
Parametreli oluşturucular, bir veya daha fazla parametre alan oluşturuculardır. Varsayılan kurucular, parametre almayan kuruculardır. Bu, yukarıdaki örnekte yalnızca tanım sırasında çalışan adını ileterek yardımcı olabilirdi. Bu, setName işlevini kaldırmalıydı.

### C++'da Yapıcı Aşırı Yüklemesi
Yapıcı aşırı yükleme, işlev aşırı yüklemesine benzer bir kavramdır. Burada, bir sınıfın farklı parametrelere sahip birden çok yapıcısı olabilir. Bir örneğin tanımı sırasında, bağımsız değişkenlerin sayısı ve türüyle eşleşen yapıcı yürütülür.

Örneğin, bir program 0, 1 ve 2 argümanlı 3 kurucudan oluşuyorsa ve biz yapıcıya sadece bir argüman iletirsek, bir argüman alan kurucu otomatik olarak çalıştırılır. 

### C++'da Varsayılan Argümanlara Sahip Yapıcılar
Yapıcının varsayılan bağımsız değişkenleri, yapıcı bildiriminde sağlananlardır. Yapıcı çağrılırken değerler sağlanmazsa, kurucu otomatik olarak varsayılan argümanları kullanır. 
 
Varsayılan bağımsız değişkenlerin bildirilmesini gösteren bir örnek,
```
class Employee
{
 
public:
    Employee(int a, int b = 9);
};
```

### Yapıcıyı C++ ile Kopyala
Kopya oluşturucu, başka bir nesnenin kopyasını oluşturan bir tür oluşturucudur. Bir nesnenin başka bir nesneye benzemesini istiyorsak, bir kopya oluşturucu kullanabiliriz. Programda herhangi bir kopya oluşturucu yazılmamışsa, derleyici kendi kopya oluşturucusunu sağlayacaktır. 

Bir kopya oluşturucu bildirmek için sözdizimi şöyledir:
```
class class_name
{
    int a;
 
public:
    //copy constructor
    class_name(class_name &obj)
    {
        a = obj.a;
    }
};
```
