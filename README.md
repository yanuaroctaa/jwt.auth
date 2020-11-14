Yanuar Octavianus
185150700111006

Modul 3
Step:
1. Membuka cmd, lalu ketik composer create-project --prefer-dist laravel/lumen jwt-app untuk membuat direktori bookapp di folder user
2. Membuat database baru di phpmyadmin dengan nama jwt.auth
3. Buka .env lalu sesuaikan nama database, password untuk menyambungkan dengan database
4. Menjalankan perintah composer require tymon/jwt-auth untuk instalasi package JWT
5. Buka bootstrap/app.php, lalu aktifkan fitur Eloquent, Facades, Middleware Auth, dan daftarkan package JWT
6. Menjalankan perintah php artisan jwt:secret untuk men generate secret key untuk JWT, yang disimpan di .env
7. Membuat migration user dengan perintah php artisan make:migration create_users_table --create=users
8. Tambahkan id, username, password di dalam migration
9. Menjalankan perintah php artisan migrate untuk mengeksekusi migration
10. Buka model user, lalu tambahkan use Tymon\JWTAuth\Contracts\JWTSubject;. Di bagian class nya tambahkan juga JWTSubject. Dan di dalam class user tambahkan fungsi getJWTIdentifier() dan getJWTCustomClaims().
11. Buat folder config di root, lalu buat file auth.php (kita bisa mengambil contoh VBsource code auth di vendor/config/auth)
12. Tambahkan driver jwt dan provider user di dalam auth.php
13. Buat file UserController lalu tambahkan fungsi constructor untuk membatasi akses pengguna yang belum login
14. Tambahkan fungsi index di UserController untuk melihat list pengguna pengguna
15. Tambahkan fungsi register di UserController untuk mendaftarkan pengguna
16. Tambahkan fungsi login di UserController untuk masuk jika sudah mendaftar
17. Tambahkan fungsi me di UserController untuk melihat pengguna tersebut
18. Tambahkan fungsi logout di UserController untuk keluar 
19. Menambahkan router baru yaitu $router->post('/register', 'UserController@register');
20. Menambahkan router baru yaitu $router->post('/login', 'UserController@login');
21. Menambahkan router baru yaitu $router->get('/user', 'UserController@index');
22. Menambahkan router baru yaitu $router->get('/me', 'UserController@me');
23. Menambahkan router baru yaitu $router->get('/logout', 'UserController@logout');
24. Melakukan test untuk seluruh fungsi
25. Meng inisiasi git dengan git init
26. Memasukkan file dengan git add .
27. Membuat commit dengan git commit -m "JwpApp"
28. Menambahkan link dengan git remote add origin "https://github.com/yanuaroctaa/jwt.auth"
29. Melakukan push dengan git push -u origin master