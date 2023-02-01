Sınıf öznitelikleri ve yöntemleri, sınıf içinde tanımlanan değişkenler ve işlevlerdir. Ayrıca tamamen sınıf üyeleri olarak bilinirler.

Sınıf niteliklerinin ne olduğunu anlamak için aşağıdaki örneği inceleyin
```
#include <iostream>
using namespace std;

class Employee
{
    int eID;
    string eName;
    public:
};


int main()
{
    Employee Harry;
}
 ```

Çalışan adlı bir sınıf oluşturulur ve sınıf içinde eId ve eName olmak üzere iki üye tanımlanır. Bu iki üye değişkendir ve sınıf öznitelikleri olarak bilinirler. Şimdi main'de Harry adında bir nesne tanımlandı. Harry, nokta operatörünü kullanarak bu niteliklere erişebilir. Ama halka açıklanmadıkça Harry'nin erişimine açık değiller.

 
```
class Employee
{
public:
    int eID;
    string eName;
};


int main()
{
    Employee Harry;
    Harry.eID = 5;
    Harry.eName = "Harry";
    cout << "Employee having ID " << Harry.eID << " is " << Harry.eName << endl;
}
```
Çıktı
```
Employee having ID 5 is Harry
 ```

Sınıf yöntemleri, bir sınıfta tanımlanan veya bir sınıfa ait olan işlevlerden başka bir şey değildir. Bir sınıfa ait yöntemlere, özniteliklere eriştikleri gibi nesneleri tarafından erişilir. Fonksiyonlar bir sınıfa ait olacak şekilde iki şekilde tanımlanabilirler.

### Sınıf içinde tanımlama
Sınıflar içindeki işlevleri tanımlamayı gösteren bir örnek,
```
class Employee
{
public:
    int eID;
    string eName;

    void printName()
    {
        cout << eName << endl;
    }
};
```
 

### Sınıf dışında tanımlama
Bir fonksiyon sınıfın dışında tanımlanabilse de, içinde bildirilmesi gerekir. Daha sonra, işlevi dışarıda tanımlamak için kapsam çözümleme operatörünü (::) kullanabiliriz.

Sınıfların dışındaki işlevleri tanımlamayı gösteren bir örnek,
```
class Employee
{
public:
    int eID;
    string eName;

    void printName();
};


void Employee::printName()
{
    cout << eName << endl;
}
```
