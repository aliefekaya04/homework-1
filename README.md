# homework-1
C# ENTRY LEVEL QUESTİONS
// First homework of the course let's begin with the written questions and the codes.On this document you'll see ten question which can be written by loop functions(if-else if-else).
//   Q1 Program that prints the entered number on the screen by taking half of it if it is even, and twice if it is odd. ;


            Console.WriteLine("WELCOME");
            Console.Write("write any integer : ");
            int number = int.Parse(Console.ReadLine());
            if (number % 2 == 0)
            {
                Console.WriteLine("number is even ");
                Console.WriteLine("result = " + (number / 2));
            }
            else
            {
                Console.WriteLine("number is odd");
                Console.WriteLine("result = " + (number * 2));
            }
            Console.ReadKey();

// Q2 Create an example showing whether the entered number is odd or even.


            Console.WriteLine("WELCOME");
            Console.Write("write any integer : ");
            int number = int.Parse(Console.ReadLine());
            if (number % 2 == 0)
            {
                Console.WriteLine("number is even ");
            }
            else
            {
                Console.WriteLine("number is odd");
            }
            Console.ReadKey();

//Q3 Program that asks the user for 2 numbers and displays "Exactly Divisible" if the 1st number is divided by the 2nd number. Otherwise, it says "It is not fully divisible" and displays the remainder on the screen. 


            Console.Write("Bir Sayı Giriniz : ");
            int sayi = int.Parse(Console.ReadLine());
            Console.Write("İkinci sayiyi giriniz: ");
            int sayi2 = int.Parse(Console.ReadLine());
            int sonuc = (int)(sayi / sayi2);
            if (sayi % sayi2 == 0)
            {
                Console.WriteLine("girilen iki sayı birbirine tam bölünüyor " + sonuc);
            }
            else
            {
                Console.WriteLine("girilen sayılar birbirine tam bölünmüyor " + sonuc);
            }
              Console.ReadKey();

//Q4 Ask the user for 2 numbers (Long Side and Short Side for Rectangle). Then output a menu to the user (like below)



	Console.WriteLine("Dikdörtgenin kısa kenar uzunluğunu giriniz :");
	double kisa_kenar = double.Parse(Console.ReadLine());
	Console.WriteLine("Dikdörtgenin uzun kenar uzunluğunu giriniz : ");
	double uzun_kenar = double.Parse(Console.ReadLine());
	Console.WriteLine(" HOŞGELDİNİZ " + " \n " + "MENÜ");
	Console.WriteLine("1 - alan hesaplama ");
	Console.WriteLine("2 - çevre hesaplama ");
	Console.Write("yapmak istediğiniz işlemi seçiniz : ");
	int secim = Convert.ToInt32(Console.ReadLine());
	if (secim == 1)
	{
    		double alan = uzun_kenar * kisa_kenar;
    		Console.WriteLine("Oluştrduğunuz dikdörtgenin alanı = " + alan);
	}
	else if (secim == 2)
	{
    		double cevre = 2 *(uzun_kenar +  kisa_kenar);
    		Console.WriteLine("oluşturduğunuz dikdörtgenin çevresi = " + cevre);
	}
	else
	{
    Console.WriteLine("!!! geçersiz İŞLEM !!! ");
	}
		Console.ReadKey();



//Q5 Is the entered whole number divisible by 3 and 5? Write the program to find it.


Console.Write("Bir Sayı Giriniz : ");
int sayi = int.Parse(Console.ReadLine());
if (sayi % 3 == 0 && sayi % 5 == 0)
{
    Console.WriteLine("Girilen sayı 3 ve 5'in ortak katıdır");
} 
else if(sayi % 3 == 0 && sayi % 5 != 0)
{
    Console.WriteLine("girilen sayı 3'ün katıdır ancak 5'in Katı Değildir");
}
else if(sayi % 3 != 0 &&  sayi % 5 == 0)
{
    Console.WriteLine("girilen sayı 5'in katıdır ancak 3'ün katı değildir");
}
else
{
    Console.WriteLine("girilen sayı 3'e ve 5'e Bölünmüyor");
}         
Console.ReadKey();


//Q6 Write c# codes on the screen that show that those who are 18 years old and over can apply for the driving license exam, and if they are under 18, how many years will it take to get a driver's license.


            Console.WriteLine("lütfen yaşınızı giriniz: " );
            int yas = int.Parse( Console.ReadLine() );
            if (yas >= 18)
            {
                Console.WriteLine("Yaşınız ehliyet almak için yeterlidir,Başvurunuz işleme alınmıştır");
            }
            else if (yas < 18)
            {
                Console.WriteLine("yaşınız ehliyet almak için yetersizdir,başvurunuz reddedilmiştir");
                int sure = ( 18 - yas );
                Console.WriteLine("ehliyet başvuru için kalan süre = " + sure + "yıl");
                if ( sure == 18 )
                {
                    Console.WriteLine("kanka daha doğmamışsın ki :) ");
                }
            }
            else
            {
                Console.WriteLine("neyin peşindesin ?????? ");  

            }
		Console.Readkey();

//Q7 If a person purchases 100 TL or more from the store, he gets a 10% discount, if he buys 200 TL or more, he gets a 15% discount, if he makes a purchase of 300 TL or more, he gets a 20% discount, and write the C# code that displays the amount he will pay on the screen.


Console.WriteLine(" ABSOLUTE SHARPNESS OF C giyim mağazısına hoşgeldiniz");
Console.WriteLine(" yaptığınız total alışveriş miktarını giriniz");
int tutar = int.Parse(Console.ReadLine());
if (tutar >= 100 && tutar < 200)
{
    Console.WriteLine("kazandığnız indirim oranı %10, TEBRİKLER 1");
    double odeme = (tutar) * 9 / 10;
    Console.WriteLine("ödemeniz gereken miktar " + odeme);
}
else if (tutar >= 200 && tutar < 300)
{
    Console.WriteLine("kazandığnız indirim tutarı %15, TEBRİKLER");
    double odeme2 = (tutar) * 85 / 100;
    Console.WriteLine("ödemeniz gereken miktar " + odeme2);
}
else if (tutar >= 300)
{
    Console.WriteLine("kazandığınız indirim tutarı %20'dir");
    double odeme3 = (tutar) * 8 / 10;
    Console.WriteLine("ödemeniz gereken miktar " + odeme3);
}
else
{
    Console.WriteLine("indirim kazanamadınız ödemeniz gerek miktar " + tutar);
}

    Console.ReadKey();

//Q8 A program that prints the letter grade according to the student grade entered from the keyboard. Conditions (0-39 = F, 40-59 = E, 60-60 = D, 70-79 = C, 80-89 = B, 90,100 = A)


Console.WriteLine("lütfen aldığınız sayısal notu giriniz");
int not = int.Parse(Console.ReadLine());
if (not >= 0 && not < 40)
{
    Console.WriteLine("DERSTEN KALDINIZ ! ");
    Console.WriteLine("HARF NOTUNUZ F dersi tekrar almanız gerekli");
}
else if (not >= 40 && not <= 59)
{
    Console.WriteLine("dersten geçtiniz");
    Console.WriteLine("Harf Notunuz E");
}
else if (not > 59 && not <= 69)
{
    Console.WriteLine("dersten geçtiniz");
    Console.WriteLine("Harf Notunuz D ");
}
else if (not >69 && not <= 79)
{
    Console.WriteLine("dersten geçtiniz");
    Console.WriteLine("Harf Notunuz C ");
}
else if (not > 79 && not <= 89)
{
    Console.WriteLine("dersten geçtiniz");
    Console.WriteLine("Harf Notunuz B ");
}
else if (not > 89 && not <= 100)
{
    Console.WriteLine("dersten geçtiniz");
    Console.WriteLine("Harf Notunuz A ");
}
else
{
    Console.WriteLine("sınav girişi bulunamadı");
}
                                           
Console.ReadKey();

//Q9 The program that displays the amount to be paid according to the hour in a parking lot (0-3 hours 10₺, 4-6 hours 15₺, 7 hours and above 20₺


Console.WriteLine("otoparktta kaldığınız süreyi lütfen görveliye bildiriniz ");
 int saat = int.Parse(Console.ReadLine());
 int ucret;
 if (saat >= 0 && saat <= 3)
 {
     ucret = 10;
 }
 else if (saat >= 4 && saat <= 6)
 {
     ucret = 15;
 }
 else 
 {
     ucret = 20;
 }
 Console.WriteLine("OTOPARK İÇİN ÖDEMENİZ GEREKEN MİKTAR " + ucret + " TÜRK LİRASI ");
 Console.ReadKey();

//Q10 Monthly electricity bill will be calculated. Get from the user how many kWh he consumes. If the consumption is less than 150, kWh is calculated as 20 kuruş, if it is between 150 and 300, it is calculated as 30 kuruş, and if it is 300 and above, it is calculated as 50 kuruş. Calculate how much the person's bill will be based on their consumption and print it on the screen.


Console.WriteLine("HARCADIĞINIZ ELEKTRİK MİKTARINI kWh CİNSİNDEN BELİRTİNİZ");
int kWh = int.Parse(Console.ReadLine());     
if (kWh < 150) 
{
    double islem = (double)kWh * 0.20;
    Console.WriteLine("Bu ay kullandığınız elektrik miktatrı = " + " " + kWh + "\n" +
        "ödemeniz gereken tutar ise " + islem + " TÜRK LİRASI ");
}
else if (kWh >= 150 && kWh < 300 )
{
    double islem = (double)kWh * 0.30;
    Console.WriteLine("Bu ay kullandığınız elektrik miktatrı = " + " " + kWh + "\n" +
        "ödemeniz gereken tutar ise " + islem + " TÜRK LİRASI ");
}
else
{
    double islem = (double)kWh * 0.50;
    Console.WriteLine("Bu ay kullandığınız elektrik miktatrı = " + " " + kWh + "\n" +
        "ödemeniz gereken tutar ise " + islem + " TÜRK LİRASI ");
}
Console.ReadKey();

