# (TR) Python ile Veri Yapıları Simülasyonları 

Bu repository, temel veri yapılarının (Bağlı Listeler, Yığınlar ve Kuyruklar) pratik uygulamalarını gösteren Python projeleri koleksiyonudur. Projeler, bir veri yapıları dersi ödevleri kapsamında geliştirilmiştir.

## Projeler

Bu repository'de üç ana proje bulunmaktadır:

### 1. Müzik Çalar Simülasyonu (Dairesel Çift Yönlü Bağlı Liste)

**Dosya:** `MusicPlayer_CircularDoublyLinkedList.ipynb`

Bu proje, bir müzik çaların şarkı listesi fonksiyonunu simüle eder.
* **Kullanılan Veri Yapısı:** Dairesel Çift Yönlü Bağlı Liste (Circular Doubly Linked List)
* **Özellikler:**
    * Listenin sonuna şarkı ekleme (`addSongToEnd`).
    * Listeden şarkı silme (`removeSong`).
    * Sonraki şarkıya geçme (`playNext`).
    * Önceki şarkıya geçme (`playPrevious`).
* **Neden Bu Yapı?** **Dairesel** yapı, listenin sonunda otomatik olarak başa dönmeyi (playlist tekrarı) sağlar. **Çift yönlü** olması ise hem ileri hem de geri gitmeyi (sonraki/önceki şarkı) $O(1)$ zaman karmaşıklığında mümkün kılar.

### 2. Yazdırma Kuyruğu Simülatörü (Kuyruk - FIFO)

**Dosya:** `PrintJob_Queue_Simulator.ipynb`

Bu proje, bir yazıcıya gelen yazdırma işlerini yöneten bir sistemin simülasyonudur.
* **Kullanılan Veri Yapısı:** Kuyruk (Queue) - (FIFO: First-In, First-Out / İlk Giren, İlk Çıkar)
* **Özellikler:**
    * Kuyruğa yeni bir yazdırma işi ekleme (`enqueuePrintJob`).
    * Sıradaki yazdırma işini işleme (kuyruktan çıkarma) (`processNextJob`).
    * Mevcut kuyruğu gösterme (`showQueue`).
* **Neden Bu Yapı?** Kuyruk yapısı, "ilk gelen ilk işlenir" mantığıyla çalıştığı için yazdırma, bilet sırası veya sunucu istekleri gibi görevlerin adil bir şekilde sırayla işlenmesi için idealdir.

### 3. Metin Düzenleyici "Geri Al" Simülasyonu (Yığın - LIFO)

**Dosya:** `TextEditor_Undo_Stack_Simulation.ipynb`

Bu proje, bir metin düzenleyicideki "geri al" (undo) özelliğinin basit bir simülasyonunu yapar.
* **Kullanılan Veri Yapısı:** Yığın (Stack) - (LIFO: Last-In, First-Out / Son Giren, İlk Çıkar)
* **Özellikler:**
    * Metin ekleme (Yığına itme) (`pushWord`).
    * Son eylemi geri alma (Yığından çekme) (`popWord`).
    * Mevcut metni gösterme (`showWords`).
* **Neden Bu Yapı?** Yığın yapısı, "son giren ilk çıkar" mantığıyla çalışır. Bu, tarayıcı geçmişi veya bir metin düzenleyicideki "geri al" işlemleri gibi en son yapılan eylemin ilk önce geri alınması gereken durumlar için mükemmeldir.


# (ENG) Python Data Structures Simulations

This repository is a collection of Python projects demonstrating the practical applications of fundamental data structures: Linked Lists, Stacks, and Queues. These projects were developed as part of a data structures course assignment.

## Projects Included

This repository contains three main projects:

### 1. Music Player Simulation (Circular Doubly Linked List)

**File:** `MusicPlayer_CircularDoublyLinkedList.ipynb`

This project simulates the playlist functionality of a music player.
* **Data Structure Used:** Circular Doubly Linked List
* **Features:**
    * Adding a song to the end of the list (`addSongToEnd`).
    * Removing a song from the list (`removeSong`).
    * Skipping to the next song (`playNext`).
    * Going back to the previous song (`playPrevious`).
* **Why This Structure?** The **circular** nature allows the playlist to loop back to the beginning automatically. The **doubly linked** nature makes both forward (`next`) and backward (`previous`) traversal highly efficient, with an $O(1)$ time complexity.

### 2. Print Job Simulator (Queue - FIFO)

**File:** `PrintJob_Queue_Simulator.ipynb`

This project simulates a system for managing print jobs sent to a printer.
* **Data Structure Used:** Queue (First-In, First-Out - FIFO)
* **Features:**
    * Adding a new print job to the queue (`enqueuePrintJob`).
    * Processing the next job in the queue (dequeue) (`processNextJob`).
    * Displaying the current print queue (`showQueue`).
* **Why This Structure?** A Queue is the ideal structure for this task because it follows the "first-come, first-served" principle. This ensures fairness in processing tasks, just like a real-world print queue or a ticket line.

### 3. Text Editor "Undo" Simulation (Stack - LIFO)

**File:** `TextEditor_Undo_Stack_Simulation.ipynb`

This project simulates the basic "undo" functionality of a text editor.
* **Data Structure Used:** Stack (Last-In, First-Out - LIFO)
* **Features:**
    * Adding text (pushing to the stack) (`pushWord`).
    * Undoing the last action (popping from the stack) (`popWord`).
    * Displaying the current text (`showWords`).
* **Why This Structure?** A Stack operates on a "last-in, first-out" basis. This is perfect for an undo feature, where the most recent action must be the first one to be reversed (e.g., browser history, call stack, or editor undo).
