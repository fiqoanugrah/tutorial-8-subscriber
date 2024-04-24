## **Hi! :wave:, I'm Muhammad Fiqo Anugrah and this is my repo for Tutorial 8 Adpro C**


> REFLECTION

a. what is amqp?

AMQP adalah singkatan dari Advanced Message Queuing Protocol, yang merupakan protokol komunikasi berbasis standar yang digunakan untuk memfasilitasi pertukaran pesan secara asinkron antara komponen aplikasi, layanan, atau sistem. Protokol ini dirancang untuk memastikan komunikasi yang andal dan aman, mendukung berbagai fitur seperti message queuing, routing (melalui exchange dan binding), publikasi-subskripsi, dan transaksi. Keandalan dan fleksibilitas AMQP membuatnya sangat cocok untuk aplikasi yang membutuhkan pengiriman pesan yang terjamin dan efisien di lingkungan terdistribusi.

b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for? 

"guest:guest": Ini merupakan pasangan nama pengguna dan kata sandi yang digunakan untuk autentikasi ke server AMQP. Dalam konteks ini, "guest" adalah nama pengguna default dan juga kata sandi default yang sering digunakan dalam pengaturan pengembangan atau tes, bukan produksi, karena alasan keamanan.
"localhost": Kata ini mengindikasikan bahwa koneksi ke server AMQP akan dibuat ke mesin lokal, yaitu komputer di mana perintah ini dijalankan. Ini sering digunakan untuk pengujian dan pengembangan lokal di mana server berjalan pada mesin yang sama dengan klien.
"5672": Ini adalah nomor port TCP standar yang digunakan oleh server AMQP untuk mendengarkan koneksi masuk. Port ini telah ditetapkan oleh konvensi untuk komunikasi AMQP, meskipun dapat dikonfigurasi untuk menggunakan port lain jika diperlukan.
Secara keseluruhan, "guest:guest@localhost:5672" menggambarkan penggunaan kredensial default untuk mengakses server AMQP yang berjalan di mesin lokal pada port standar. Ini biasanya digunakan untuk tujuan pengembangan dan pengujian.


