<h1 align="center">Instalasi Frida dan Testing Debugger untuk Android</h1>

1. Install python 3.7 dan pip terbaru.
2. Buka *command prompt* dan jalankan ***$ pip install frida-tools***.
3. Jalankan perintah ***$ frida --version*** untuk melihat apakah frida sudah benar ter-*install*.

<h3 align="left">Di Android</h3>

1. Gunakan perintah ***$ adb shell***. 
2. Gunakan perintah ***$ getprop | grep abi*** untuk melihat processor device (Emulator or Physical Device).

<h3 align="left">Di Laptop</h3>

1. Download frida server, sebelum download frida server pastikan untuk tahu Arsitektur Laptop (x86 untuk 32 bit atau x86_64 untuk 64 bit), download frida server dari <a href="https://github.com/frida/frida/releases">*link frida server*.</a>
2. Ekstrak file frida server (di contoh ini menggunakan **$ frida-server-16.1.4-android-x86_64**), dan pindah ke direktori tersebut menggunakan *command prompt*.
3. Push frida server kedalam device android menggunakan perintah ***$ adb push frida-server-16.1.4-android-x86_64 /data/local/tmp/frida-server-16.1.4-android-x86_64***.
4. Lakukan perintah ***$ adb shell***
5. Selanjutnya ketikan perintah ***$ su root***.
6. Setelah itu, pindah ke direktori menggunakan perintah ***$ cd /data/local/tmp***.
7. Selanjutnya, berikan permission ke frida server menggunakan perintah ***$ chmod 777 frida-server-16.1.4-android-x86_64***.
8. Jalankan frida server menggunakan perintah ***$ ./frida-server-16.1.4-android-x86_64***.

<h3 align="left">Menjalankan Debugger untuk Android</h3>

1. Jalankan perintah ***$ frida-ps -Uai*** untuk melihat aplikasi apa yang sedang berjalan.
2. Selanjutnya, jalankan perintah ***$ frida -U --codeshare dzonerzy/fridantiroot -f $nama_package_dari aplikasi***.
3. Selesai.

