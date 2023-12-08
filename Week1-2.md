## Veri Tipleri
2 adet veri tipi var. Primitive ve complex:

primitive: sstring, number boolean symbol null undefined.

complex: object functon ve array.
## Değişken tanımlama ifadeleri
3 adet değişken tanımlama ifadesi var. Var,let,const.

Var globale scope, let ve const function scopetur.

Var global scope olduğu için her yerden ulaşılabilir ama let ve const’ta tanımlandığı fonksiyon aralığının dışında erişilemez.

Var’da üst üste değişken tanımlayabiliyoruz.

Let ve var değiştirilebilirken, const değiştirilemez.
## Null undefined ve NaN
Undefined: Bir değişken tanımlanmış ancak değeri atanmadığını ifade eder. 

Null: Bir değişkenin bilinçli olarak boşaltıldığını veya atanmadığını ifade eder. Yani değişkenin değeri 
olmadığına ve özellikle boş olduğunu söyler.

NaN: "Not-a-Number"ın kısaltmasıdır ve JavaScript'te özel bir değerdir. Bu değer, matematiksel bir işlemin sonucunun sayısal bir değere dönüşmediği veya tanımlanamadığı durumları temsil eder. NaN, genellikle hatalı veya geçersiz sayısal işlemler sonucunda ortaya çıkar.

## Arrow Fonk- Normal fonk farkı
Temel farkları, arrow fonksiyonlarının daha kısa ve hızlı söz dizimi kullanmalarıdır. Aynı zamanda this 
bağlamını da farklı işlerler. Arrow fonksiyonları kendi ‘this’ bağlamını oluşturmaz ve genelde 
fonksiyounun dışındaki this’i miras alır.

## Switch-case ve if-else
Bir değeri kontrol etmek ve farklı caselere göre işlem yapmak için kullanılır.

İkisi arasındaki temel fark, if/else ifadesinin bir koşulu değerlendirmesi ve koşulun doğru olması 
durumunda bir kod bloğunu yürütmesi, switch ifadesinin ise bir ifadeyi değerlendirmesi ve eşleşen 
case ifadesiyle ilişkili kodu yürütmesidir.

## Do-while ve while
While, başlangıçta döngü koşulunu kontrol eder ve koşul doğruysa döngüye girer.

Do-while, önce döngünün içindeki işlemi yapar sonra koşulu kontrol eder.

## For-foreach 
For döngüsünde başlangıç ifadesş koşul ifadesi ve artış ifadesi belirtildiği için daha fazla kontrol ve 
esneklik sağlar. 

Foeach ise daha okunaklı ama daha az kontrol sağlar. Çünkü her ögeyi işler.

Yani daha komplex işlemler için for kullanılırız.

## Recursive fonksiyon
Kendini içerde tekrar çağıran fonksiyondur.

Eğer bir fonksiyonda belirli bir koşul sağlanıyorsa ve içerde tekrar aynı fonksiyon çağırılıyorsa bu recursive fonksiyondur.

## Constructor method
Bir classta obje üretirken objeye başlangıç değerlerini atamak için kullandığımız fonksiyondur.

## Inheritence
Bir üst sınıfın özelliklerini ve yöntemlerini alt sınıfa aktarmaktır.
## Get-Set
Bir sınıfın verilerine erişimi kontrol etmek ve yönetmek için kullanılır

Set:değeri değiştirmek için

Get: Bize görünen ksımını değiştirmek için kullanılır.
## Super fonk
Alt class oluştururken üst classtan değişkenleri miras almak için kullandığımız fonk.

## Obje-class farkı
Nesneler anahtar-değer şeklinde verileri tanımladığımız değişken oluşturmak için kullandığımız 
yapılardır. nesneler belli özellikleri ve fonksiyonları alırken, classlar nesneleri türeteceğimiz zaman 
kullandığımız yapılardır. Class, nesne oluşturmak için sadece başlangıç değerlerini verdiğimiz yapıdır 
ve classlarda 1den fazla obje oluşturabiliriz. Fakat bir objeden 1 den fazla obje oluşturamayız. 
Değişkenleri keylerini her seferinde tanımlamamız gerekir.

## Senkron- asenkron
Senkron- işlerin sırasıyla yapıldığı ve işlerin her birinin birbirini beklediği durum.

Asenkron – yine işler sırasıyla yapılıyor ama işler birbirini beklemez.(JS ‘de asenkron yapıdadır)
## Callback
Bir işlem tamamlandığında başka bir işlemi başlatmak veya işlem sonuçlarını işlemek amacıyla 
callback fonksiyonları kullanılır.

Ama çok fazla işlem olduğu zaman bazı problemler ortaya çıkabilir.

-işlemin beklenilenden erken çağırılması

-hiç çağırılmaması

-hata kontrol durumunun problemli olması

-parametreyi bazen doğru alamaması

## Callback hell
Kodun iç içe geçmiş ve aşırı derecede karmaşık bir şekilde kullanıldığı bir durumu ifade eder.

## Promise
Bir işlemin sonucunu temsil eder. Resolve ve reject adında 2 adet parametre alır. Olumlu durumlarda 
resolve ile belirtilen işlemleri, olumsuz durumlarda ise reject ile belirtilen işlemlerin yapılacağına dair 
güvence (söz) verir.
## PromiseAll
Birden fazla promise varsa ve herbirnin düzgün şekilde çalıştığına emin olmak istiyorsak kullanırız.
ve then ve catch bloğuna yönlendirmemizi sağlar.
## Allsettled
Yine birden fazla promise olduğunda kullanılır. Ancak hem düzgün çalışanı hem de hatalı olanın 
sonucunu gösterir.
## Finally
Başarılı veya başarısız olsa bile çalıştırılması gereken kodu belirtir. Yani her koşulda çalışır.
##Async- await
Asenkron işlemleri senkron şekilde yönetmek için kullanılır.
## Access Modifiers
Public: Herhangi bir kod parçasından (sınıf dışından veya başka sınıflardan) erişime izin verir.

Private: Sadece ilgili sınıf içinden erişime izin verir. Diğer kod parçaları bu özelliği veya metodu doğrudan 
kullanamazlar.

Protected: Sınıf içi ve sınıftan türetilmiş (alt) sınıflardan erişime izin verir. Bu, kalıtım (inheritance) ile ilgilidir ve 
alt sınıfların üst sınıfın özelliklerine veya metotlarına erişmesini sağlar.

Internal(package-private): Sadece aynı paket veya modül içindeki kod parçalarından erişime izin verir.
## Private Variables
Private variable" (özel değişken), bir programın belirli bir kapsam içinde sadece belirli bir kod parçası 
tarafından erişilebilen değişkenlerdir. Diğer kısımlardan bu değişkenlere doğrudan erişim sağlanamaz 
ve bu değişkenlerin değeri veya durumu yalnızca belirli yöntemler veya işlevler aracılığıyla erişilebilir 
veya değiştirilebilir. Bu, değişkenlerin istenmeyen yan etkilerden korunmasına ve kodun daha güvenli 
ve sürdürülebilir hale gelmesine yardımcı olur.
## Prototip mantığı
Nesneler arasındaki ilişkiyi ve kalıtımı (inheritance) sağlayan temel bir özelliktir. Prototipler, nesnelerin 
metotları ve özellikleri paylaşmasını mümkün kılar. Bir nesnenin prototipi, o nesnenin metotlarını ve 
özelliklerini içerebilir.
## Array Methodları
### Eleman ekle-çıkar
Push-sona ekler
```javascript
var sports = ['basketball', 'football', 'tennis' ];
console.log(sports); // basketball, football, tennis
sports.push('baseball');
console.log(sports); // basketball, football, tennis, baseball
```
Unshift-başa ekler
```javascript
var sports = ['basketball', 'football', 'tennis' ];
console.log(sports); // basketball, football, tennis
sports.unshift('baseball');
console.log(sports); // baseball, basketball, football, tennis
```
Pop-sondan siler
```javascript
var sports = ['basketball', 'football', 'tennis' ];
console.log(sports); // basketball, football, tennis
sports.pop();
console.log(sports); // basketball, football
```
Shift-baştan siler.
```javascript
var sports = ['basketball', 'football', 'tennis' ];
console.log(sports);  // basketball, football, tennis
sports.shift();
console.log(sports);  // football, tennis
```

Splice-Belirli bir konuma eleman ekle,çıkar, değiştir.
```javascript
var sports = ['basketball', 'football', 'tennis' ];
console.log(sports); // basketball, football, tennis
sports.splice(1,0,'baseball');
console.log(sports); // basketball, baseball, football, tennis
```
Slice-Belirli bir aralığı kopyalar.
```javascript
var sports = ['basketball', 'football', 'tennis'];
var slicedSports = sports.slice(1, 3);
console.log(slicedSports); //football, tennis
```
Spread operatör – Dizi veya nesnenin elemanlarını başka bir dizi veya nesneye ekler.
### Birleştirme
Concat- 2 veya daha fazla diziyi birleştirir.

Join- dizi elemanlarını birleştirerek belirli ayraç kullanılır.

Flat – alt dizi elemanlarını birleştirir.
### Eleman bulma
Indexof- elemanın konumu bulur. Bulamazsa -1 döner. – ise sondan başlar.

LastIndexOf – Elemanın dizide geçtiği son konumunu bulur. Belirtilen eleman yoksa -1 döner.

Find – Koşulu sağlayan ilk elemanı döndürür. Koşulu sağlayan herhangi bir eleman yoksa undefined 
döner.

Include – dizinin belirli bir elemanı içerip içermedğini kontrol eder.

Destructing – Nesne veya dizinin belirli elemanlarına ulaşır. İndex – verilmişse sondan başlar.
### Array oluşturma-dönüştürme
Map – Her elemanı işler, yeni değerlerden yeni bir array oluşturur

Filter – Koşulu sağlayan elemanlardan yeni array oluşturur.

Of – türü farketmeksizin iletilen değerleri içeren bir dizi oluşturur.

From – dizi benzeri nesneyi diziye dönüştürür.

Flatmap – Her elemanı işleyerek yeni bir dizi oluşturur.
### İşleme ve sorgulama
Reduce – Belirtilen işlemi gerçekleştirerek tek bir değer döndürür.

Every – Tüm elemanların koşulu karşılayıp karşılamadığına bakar.

Some – En az 1 elemanın koşulu sağlayıp sağlamadığına bakar.

Sort-Elemanları sıralar.

Foreach- tüm elemanları işler.

## Obje metodları
### obje oluşturma
const car ={} 

const car = new .Object()

const car = object.create

const car= model:’punto’, year:’2018…} JSON.parse() ile oluşturma

const {name, age} = {name: ‘John’, age:30};//Destructing ile oluşturma

const users = {name,age}

function createUser(name, age) { //fonksiyon ile oluşturma
Return{name, age};
}

### eleman silmek
delete.obj.element

### elemana ulaşmak
this
### arraya dönüştürme
keyleri arrraya dönüştürme: const keys = object.keys(0:obje)

Valueları arraya dönüştürme: object.values

Objeti arraye döüştürme: let objcont =object.entries(obje)
### Obje kopyalama
Assign, spread operatör
### Değişiklik
Freeze: tamamen dondurur. Değişiklik veya parametre ekleme yapılamaz.

Seal: parametre eklenemez sadece var olan parametreler üzerinde değişiklikl yapılabilir.

Getprototype
