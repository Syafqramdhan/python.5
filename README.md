Pada Tugas ini Saya Telah Membersihkan Data ('marketing_data.csv')
Prinsip yang di gunakan adalah Basic OOP, Inheritance, Polymorphism

Pada Soal No 1
saya membuat sebuah class yaitu MarketingDataETL yang memiliki 3 metode:

Extract
Transform
Pada transform saya mengubah format tanggal, dan membershikan nilai NULL
Store
Membuat data store dengan data yang sudah di tranform kemudian dimasukan kedalam ('transformed_marketing_data.csv')
('transformed_marketing_data.csv') berisi data yang sudah di ubah dan di bersihkan.

Pada Soal No 2
Saya membuat class TargetedMarketing ETL yang mewarisi dari Class MarketingDataETL
Kemudian saya menambahkan Metode Segment_customers dengan kriteria: Total_spending
Total_spending = Mengelompokkan pelanggan berdasarkan jumlah harga produk yang dibeli
Kemudian hasil tersebut di simpan kedalam ('segmented_marketing_data.csv')
