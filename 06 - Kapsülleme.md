Kapsülleme, Nesne Yönelimli Programlamanın ilk ayağıdır. Veri niteliklerini ve yöntemlerini bir araya getirmek anlamına gelir. Amaç, hassas verileri kullanıcılardan gizli tutmaktır.

Kapsülleme, ihtiyaç duyulana kadar değiştirilemez hale gelmeleri için özniteliklerin her zaman özel yapılması gereken iyi bir uygulama olarak kabul edilir. Veriler sonuçta bunun bir sonucu olarak daha güvenlidir. Üyeler gizli hale getirildikten sonra, onlara erişme veya onları değiştirme yöntemleri bildirilmelidir. 

 
Kapsüllemenin nasıl gerçekleştirildiğine bir örnek
```
#include <iostream>
using namespace std;
 
class class_name
{
private:
    int a;
 
public:
    void setA(int num)
    {
        a = num;
    }
 
    int getA()
    {
        return a;
    }
};
 
int main()
{
    class_name obj;
    obj.setA(5);
    cout << obj.getA() << endl;
}
```
Çıktı:
```
5
```
