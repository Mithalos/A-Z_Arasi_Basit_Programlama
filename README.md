# C# Okul Tekrarı

Kitabın Başından İtibaren Genel Tekrar

## Operatörler
~~~cs  
== : Eşit //x ve y değeri birbirine eşit mi diğer kontrol ifadesi (Sadece x , y)
!= : Eşit Değil
<= : Küçük Eşit
>= : Büyük Eşit 
&& : Veya //Birden fazla parametre için kullanılır.
|| : Ve //Birden fazla parametre için bütün koşulları sağlaması gereken durumlarda kullanılır.

/* Eşitlik */
int x = 9;
int y = 9;

if (x == y){
    //Çalışıcak Kodlar
}


/* Eşit Değilse */
int x = 8;
int y = 7;

if (x != y){
    //Çalışıcak Kodlar
}


/* <= */
int x = 1;
int y = 8;

if (x <= y){
    //Çalışıcak Kodlar
}


/* >= */
int x = 8;
int y = 1;

if (x >= y){
    //Çalışıcak Kodlar
}


/* && */

//Tasarımda 2 adet TextBox olduğunu varsayarak yapıyorum
String Parametre_1 = textBox1.Text;
String Parametre_2 = textBox2.Text;

string Sonuc = "Deneme";

if (Parametre_1 && Parametre_2 == Sonuc){ //Textleri'nin Değerlerinin herhangi birisi döngüyü tamamlıyorsa
    //Çalışıcak Kodlar
}


~~~ 
 
## If Döngüsü 
~~~cs  
//Sayısal değerde x ve y değeri oluşturuyoruz.
int x , y;
    x = 5; //x değeri 5'e Eşit
    y = 6; //y değeri 6'e Eşit

if (x >= y) { //Eğer x değeri büyük eşit ise ye'ye 
    MessageBox.Show("X Değeri Büyüktür"); //Ekrana "X Değeri Büyüktür" Yazdır
}
~~~  


## If Else Döngüsü 
~~~cs  
//Sayısal değerde x ve y değeri oluşturuyoruz.
int x , y;
    x = 5; //x değeri 5'e Eşit
    y = 6; //y değeri 6'e Eşit

if (x >= y) { //Eğer x değeri büyük eşit ise ye'ye 
    MessageBox.Show("X Değeri Büyüktür"); //Ekrana "X Değeri Büyüktür" Yazdır
}
else { //Eğer x değeri küçük eşit ise ye'ye 
    MessageBox.Show("X Değeri Küçüktür"); //Ekrana "X Değeri Büyüktür" Yazdır
}
~~~  

## Else if Döngüsü 
~~~cs  
//Sayısal değerde x ve y değeri oluşturuyoruz.
int x , y;
    x = 5; //x değeri 5'e Eşit
    y = 6; //y değeri 6'e Eşit

if (x >= y) { //Eğer x değeri büyük eşit ise ye'ye 
    MessageBox.Show("X Değeri Büyüktür"); //Ekrana "X Değeri Büyüktür" Yazdır
}
else if (x <= y) { //Eğer x değeri küçük eşit ise ye'ye 
    MessageBox.Show("X Değeri Küçüktür"); //Ekrana "X Değeri Büyüktür" Yazdır
}
~~~ 


## Swich Case Döngüsü 
~~~cs  

parametre (değer atanmalı , veri türü belinlenip)

switch (parametre) {
    case (1/deger/"değer"): //Birinci çıkıştan çıkarsa
        //Çalışıcak Kodlar
    break; //Birinci Çıkışı Durdur, sonrasında ise İkinci çıkış var ise ondan devam et.
}

int Gun = Convert.ToInt32(DateTime.Now.DayOfWeek);
    switch (Gun)
    {
    case 1:
        MessageBox.Show("Pazartesi");
    break;
    case 2:
        MessageBox.Show("Salı");
    break;
    case 3:
        MessageBox.Show("Çarşamba");
    break;
    case 4:
        MessageBox.Show("Perşembe");
    break;
    case 5:
        MessageBox.Show("Cuma");
    break;
    case 6:
        MessageBox.Show("Cumartesi");
    break;
    case 0:
        MessageBox.Show("Pazar");
    break;
    default:
        MessageBox.Show("Hata oluştu.");
    break;
    }

~~~  

## Operatörler 
~~~cs  
i++; //Arttırma
i--; //Azaltma
x = x*3; //X değerini x + 3 katı ile çarp
x = x/5; //X değerini x + 5'e böl

~~~ 


## For Döngüsü
~~~cs  
for (int i = 0; /* Döngü değişkeni başlangıç değeri */ i >= 10 /* Döngü şart ifadesi */; i++ /* Döngü değişkeni sayacı */)
{
    //Çalışıcak Kodlar
}

~~~ 



## While Döngüsü
~~~cs  
//While ile kontrol etmeden direkt çalıştırır.

int parametre = 1;
while(parametre <= değer){
    //Çalışıcak Kodlar
}

//Örnek
int Sayi = 1;
while (Sayi <= 10)
{
    listBox1.Items.Add(Sayi);
    Sayi++;
}

~~~ 
  


## Do While Döngüsü
~~~cs  
//Do ile kontrol ederek çalıştırır , sonrasında ise while ile kontrol eder.

int parametre = 1;
do{
    //Çalışıcak Kodlar
}
while(parametre <= değer);

//Örnek
int Sayi = 1;
do
{
    listBox1.Items.Add(Sayi);
    Sayi++;
} while (Sayi > 5);

~~~


## Döngüyü Kesme (Durdurma) & Döngüyü Devam Ettirme 
~~~cs  
int a = 0;
while (a<10){
    MessageBox.Show(“Döngü Çalışıyor.”);
    if (a == 9)
    {
        MessageBox.Show(“Döngü Durdu.”);
        break;
    }
    a++;
    if(a == 5){
        continue;
        a++;
    }
 }

~~~


## Try-Catch-Finally
~~~cs  
Try = Hata OLMADAN derlenip çalıştırılan kodlar.
Catch = (Exception <$Parametre>) İle çalışan sytax veya DeBug Fix'e girerek hata yazdıran method 
Finally = (Genellikle Kullanılmaz) Hata dahi olsa derlenmeye devam edicek olan kod bloğu 

Kullanımı;

try {

} catch (Exception Err) {
     MessageBox.Show("Hata Mesajı", "Hata İle Derlenen Kod" + Err , MessageBoxButtons.OK , MessageBoxIcon.Warning);
} finally {

}
~~~


## Yapıcı / Yıkıcı Methodlar
~~~cs  



~~~


## Class , Nesne Oluşturma
~~~cs  
class = Sınıf değişkeni , aktivate olarak çalışan bağımlı bir tür.

#Seçiciler 
private : Başka bir sınıfdan çağrılması esnasında erişim belirleyiciler ile tanımlanması gerekmekte
public : Heryerden çekilebilen erişim engeli olmayan sınıf
protected : Korumalı sınıf , seçici'dir. Kendi içersinde kendi parametresi ile oluşturulan sınıflardan veri aktarımı yapılabilir.
internal : Dahili sayfa içerisinde veri kullanımına izin verir harici sayfadan çekim sağlamaz.
protected interna : Kendi sınıfını başka bir sayfada türetse bile sadece Args[] açıldığı sayfada kullanılır.

#Void ?
Void değeri olmayan , değer döndürmeyen veri tipi demektir classlarda en fazla kullanılan referanstır.

private void Class_Name() {

}

Voidsiz sınıf lar ise değer döndürür.

private int Class_Name(int a; int b;){
    return a + b;
}
~~~
