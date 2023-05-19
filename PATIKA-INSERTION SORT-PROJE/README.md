# Insertion Sort

<b>Soru 1:</b> [22,27,16,2,18,6] -> Insertion Sort

Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.

---

<b>Cevap 1:</b> Karşılaştırma işlemine dizinin ikinci elemanından başlanılır. " * " işareti olan elemanlar soldaki (yani kendinden bir önceki) elemanlarla tek tek karşılaştırılır. Soldakinden küçük ise yer değiştirirler. Bu işlem seçilen eleman soldaki sayıdan büyük olana kadar tekrar eder. Karşılaştırmanın sonunda dizi soldan sağa doğru küçükten büyüğe sıralanmış olur.


1. [22, 27*, 16, 2, 18, 6] -> Aynı kalır, sağdaki diğer elemanın karşılaştırma işlemine geçilir.
2. [22, 27, 16*, 2, 18, 6] -> [16, 22, 27, 2, 18, 6]
3. [22, 27, 16, 2*, 18, 6] -> [2, 16, 22, 27, 18, 6]
4. [2, 16, 22, 27, 18*, 6] -> [2, 16, 18, 22, 27, 6]
5. [2, 16, 18, 22, 27, 6*] -> [2, 6, 16, 18, 22, 27]




---
<b>Soru 2:</b> Big-O gösterimini yazınız.

---
<b>Cevap 2:</b> Eleman sayısı n olduğunda, her eleman için en fazla (n-1) karşılaştırma yapılır. Algoritmanın tüm elemanlarını bu şekilde işlemesi gerektiğinde, toplam karşılaştırma sayısı (n-1) + (n-2) + ... + 1 olur, bu da toplam (n * (n-1) / 2)'ye eşittir.

Big-O gösterimi için en yüksek dereceli terimi göstermemiz gerekiyor. Bu yüzden formülden (n^2) geldiği için gösterimi <b>O(n^2)</b> şeklinde olur. 

---
<b>Soru 3:</b> Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız.

1. Average case: Aradığımız sayının ortada olması
2. Worst case: Aradığımız sayının sonda olması
3. Best case: Aradığımız sayının dizinin en başında olması.

---
<b>Cevap 3:</b> Dizi sıralandıktan sonraki hali <b>[2, 6, 16, 18, 22, 27]</b> şeklindedir. " 18 " sayısı dizinin ortasındaki eleman olduğu için cevap " Average case (yani aradığmız sayının ortada olması) " olacaktır.

---
<b>Soru 4:</b> [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.

---
<b>Cevap 4:</b>

1. [7, 3, 5, 8, 2*, 9, 4, 15, 6] -> [2, 3, 5, 8, 7, 9, 4, 15, 6]
2. [2, 3*, 5, 8, 7, 9, 4, 15, 6] -> [2, 3, 5, 8, 7, 9, 4, 15, 6]
3. [2, 3, 5, 8, 7, 9, 4*, 15, 6] -> [2, 3, 4, 8, 7, 9, 5, 15, 6]
4. [2, 3, 4, 8, 7, 9, 5*, 15, 6] -> [2, 3, 4, 5, 7, 9, 8, 15, 6]

<b>Not:</b> Karşılaştırması yapılan elemana "*" işareti koydum. Dizide en küçük eleman bulunarak ilk elemanla yer değiştirir , ardından tekrar en küçük eleman bulunur ve bu sefer ilk elemana 1 ekler ve o eleman ile yer değiştirir (yani sürekli i + 1 olarak yer değiştirme yapar). Bu işlem dizi soldan sağa doğru küçükten büyüğe sıralanana kadar devam eder. 