1.PENGAMBILAN KEPUTUSAN
Jenis-jenis pengambilan keputusan adalah sebagai berikut:

## 1. IF 
    -   Memerlukan nilai bool (dari operator logical atau comparison)
    -   Menjalankan bagian proses jika nilai bool bernilai true

Contoh

    
        if(nilai_bool){
        // proses jika nilai_bool adalah true
        }
    

## 2. IF-ELSE
    -   Berjalan dengan if
    -   Menambah alternatif jika nilai bool adalah false

Contoh 

    
        if(nilai_bool){
            // proses jika nilai_bool adalah true
        } else {
            // proses jika nilai_bool adalah false
        } 
    

## 3. ELSE-IF
    -   Berjalan dengan if
    -   Menambah alternatif jika nilai bool adalah false
    -   Menambah pengujian nilai bool lain

Contoh

    
        if(nilai_bool){
            // proses jika nilai_bool adalah true
        } else if(nilai_bool1) {
            // proses jika nilai_bool adalah false
            // dan nilai_bool1 adalah
        } 
    

# 2.PERULANGAN
## 1. FOR
    -   Diketahui berapa kali perulangan terjadi
    -   Memerlukan nilai awal
    -   Memerlukan nilai bool, jika true maka perulangan dilanjutkan 
    -   Memerlukan pengubah nilai

Contoh

    
        for (nilai_awal; nilai_bool, pengubah_nilai_awal) {
            // Proses berulang jika nilai_bool adalah true
        }
    

## 2. WHILE
    -   Tidak diketahui berapa kali perulangan terjadi
    -   Memerlukan nilai bool , jika true maka perulangan dilanjutkan

Contoh

    
        while (nilai_bool){
            // Proses berulang jika nilai bool adalah true
        }
    

## 3. DO-WHILE
    -   Mengubah bentuk while
    -   Proses dijalankan minimum sekali, akan diteruskan jika nilai bool adalah true

Contoh 

    
        do {
            // Proses berulang jika nilai_bool adalah true
        } while(nilai_bool);
    



# 3.FUNGSI (Kumpulan kode yang dapat digunakan ulang)
-   Kumpulan perintah
-   dapat digunakan berkali-kali
-   Cukup mengubah fungsi sekali, penggunaan lainnya akan ikut berubah

Contoh membuat fungsi

    
    tipe_data nama_fungsi(){
        // Perintah yang dijalankan saat fungsi dipanggil
    }
    

Contoh memanggil fungsi

    
    nama_fungsi();
    

# 4.FUNGSI DENGAN PARAMETER 

Mengirim data saat menjalankan fungsi


    tipe_data nama_fungsi(tipe_data nama_parameter){
        // Perintah yang dijalankan saat fungsi dipanggil
    }


## 5.FUNGSI DENGAN RETURN

Memberi nilai pada fungsi saat dipanggil


    tipe_data nama_fungsi(tipe_data nama_parameter){
        // Perintah yang dijalankan saat fungsi dipanggil
        return nilai;
    }