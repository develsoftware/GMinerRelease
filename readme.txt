
@@ -1,23 +1 @@
Pilihan:

'--algo' atau singkatnya '-a' - algoritma penambangan ('equihash96_5', 'equihash144_5', 'equihash150_5', 'equihash192_7', 'equihash210_9', 'cuckaroo29', 'cuckatoo31', 'cuckatoo31', 'cuckkatoo31', 'cuckoo' atau singkat: ' 96_5 ',' 144_5 ',' 150_5 ',' 192_7 ',' 210_9 ',' grin29 ',' grin31 ',' aeternity ')
'--cuda_devices' - daftar perangkat yang tersedia untuk ditambang
'--server' atau tak lama '-s' - alamat pool penambangan (misalnya: 'eu.btgpool.pro', 'eu1.zhash.pro')
'--port' atau segera '-n' - port pool penambangan (misalnya: '5057', '1445')
'--user' atau singkatnya '-u' - nama pekerja pool pool atau alamat dompet (misalnya: 'sRuJK1BmA758GbOn.worker', 'GfGLyfP9GzZbPeTzvW1KSx3HeMnrNAiGWY.rig0')
'- pass' atau singkatnya '-p' - kata sandi pekerja atau kata sandi kumpulan standar, dapat kosong, nilai defaultnya adalah 'x' (misalnya: 'sRuJK1Bm')
'--ssl' - aktifkan / nonaktifkan koneksi aman dengan pool penambangan, harus didukung oleh pool, bisa kosong, nilai default adalah '0' ('0' - off atau '1' - on)
'--ssl_verification' - aktifkan / nonaktifkan verifikasi sertifikat untuk koneksi aman, itu mungkin tidak berfungsi dengan kumpulan yang telah kadaluarsa sertifikat, bisa kosong, nilai default adalah '0' ('0' - off atau '1' - on)
'--device' atau singkatnya '-d' - daftar perangkat cuda yang dipisahkan oleh ruang, bisa kosong, nilai default adalah semua perangkat yang tersedia (misalnya: '1 3 5')
'--logfile' atau segera '-l' - nama file untuk menyimpan log pada disk, dapat kosong, nilai default adalah '' (misalnya: '/usr/user/miner.log', 'c: \ miner.log ')
'--templimit' atau segera '-t' - daftar batas suhu yang dipisahkan oleh ruang, setelah mencapai batas, GPU menghentikan penambangan hingga dingin, dapat kosong (misalnya: '85 80 75 ')
'--color' atau segera '-c' - aktifkan / nonaktifkan output warna untuk konsol, nilai default adalah '1' ('0' - off atau '1' - on)
'- watchdog' atau segera '-w' - mengaktifkan / menonaktifkan watchdog, watchdog memonitor proses penambangan utama dan me-restart aplikasi jika terjadi kegagalan atau kehilangan koneksi ke pool, bisa kosong, nilai defaultnya adalah '1 '(' 0 '- mati atau' 1 '- aktif)
'--api' - port server telemetri, memungkinkan Anda memantau status penambang dari jarak jauh, membuka tautan di peramban Anda http: // localhost: <port> (misalnya: '10050', '20030')
'--config' - tentukan file konfigurasi
'--pers' - string personalisasi untuk algoritme equihash (misalnya: 'BgoldPoW', 'BitcoinZ', 'Safecoin')
'--pec' - mengaktifkan / menonaktifkan kalkulator efisiensi daya. Kalkulator efisiensi daya menampilkan statistik efisiensi energi GPU dalam S / w, beban CPU lebih tinggi. Nilai default adalah '1' ('0' - mati atau '1' - aktif)
'--electricity_cost' - lulus biaya listrik dalam USD per kWh, penambang akan melaporkan $ dihabiskan untuk menambang

DevFee:
Biaya adalah 2%
GMiner
