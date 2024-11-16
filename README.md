# TUGAS BAHASA PEMOGRAMAN PERTEMUAN 9

![Screenshot 2024-11-16 222855](https://github.com/user-attachments/assets/1da44130-6b33-4684-a0c3-23b6d355d701)

# Penjelasan alur flowchart:
1.	Program dimulai
2.	Proses input data siswa dimulai dengan: 
 -	Masukan Nama
 -	Masukan NIM
 -	Input Nilai Tugas
 -	Masukan Nilai UTS
 -	Masukan Nilai UAS
3.	Setelah input selesai, program menanyakan apakah ingin menambah data lagi (y/t)
4.	Jika jawaban 'y', program kembali ke proses input nama
5.	Jika jawaban 't', program akan: 
 -	Menampilkan tabel data siswa
 - Menghitung nilai akhir dengan bobot:
Tugas: 30%
UTS: 35%
UAS: 35%
Menampilkan seluruh data dalam bentuk tabel
6.	Program selesai

# Pyhton 

    # Program untuk menambahkan data ke dalam sebuah list

    # List untuk menyimpan data mahasiswa
    data_mahasiswa = []

    while True:
    # Meminta input dari user
    nama = input("Nama: ")
    nim = input("NIM: ")
    nilai_tugas = float(input("Nilai Tugas: "))
    nilai_uts = float(input("Nilai UTS: "))
    nilai_uas = float(input("Nilai UAS: "))
    
    # Menghitung nilai akhir
    nilai_akhir = (0.3 * nilai_tugas) + (0.35 * nilai_uts) + (0.35 * nilai_uas)
    
    # Menambahkan data ke list data_mahasiswa
    data_mahasiswa.append({
        "Nama": nama,
        "NIM": nim,
        "Tugas": nilai_tugas,
        "UTS": nilai_uts,
        "UAS": nilai_uas,
        "Akhir": nilai_akhir
    })
    
    # Menanyakan apakah user ingin menambah data lagi
    tambah_data = input("Tambah data(y/t)? ")
    if tambah_data.lower() != 'y':
        break

    # Menampilkan daftar data mahasiswa
    print("\n| No | Nama      | NIM   | Tugas | UTS | UAS | Akhir |")
    print("=======================================================")
    for i, mhs in enumerate(data_mahasiswa, start=1):
    print(f"| {i:<2} | {mhs['Nama']:<9} | {mhs['NIM']:<5} | {mhs['Tugas']:<5} | {mhs['UTS']:<3} | {mhs['UAS']:<3} | {mhs['Akhir']:.2f} |")

# Hasil Phyton

![Tugas petr 9](https://github.com/user-attachments/assets/ed4fd443-51b0-4d50-bc82-eb12483172fe)

