 ///////////////////////////////////////////////     String.prototype    /////////////////////////////////////////

 //String.prototype.split()

1. split() => berilgan matinni array ko'rinishida qaytaradi split ichida 2ta qiymat qabul qiladi 

     splitni oddiy holda ishlatganda matnni o'zini array qiymati sifatida qaytaradi

       let massage = "salom ishlar qaly";
       const splitMasage = massage.split();
       console.log(splitMasage)              //  NATIJA =>  [ 'salom ishlar qaly' ]

     agar split scop (qavslari)ichida qo'shtirnoq ochib qo'yilsa matindagi barcha so'zlardagi harflarni array qiymatlari sifatida  qaytaradi 

       let massage = "salom ishlar qaly";
       const splitMasage = massage.split("");
       console.log(splitMasage)  // NATIJA => [ 's', 'a', 'l', 'o', 'm', ' ', 'i', 's', 'h', 'l',  'a', 'r', ' ', 'q', 'a',  'l', 'y']

     agar split  scop (qavslari)ichida qo'shtirnoq ochib va bitta tab tashlansa berilgan matnni barcha so'zlarini array qimatlari sifatda qaytaradi

      let massage = "salom ishlar qaly";
      const splitMasage = massage.split(" ");
      console.log(splitMasage)  // NATIJA => [ 'salom', 'ishlar', 'qaly' ]

     split('',n) => n bu yerda istalgan son yani matnni array ko'rinishida qaytarganda arrayni nechta qiymati chiqishi kerakligini aniqlab array qaytaradi

       let massage = "salom ishlar qaly yaxshimisan";
       const splitMasage = massage.split(" ",2);
       console.log(splitMasage)  // NATIJA => [ 'salom', 'ishlar' ]

///////////////////////////////////////////////     Array.prototype    /////////////////////////////////////////

// Array.prototype.join()

1. join() => join array prototype hisoblanib vazifasi array qiymatlarini arraydan halos etib string ko'rinishida chiqarib beradi
     
       let arr = [1,2,3,4,5];
       const joinArr= arr.join();
       console.log(joinArr)  // NATIJA => 1,2,3,4,5
    
     arraydan join qilingan qiymatlar orasidagi vergullar shundayligicha string xolda bo'ladi uni olib tashlash  uchun join  scop (qavslari)ichida   qo'shtirnoq ochib qo'yish kifoya

       let arr = [1,2,3,4,5];
       const joinArr = arr.join('');
       console.log(joinArr)  // NATIJA => 12345

     arraydan join qilingan qiymatlar bir biridan ajralib turishi uchun  join  scop (qavslari)ichida  qoshtirnoq qo'yilib unga bitta tab tashlab qo'yiladi
      
       let arr = ["salom","ishlar", "qalay"];
       const joinArr = arr.join(' ');
       console.log(joinArr)  // NATIJA => salom ishlar qalay

     arraydan join qilingan qiymatlar orasida  bo'sh joylari orasida turli belgi ba harlar yoki so'zlar chiqishi uchun scop (qavslari)ichida  qoshtirnoq qo'yilib uning ichiga qiymatlar orasidagi   bo'sh joyda chiqishi kerak bo'lgan qiymatni kiritasiz
      
      1. let arr = ["salom","ishlar", "qalay"];
         const joinArr = arr.join(' - ');
         console.log(joinArr)  // NATIJA => salom - ishlar - qalay
        
      2. let arr = ["salom","ishlar", "qalay"];
         const joinArr = arr.join(' 0 ');
         console.log(joinArr)  // NATIJA => salom 0 ishlar 0 qalay

      3. let arr = ["salom","ishlar", "qalay"];
         const joinArr = arr.join(' men ');
         console.log(joinArr)  // NATIJA => salom men ishlar men qalay

     join  split() bilan ham ishlatiladi chunki split qaytaradigan qiymat array ko'rinishida bo'ladi uni yaxlit bitta arraylardan halos qildirib matn ko'rinishida natija olmoqchi bo'lsak fofdalanishimiz mumkin

       let massage = "salom ishlar qalay";
       const splitMasage = massage.split(' ');
       console.log(splitMasage)  // NATIJA => [ 'salom', 'ishlar', 'qalay' ]
       const joinArr = splitMasage.join(' ');
       console.log(joinArr);     // NATIJA => salom ishlar qalay


// Array.prototype.shift()

2. shift() =>  array qiymatlarida eng 1-sini olib tashlash uchun ishlatiladi
     
       const array1 = [1, 2, 3];
       const firstElement = array1.shift();
       console.log(array1); // NATIJA => [ 2, 3 ]

3. unshift() =>  array qiymatlarni eng boshidan qiymat qo'shish uchun ishlatiladi

       const array1 = [1, 2, 3];
       array1.unshift(4, 5)
       console.log(array1); // NATIJA => [ 4, 5, 1, 2, 3 ]       

3. pop() =>  array qiymatlarni eng oxirgi qiymatni olib tashlash uchun ishlatiladi
    
      const array1 = [1, 2, 3];
      array1.pop()
      console.log(array1); // NATIJA => [ 1, 2 ]

3. push() =>  array qiymatlarni eng oxiridan qiymat qo'shish uchun ishlatiladi

      const array1 = [1, 2, 3];
      array1.push(4)
      console.log(array1); // NATIJA => [ 1, 2, 3, 4 ]