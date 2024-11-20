class DataNilai:
    def __init__(self):
        self.data = {}

    def tampilkan_menu(self):
        print("\nProgram Input Nilai")
        print("="*20)
        print("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari (K)eluar]: ")

    def tampilkan_daftar(self):
        print("\nDaftar Nilai")
        print("="*61)
        print("| NO |    NIM    |    NAMA    | TUGAS | UTS | UAS | AKHIR |")
        print("="*61)
        if not self.data:
            print("|                     TIDAK ADA DATA                         |")
        else:
            for idx, (nim, nilai) in enumerate(self.data.items(), 1):
                nama = nilai['nama']
                tugas = nilai['tugas']
                uts = nilai['uts']
                uas = nilai['uas']
                akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
                print(f"| {idx:2} | {nim:9} | {nama:10} | {tugas:5} | {uts:3} | {uas:3} | {akhir:5.2f} |")
        print("="*61)
        print("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari (K)eluar]: ")

    def tambah_data(self):
        print("\nTambah Data")
        nim = input("NIM         : ")
        nama = input("Nama        : ")
        tugas = int(input("Nilai Tugas : "))
        uts = int(input("Nilai UTS   : "))
        uas = int(input("Nilai UAS   : "))
        
        self.data[nim] = {
            'nama': nama,
            'tugas': tugas,
            'uts': uts,
            'uas': uas
        }
        
        self.tampilkan_daftar()

    def ubah_data(self):
        print("\nUbah Data")
        nim = input("Masukkan NIM: ")
        if nim in self.data:
            nama = input("Nama        : ")
            tugas = int(input("Nilai Tugas : "))
            uts = int(input("Nilai UTS   : "))
            uas = int(input("Nilai UAS   : "))
            
            self.data[nim] = {
                'nama': nama,
                'tugas': tugas,
                'uts': uts,
                'uas': uas
            }
        else:
            print("Data tidak ditemukan")
        self.tampilkan_daftar()

    def hapus_data(self):
        print("\nHapus Data")
        nim = input("Masukkan NIM: ")
        if nim in self.data:
            del self.data[nim]
        else:
            print("Data tidak ditemukan")
        self.tampilkan_daftar()

    def cari_data(self):
        print("\nCari Data")
        nim = input("Masukkan NIM: ")
        if nim in self.data:
            nilai = self.data[nim]
            print(f"NIM         : {nim}")
            print(f"Nama        : {nilai['nama']}")
            print(f"Nilai Tugas : {nilai['tugas']}")
            print(f"Nilai UTS   : {nilai['uts']}")
            print(f"Nilai UAS   : {nilai['uas']}")
        else:
            print("Data tidak ditemukan")
        print("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari (K)eluar]:t")

def main():
    aplikasi = DataNilai()
    aplikasi.tampilkan_menu()
    
    while True:
        pilihan = input().lower()
        if pilihan == 'l':
            aplikasi.tampilkan_daftar()
        elif pilihan == 't':
            aplikasi.tambah_data()
        elif pilihan == 'u':
            aplikasi.ubah_data()
        elif pilihan == 'h':
            aplikasi.hapus_data()
        elif pilihan == 'c':
            aplikasi.cari_data()
        elif pilihan == 'k':
            break
        else:
            print("Pilihan tidak valid")

if __name__ == "__main__":
    main()