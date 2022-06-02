## Tugas 6 MK Sistem Basis Data "Backup dan Restore MYSQL"

### 1. Backup dan Recovery Database dengan Perintah Sql.
##### a. Tabel Users
<img width="780" alt="backup_restore_sql_tabel_users" src="https://user-images.githubusercontent.com/69449808/171566331-7b49d428-0605-43e7-a018-5a1e7756460e.png">

##### b. Tabel Dokter
<img width="780" alt="backup_restore_sql_tabel_dokter" src="https://user-images.githubusercontent.com/69449808/171567025-35e81159-6b58-40ab-8e0d-0c1cd116473a.png">

##### c. Tabel Pasien
<img width="780" alt="backup_restore_sql_tabel_pasien" src="https://user-images.githubusercontent.com/69449808/171567578-8623caa2-9879-4ee4-9e1e-6c781718d602.png">

##### d. Tabel Berobat
<img width="780" alt="backup_restore_sql_tabel_berobat" src="https://user-images.githubusercontent.com/69449808/171567536-eba7b4f7-1e05-4a15-a2d7-5afa3216679c.png">

##### e. Tabel Obat
<img width="780" alt="backup_restore_sql_tabel_obat" src="https://user-images.githubusercontent.com/69449808/171567657-17c80fbe-bd79-4782-8e40-f03488aee45d.png">

##### f. Tabel Resep Obat
<img width="780" alt="backup_restore_sql_tabel_resep_obat" src="https://user-images.githubusercontent.com/69449808/171567725-52d5abb9-d8ad-4567-bbbb-cd56503adf6e.png">

###### Hasil Backup:
<img width="650" alt="ss_file_backup_perintah_sql" src="https://user-images.githubusercontent.com/69449808/171568595-ad687f80-9de3-456e-9d07-df58ef796f3b.png">

### 2. Backup dan Recovery Database Menggunakan MySQLDump.
<img width="780" alt="backup_restore_db_mysqldump" src="https://user-images.githubusercontent.com/69449808/171568344-3ae4e56c-f50c-406a-a7e3-35ba27a3f3eb.png">


### 3. Backup Database MySQL Otomatis dengan cron job.

##### a. Script untuk melakukan backup otomatis mysql setiap hari minggu jam 12:00 malam:

0 0 * * 0 mysqldump -u adminklinik -p312010147 klinik_312010147 > backup_db_klinik.sql

##### b. Script dengan menambahkan postfix tanggal dan waktu pada setiap file .sql dari hasil backup:

0 0 * * 0 mysqldump -u adminklinik -p312010147 klinik_312010147 > backup_db_klinik_`date '+%Y-%m-%d@%H:%M'`.sql
