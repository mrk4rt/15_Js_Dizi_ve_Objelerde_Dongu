# JavaScript'te Dizi ve Nesne Döngüleri

Diziler ve nesneler üzerinde döngüler kullanmak, JavaScript'te veri yapıları içinde gezinmemizi sağlar. Hem dizilerde hem de nesnelerde farklı döngü yöntemleri kullanarak eleman veya özelliklere erişim sağlayabiliriz. İşte en sık kullanılan döngüler ve kullanımları:

## 1. Diziler Üzerinde Döngüler

Diziler, belirli bir sıralamada elemanları saklayan veri yapılarıdır. JavaScript’te dizilerde döngü kullanarak her bir elemana kolayca erişebilirsiniz.

### a. `for` Döngüsü

Bir dizinin her elemanına klasik bir `for` döngüsü ile erişebilirsiniz. Bu döngü, belirli bir başlangıç değerinden bir bitiş değerine kadar döner ve her adımda dizinin elemanlarına indeks numaraları ile erişir.

```javascript
let meyveler = ["Elma", "Armut", "Çilek"];
for (let i = 0; i < meyveler.length; i++) {
  console.log(meyveler[i]);
}
```

### b. `for...of` Döngüsü

for...of , diziler üzerinde gezinmek için daha kısa ve anlaşılır bir yöntemdir. Bu döngü, dizinin elemanlarını direkt olarak kullanmamızı sağlar.

```javascript
let meyveler = ["Elma", "Armut", "Çilek"];
for (let meyve of meyveler) {
  console.log(meyve);
}
```

### c. `forEach` Metodu

Dizilere özel forEach metodu, her eleman üzerinde bir işlem yapabilmemizi sağlar. Bu yöntem, genelde dizilerde işlem yapmak için en çok tercih edilen yöntemlerden biridir.

```javascript
let meyveler = ["Elma", "Armut", "Çilek"];
meyveler.forEach((meyve) => {
  console.log(meyve);
});
```



## 2. Nesneler (Objeler) Üzerinde Döngüler

JavaScript'te nesneler, anahtar-değer çiftlerinden oluşur ve belirli bir sıralamaya sahip değildirler. Nesneler üzerinde döngü yapmak için `for...in` döngüsü kullanılır.

### a. `for...in` Döngüsü

for...in, nesnenin tüm anahtarlarını döndürür. Bu sayede, her bir anahtar için nesnedeki değerine erişebilirsiniz.

```javascript
let ogrenci = {
  isim: "Ali",
  yas: 21,
  bolum: "Bilgisayar Mühendisliği"
};

for (let anahtar in ogrenci) {
  console.log(`${anahtar}: ${ogrenci[anahtar]}`);
}
```


## 3. Dizi ve Nesne Karışımı Yapılarda Döngüler

Bazen nesneler içinde diziler veya diziler içinde nesneler olabilir. Bu gibi durumlarda iç içe döngüler kullanarak her bir elemana veya özelliğe ulaşabilirsiniz.

```javascript
let sinif = [
  { isim: "Ali", yas: 21 },
  { isim: "Ayşe", yas: 22 },
  { isim: "Fatma", yas: 23 }
];


for (let ogrenci of sinif) {
  for (let ozellik in ogrenci) {
    console.log(`${ozellik}: ${ogrenci[ozellik]}`);
  }
}
```



# Özet

- **Diziler için**: `for`, `for...of`, `forEach`
- **Nesneler için**: `for...in`
- **Karışık yapılar için**: İç içe döngüler (diziler için `for...of`, nesneler için `for...in`)

Dizi ve nesne döngülerini birlikte kullanarak, JavaScript’te veri yönetimini daha etkin bir şekilde gerçekleştirebilirsiniz.

