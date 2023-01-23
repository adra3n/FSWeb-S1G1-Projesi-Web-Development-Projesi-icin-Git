## Araştırma Soruları

Şimdi görevi gerçekleştirmek için hazırsınız. Şimdi biraz daha kullandığımız araçları anlama zamanı. Bu dokümanı güncelleyerek, aşağıdaki soruları cevaplayınız. Git'e biraz daha aşina olmaya başladığınızı göreceksiniz. 

Soruları cevaplamak için [GitHub docs](https://docs.github.com/en)'u kullanabilirsiniz. Docs, (ingilizce documentation'ın kısaltılmış halidir) bir programı veya dilin nasıl kullanılacağını anlatan dokümandır. Yazılım dünyasında sıkça kullanılır. Bir yazılımcı olarak zamanınızın büyük çoğunluğu da bu tarz dokümanları okumakla ve üzerinde çalışmakla geçer.

Eğer aradığınız soruların cevapları GitHub docs'ta yok ise Google'lama becerileriniz size yardımcı olacaktır :)

1. Git nedir?

Bir versiyon kontrol sistemidir. Projede yaşanacak hataları geçmişe dönerek daha rahat çözmemizi sağlar.

2. Git ile GitHub arasında ne fark var?

Git, yazılan bir projenin bir çok kişi ile aynı anda yapılabilmesini sağlayan ve bunu internet üzerinde tutmamızı sağlayan versiyon kontrol sistemine denir.
GitHub ise Git ile yönettiğimiz bu projelerimizi cloud üzerinde saklayabildiğimiz ve paylaşıma açabildiğimiz bir depolama servisidir.

3. Neden bir branch oluşturuyoruz? 

Projelerimiz için Git üzerinden bir repo oluşturduğumuzda yaptığımız değişiklikler varsayılan olarak "main branch" altına kaydolur. 
Branch özelliği projelerimizde yaptığımız değişiklikleri istersek bu "main branch" ten ayrı tutarak dallara ayırmamızı sağlar ve projemizin farklı versiyonlarını kayıt altında tutmamıza imkan verir.
Böylelikle proje üzerinde yapılan değişikler kontrol altında tutulur. Branchler her hangi bir hata durumunda sorunları rahat bir şekilde çözmemize imkan sağlar.

4. Pull Request'in amacı nedir?

Uzak sunucudaki değişiklikleri veya herhangi bir projeyi yerele repo olarak çekmek için kullanırız. 
Uzaktaki repoda değişikliğe uğramış dosyalar varsa bunları indirir ve yereldeki repo ile birleştirerek dosyalarımızı günceller.

5. Bir Branchten diğerine geçmek için kullanıdığımız KOMUT nedir? Örneğin ADINIZ-SOYADINIZ branch'inde çalıştığınızı hayal edin ve main branch'ine geçmek istiyorsunuz.

"git checkout" komutudur. "git checkout main" yazarak main-branch'e geçeriz.

6. `git fetch`, `git merge` ve `git pull` arasındaki farklıarı açıklayınız. Bu konutlar ne yapar açıklayınız.

"git fetch" uzak repodaki tüm değişiklikleri yerele çeker. Fakat çekilen değişiklikler remote branch’lar olarak depolanır, yerel olarak değil. Bu sayede yereldeki kodla merge etmeden önce gözden geçirme şansı verir.
"git merge" başka bir branch'deki değişiklikleri üzerinde çalıştığınız kendi branch'inize entegre etme işlemidir. 
"git pull" yapılan değişiklikleri gözden geçirmenize izin vermeden uzaktaki reponun tüm değişikliklerini yereldeki repoya getirip birleştirir.

 En temel haliyle "git pull" önce bir "git fetch" yapar, sonrasında ise "git merge" uygular. Yani iki komutun kombinasyonudur. "git fetch" ve "git merge" ikilisini daha kontrollü bir pull işlemi yapmak için kullanırız.
Detaylı şekilde karşılaştırırsak, "git fetch" başka bir sunucunun projesindeki her türlü içeriği veya veriyi yerel sisteminize indirmek için kullanılan bir komuttur. 
Sistemde zaten mevcut olan yerel kodların üzerine yazılmaz. Birleştirme yapmadığı için çakışma yaratmaz. "git fetch" ile birleştirme yapmadan önce dosyalarımızı kontrol etme imkanı sunar. Çakışma riskini azaltır.
Ama "git pull" tek seferde uzak depoda yapılan tüm değişiklikleri kaydeder ve bunları birleştirir, bu da çakışmalar yaratabilir. 
"git pull" aynı zamanda riskli bir komut olarak da adlandırılır, çünkü bilgi vermeden birleştirmek istemediğiniz değişiklikleri karıştıracaktır. 

7. Merge conflict nedir?

Merge conflict genellikle tek bir kod üzerinde aynı anda iki bilgisayar çalıştığında ortaya çıkar. Aynı kodun birden fazla kopyası merge edilmeye çalıştığında hangisinin mergeleneceğine dair karışık olur. Bu duruma denir.

8. Merge conflict'i nasıl çözeriz?

Genelde çakışan kodların üzerinden tek tek düzenleme yapılması gerekilir. Ve çakışan kodlardan merge yapılacak olanlara karar verilip buna göre hareket edilir.