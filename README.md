# java_gradle

proyek ini dibuat untuk melatih dalam menggunakan serta mengelola perintah-perintah gradle pada pembahasan saat ini,
serta menghubungkan juga memanfaatkan repository penggunaan git dalam penggunaan gradle saat ini.

langkah-langkah yang dilakukan adalah:
1. membuat repo github
2. clone repo github
3. lalu buat java project - menggunakan gradle architecture
4. kemudian ikutin perintah:
   a. plugin CLI menggunakan Java
   b. gradle init java-library
   c. dependencies:
       a. source code java - implementation 'com.google.guava:guava:29.0-jre'
       b. test build - JUnit - testImplementation 'junit:junit:4.13'
       c. test build cucumber, selenium - implementation 'io.cucumber:cucumber-java:6.9.1'; implementation 
         'org.seleniumhq.selenium:selenium-java:3.141.59'
       d. fungsi rest io untuk update setiap saat - implementation 'io.rest-assured:rest-assured:4.3.3'
   d. kemudian buka tab build.gradle, lakukan:
   1. custom task - task yang dieksekusi sesuai yang diinginkan (bukan by default - otomatis)
   2. tuliskan kode:
      task greetingTask() {
    doLast {
        String nama = project.hasProperty('nama') ? project.property('nama') : 'Gradle User'
        println "Hello, $nama! Welcome to Gradle World!"
    }
}
5. lakukan push ke github:
   a. git init
   b. git add .
   c. git commit -m "<message>"
   d. git remote add <nama file> <link url github clone>
   e. git push

