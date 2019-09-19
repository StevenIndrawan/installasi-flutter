# installasi-flutter
<H3><b>(-)Installasi flutter tanpa menggunakan Android Studio</H3><b>

Pada umumnya cara menginstal flutter dengan step -step berikut :
1.	Download SDK Flutter
2.	Instalasi Android Studio
3.	Download plugin dart & flutter untuk VsCode atau Android Studio
4.	Buat Project dan Jalankan hello world

<H3><B>(-)Langkah mudah instalasi Flutter<B></H3>

•	Download SDK Flutter. Silahkan kunjungi halaman download disini, dan sesuaikan dengan sistem yang digunakan,.terdapat 3 sistem operasi Windows, macOS dan Linux.
![](https://i.ibb.co/dBcZ6sT/Untitled.png)
•	Selanjutnya silahkan download Command Line Tools Only di halaman ini, penampakan nya seperti berikut, silahkan download sesuai sistem operasi yang digunakan
![](https://i.ibb.co/vDp3QxY/Untitled1.png)

Kemudian ceklis   I have read and agree with the above terms and conditions tekan Download seperti gambar berikut :

![](https://i.ibb.co/nLfFpNj/Untitled3.png)
•	Ekstrak kedua file tersebut dan letakkan di C:\Android untuk windows dan untuk sistem operasi yang lainnya bisa menaruh di root dan buat folder Android. Maka hasilnya akan ada 2 folder yaitu folder flutter dan tools.

![](https://i.ibb.co/bKQMRQM/Untitled4.png)

•	Selanjutnya silahkan download OpenJDK di halaman ini, dan pilih yang berekstensi zip. sesuaikan dengan sistem operasi yang digunakan, saya menggunakan versi jdk8u222-b10
![](https://i.ibb.co/BqCGMdX/Untitled5.png)
 
 
•	setelah di download jangan lupa untuk mengekstrak ke folder Android yang sudah kita punya sebelumnya dan rename nama folder dari jdk8u222-b10 menjadi openjdk. totalnya sekarang kita punya 3 folder yaitu flutter, tools dan openjdk.
![](https://i.ibb.co/cc4n7sq/Untitled6.png) 

•	sampai sini kita harus menge-set Environment Variable dan Path, untuk windows silahkan buka command prompt dan ketikan command perbaris.

setx JAVA_HOME “C:\Android\openjdk”
setx ANDROID_HOME “C:\Android”
setx ANDROID_SDK_ROOT “C:\Android\tools”
setx path “%path%;”C:\Android\sdk;C:\Android\tools\bin;C:\Android\flutter\bin”

Untuk OS lainnya silahkan menyesuaikan.

•	Buka terminal (Command Prompt) di C:/Android/tools/bin lalu ketikan beberapa perintah berikut.

sdkmanager “system-images;android-28;default;x86_64”  (android-28 ubah menjadi android-Q)
sdkmanager “platform-tools”
sdkmanager “build-tools;28.0.3” 
sdkmanager “platforms;android-28”
untuk SDK sendiri, Flutter selalu memerlukan Android SDK yang terbaru. jadi silahkan update sdk dengan command :

sdkmanager —-update
Jangan lupa untuk menjalankan syntax accept licenses nya

flutter doctor --android-licenses


•	Selanjutnya install Visual Studio Code dan ekstension flutter serta dart nya

![](https://i.ibb.co/y5hsGJQ/Untitled7.png)
 
•	Dart
![](https://i.ibb.co/RP14SvX/Untitled8.png) 


•	Jika semuanya sudah selesai silahkan buka terminal (Command Prompt) di Android/flutter atau untuk pengguna windows bisa double klik di C:\Android\Flutter\flutter_console.bat dan jalankan perintah flutter doctor, maka hasilnya seperti gambar berikut.
![](https://i.ibb.co/QQYKwVR/Untitled9.png) 

•	Step terakhir adalah buat project di VsCode dengan klik F1 dan mengetikan Flutter: New Project setelah project selesai di load, klik F5 untuk mendeploy ke android device teman-teman. dan hasilnya seperti gambar dibawah ini
![](https://i.ibb.co/tMFWBFp/Untitled10.png) 
