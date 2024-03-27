Impor perpustakaan yang diperlukan:
import pandas as pd
Buat instance dari kelas MarketingDataETL, dengan menyediakan jalur file CSV data mentah:
etl_processor.extract()
etl_processor.transform()
etl_processor.sort_by_customer_id()
etl_processor.remove_empty_rows()
etl_processor.store("transformed_marketing_data.csv")
jalankan proses ETL dengan memanggil metode-metode terkait:
etl_processor.extract()
etl_processor.transform()
etl_processor.sort_by_customer_id()
etl_processor.remove_empty_rows()
etl_processor.store("transformed_marketing_data.csv")
Kelas MarketingDataETL
__init__(self, file_path)
Menginisialisasi kelas dengan mengatur file_path untuk file CSV data mentah.
Menginisialisasi variabel raw_data dan transformed_data untuk menyimpan data mentah dan data yang telah ditransformasi.
extract()
Membaca data mentah dari file CSV menggunakan pd.read_csv() dan menyimpannya dalam variabel raw_data.
Menangani FileNotFoundError dan pengecualian lain yang mungkin terjadi selama proses ekstraksi.
transform()
Mentransformasi kolom 'purchase_date' dalam DataFrame raw_data menjadi format 'YYYY-MM-DD' menggunakan pd.to_datetime() dan dt.strftime().
Menyimpan data yang telah ditransformasi dalam variabel transformed_data.
Menangani pengecualian yang mungkin terjadi selama proses transformasi.
sort_by_customer_id()
Mengurutkan baris dalam DataFrame transformed_data berdasarkan kolom 'customer_id' menggunakan sort_values().
Menangani pengecualian yang mungkin terjadi selama proses pengurutan.
remove_empty_rows()
Menghapus baris dengan nilai kosong (NaN) dari DataFrame transformed_data menggunakan dropna().
Menangani pengecualian yang mungkin terjadi selama proses penghapusan baris.
store(output_file)
Menyimpan DataFrame transformed_data ke file CSV baru yang ditentukan oleh output_file menggunakan to_csv().
Menangani pengecualian yang mungkin terjadi selama proses penyimpanan data.
Contoh Penggunaan
Skrip ini menyertakan contoh penggunaan di bagian bawah, di mana instance dari kelas MarketingDataETL dibuat, dan proses ETL dijalankan dengan memanggil metode-metode terkait.
etl_processor = MarketingDataETL('https://raw.githubusercontent.com/Anissls333/TPG/main/marketing_data.csv')
etl_processor.extract()
etl_processor.transform()
etl_processor.sort_by_customer_id()
etl_processor.remove_empty_rows()
etl_processor.store("transformed_marketing_data.csv")
