## Assignment 18
Buat tugas khusus Gradle dan add libraries

Kriteria:
- buat tugas Gradle sederhana untuk menerima parameter CLI dan mencetaknya dengan pesan ucapan
- Proyek skrip Gradle harus dibuat di repositori yang berbeda dan dorong ke GitHub
Berikut adalah langkah-langkah untuk membuat tugas khusus Gradle dan menambahkan pustaka:

Buat proyek Gradle baru dengan menjalankan perintah "gradle init --type java-library". Ini akan membuat proyek Gradle baru dengan struktur direktori dan file build.gradle awal.

Buka file build.gradle di direktori root proyek dan tambahkan kode berikut untuk menentukan tugas khusus:

task greetingTask(type: DefaultTask) {
    doLast {
        String name = project.hasProperty('name') ? project.property('name') : 'Gradle User'
        println "Hello, $name! Welcome to Gradle World!"
    }
}

Anda dapat menjalankan tugas dengan menjalankan perintah berikut: "./gradlew greetingTask -Pname=YourName"

Untuk menambahkan pustaka, Anda dapat menggunakan fitur manajemen dependensi bawaan Gradle. Untuk melakukannya, tambahkan kode berikut ke file build.gradle Anda:

dependencies {
    implementation 'com.google.guava:guava:29.0-jre'
    testImplementation 'junit:junit:4.13'
}

Terakhir, dorong proyek ke GitHub dengan membuat repositori baru dan menjalankan perintah berikut:

git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<your_username>/<repository_name>.git
git push -u origin master

## Tujuan
Membuat projek gradle sederhana

Command: gradlew greetingTask -Pargs=User <br/>
Hasil run: <br/>
![alt text](https://github.com/aufarr16/testGradle/blob/master/hasil%20run%20gradle%20project.png?raw=true)
