# tugas-arsy
Nama : Muhammad Arsy Al-Fahd
NIM : 2309116079

print("---------------------------")
print("-------Halaman Login-------")
print("---------------------------")

pengguna = {
    'Nama': 'Arsy',
    'NIM': '2309116079'
}

x = input("Nama : ")
y = input("NIM : ")

if  x==pengguna["Nama"] and y==pengguna["NIM"]:
    print("Login berhasil, Selamat datang " + x + "!!")
    
    print("\n-------Konversi Mata Uang-------")
    total_idr = float(input("Masukkan jumlah uang dalam IDR: "))
    print("Konversi IDR ke mata uang :")
    print("1.USD")
    print("2.Yen")
    print("3.Ringgit Malaysia")
    
    #mendefinisikan nilai tukar kurs
    nilai_tukar_1 = 0.000065 #1 rupiah ke dollar
    nilai_tukar_2 = 0.097 #1 rupiah ke yen
    nilai_tukar_3 = 0.00031 #1 rupiah ke ringgit

    pilihan = input("Masukkan pilihan (1/2/3): ")
    if pilihan == '1':
        def idr_ke_usd(total_idr, nilai_tukar_1):
            jumlah_usd = total_idr * nilai_tukar_1
            return jumlah_usd
        jumlah_usd = idr_ke_usd(total_idr, nilai_tukar_1)
        print(f"{total_idr} IDR sama dengan {jumlah_usd} USD")
    elif pilihan == '2':
        def idr_ke_jpy(total_idr, nilai_tukar_2):
            jumlah_jpy = total_idr * nilai_tukar_2
            return jumlah_jpy
        jumlah_jpy = idr_ke_jpy(total_idr, nilai_tukar_2)
        print(f"{total_idr} IDR sama dengan {jumlah_jpy} JPY")    
    elif pilihan == '3':
        def idr_ke_myr(total_idr, nilai_tukar_3):
            jumlah_myr = total_idr * nilai_tukar_3
            return jumlah_myr
        jumlah_myr = idr_ke_myr(total_idr, nilai_tukar_3)
        print(f"{total_idr} IDR sama dengan {jumlah_myr} MYR")
    else:
        print("Kesalahan")

else:
    print("Username atau Password Anda Salah, Silahkan coba lagi")

output nya adalah hasil konversi dari idr ke mata uang yang user pilih.
