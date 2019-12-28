1. Kristian Sentosa (173210001)
2. Deni Herdiana (173210002)
3. Marfiana Ayu Irawati(173210004)
4. Risa Kurniawati (173210008)

# Functional Programming

Pemrograman Fungsional adalah paradigma pemrograman populer yang terkait erat dengan dasar matematika sains komputer. Meskipun tidak ada definisi ketat tentang apa yang merupakan bahasa fungsional, kami menganggapnya sebagai bahasa yang menggunakan fungsi untuk mengubah data. 
Bahasa fungsional adalah bahasa deklaratif , mereka memberi tahu komputer hasil apa yang mereka inginkan. Ini biasanya kontras dengan bahasa imperatif yang memberi tahu komputer langkah apa yang harus diambil untuk menyelesaikan masalah. Python biasanya dikodekan dengan cara imperatif tetapi dapat menggunakan gaya deklaratif jika perlu.
-	Fungsi Murni - tidak memiliki efek samping, yaitu, mereka tidak mengubah keadaan program. Dengan input yang sama, fungsi murni akan selalu menghasilkan output yang sama.
Contohnya
```python
A = 5
def impure_sum(b):
    return b + A
def pure_sum(a, b):
    return a + b

print(impure_sum(6))
10
print(pure_sum(4, 6))
11
```
-	Kekekalan - data tidak dapat diubah setelah dibuat. immutable adalah obyek yang tidak dapat diubah setelah itu dibuat. Sebaliknya  mutable  memungkinkan perubahan kondisinya yang tidak dapat diubah umumnya diinginkan dalam pemrograman fungsional.
Contoh 1
```python
a = [1, 2, 4, 8, 16] 
a[0] = 32
a

# [32, 2, 4, 8, 16]
#dapat merubah isi dari var a
```
Contoh 2
```python
a = (1, 2, 4, 8, 16) 
a [0] = 32 
# Salah! Anda tidak dapat memodifikasi tuple. 
Traceback (most recent call last):
File “”, line 1, in 
TypeError: ‘tuple’ object does not support item assignment
```
-	Fungsi Orde Tinggi - fungsi dapat menerima fungsi lain sebagai parameter dan fungsi dapat mengembalikan fungsi baru sebagai output. Ini memungkinkan kami untuk mengabstraksi tindakan, memberi kami fleksibilitas dalam perilaku kode kami.
fungsi yang mencetak garis beberapa kali:
```python
>>> def write_repeat(message, n):
...     for i in range(n):
...         print(message)
...
>>> write_repeat('Hello', 5)
Hello
Hello
Hello
Hello
Hello

#membuat fungsi yang menambah angka dalam daftar dengan 2, 5, dan 10. 
>>> def add2(numbers):
...     new_numbers = []
...     for n in numbers:
...         new_numbers.append(n + 2)
...     return new_numbers
...
>>> print(add2([23, 88])) 
[25, 90]
```
-	Fungsi  Lambda - juga dikenal sebagai "fungsi anonim" - memungkinkan kita untuk membuat dan menggunakan fungsi dalam satu baris. Mereka berguna ketika kita membutuhkan fungsi pendek yang hanya akan digunakan sekali. Mereka sebagian besar digunakan bersama dengan peta, filter dan metode pengurutan, yang akan kita lihat nanti dalam artikel.
Contoh 
```python
menghitung nilai 5x + 2. 

 >>> def f(x):
...     return 5*x+2
...
>>> f(3)
17
>>>
```
ungkapan dengan lambda “a”. Sekarang, kita bisa menggunakan ini seperti fungsi lainnya.
```python
>>> a = lambda x : 5*x+2
>>> a(3)
17
>>>
```


