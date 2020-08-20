Strateji tasarım deseni(Strategy Design Pattern)

Strateji tasarım deseni en sık kullanılan davranışsal tasarım desenlerinden biridir.
Bu desenin amacı, bir istemcinin(Client) aynı görevi yapabilmek için birden farklı algoritma veya prosedürler arasında seçim yapabilmesini sağlamaktır.
Strateji tasarım modeli, onu kullanan istemcilerden(Client) bağımsız olarak algoritmayı kolayca değiştirmesini ve yeni bir algoritma eklenmesini sağlar.

Strateji tasarım deseninin nasıl olduğunu kısaca anlatacak olursak; 
-Öncelikle bir Strategy interface'i yazılır ve burada uygulanacak(implement) sınıflarda kullanılacak ortak fonksiyonlar belirtilir. 
-Yapılacak işlem için olan farklı algoritmalar farklı sınıfların içine yazılır ve yazılan sınıflar Strategy interface'sine implement edilir.
-Oluşturulan Strategy interface'ini kullanmak için bir Context sınıfı yazılır. Yapılacak işlem için hangi algoritmanın kullanılacağı yazılan Context sınıfında belirtilir.
Context sınıfında kullanılacak algoritmanın sınıfı Strategy olarak tutulur ve gerekli işlemler(Business Logic) Context sınıfı içindeki algoritmayı çalıştıracak fonksiyonun içinde yapılır.
Istenildiği takdirde Context sınıfındaki Strategy değiştirilip farklı algoritmalar kullanılabilir.

Daha detaylı öğrenim için UML diagramının incelenmesi tavsiye edilir. 

Örnek amacıyla 4 işlem yapabilen ufak bir program Strateji tasarım deseni ile yazılmıştır. Oluşturulan 4 işlem dışında farklı bir işlem yapılması istenirse; yapılacak işlem için bir sınıf oluşturulması
ve Strategy sınıfına implement edilmesi yeterlidir. Daha sonra Context sınıfına yeni yazılan sınıf Strategy olarak verilip kullanılabilir.