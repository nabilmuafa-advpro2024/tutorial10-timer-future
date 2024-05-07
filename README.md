# Tutorial 10.1 Reflection Notes

## 1.2 Understanding How It Works

Pada pemrograman secara asikronus, instruksi tidak dijalankan secara sekuential/berurutan. Dalam hal ini, fungsi `main()` awalnya membuat executor dan spawner terlebih dahulu, kemudian memanggil spawn pada spawner secara asinkronus untuk mem-spawn sebuah thread terpisah yang bisa mengeksekusi instruksi yang diberikan pada spawner. Karena instruksi baru diberikan ke spawner dan belum ada instruksi untuk mengeksekusinya, maka instruksi belum dijalankan. Kemudian `main()` menerima instruksi mencetak "hey hey" dan menjalankannya lebih dulu. Barulah di akhir `main()`, executor untuk thread yang sudah di spawn tadi dijalankan dan "howdy!" serta "done!" dicetak. Itulah mengapa urutannya justru "hey hey" paling dulu.
