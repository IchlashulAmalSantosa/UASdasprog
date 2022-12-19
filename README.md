# Ujian Akhir Semester
<br> Mata kuliah : Dasar Pemrograman
<br> Nama : Ichlashul 'Amal Santosa
<br> Nim : 1227050054
<br>Jurusan		: [Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## DESKRIPSI UMUM
1).Untuk mentransposisi sebuah matrix (membalikkan posisi baris dan kolom), kita dapat menggunakan rumus berikut:
matrix_transpose[j][i] = matrix[i][j]
Di mana matrix adalah matrix yang ingin kita transposisi, dan matrix_transpose adalah matrix hasil transposisi. i dan j adalah indeks baris dan kolom dari matrix_transpose.
Program ini akan meminta input ukuran matrix, kemudian akan meminta input isi matrix. Setelah itu, program akan menampilkan matrix sebelum dan sesudah transposisi.
==================================================================================================================================================================
2).Program ini akan meminta input sebuah bilangan, kemudian akan mengecek apakah bilangan tersebut habis dibagi 3, 5, atau 7. Jika ya, maka program akan mencetak "Bilangan habis dibagi 3, 5, atau 7". Jika tidak, program akan mencetak "Bilangan tidak habis dibagi 3, 5, atau 7".
Sebagai contoh, jika kita memasukkan bilangan 15, maka program akan mencetak "Bilangan habis dibagi 3, 5, atau 7". Namun jika kita memasukkan bilangan 8, maka program akan mencetak "Bilangan tidak habis dibagi 3, 5, atau 7".

## SOURCE CODE
1).
#include<iostream>
#include<iomanip>
using namespace std;

int main(){
    
	int arr[100][100], jumlahBaris, jumlahKolom, i, j, baris, kolom;
	
	cout<< "=======================================\n";
	cout<< "Program Mencetak Matrix Transpos\n";
	cout<< "=======================================\n";
	cout<< "Nama  : Ichlashul 'Amal Santosa\n";
	cout<< "Nim   : 1227050054\n";
	cout<< "Kelas : Informatika - B\n\n";

    cout<<"Input jumlah baris: "; cin>>jumlahBaris;
    cout<<"Input jumlah kolom: "; cin>>jumlahKolom;
    cout << endl;

    for(i = 0; i < jumlahBaris; i++){
        for(j = 0; j < jumlahKolom; j++){
            cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
            cin >> arr[i][j];
        }
        cout << endl;
    }
    cout << "Hasil matriks: " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    for(j = 0; j < jumlahKolom; j++){
        cout << setw(3) << arr[i][j] << " ";
    }
    cout << endl;
    }

    baris = jumlahBaris;
    kolom = jumlahKolom;

    jumlahKolom = baris;
    jumlahBaris = kolom;

    cout << "\nUbah kolom jadi baris dan baris jadi kolom: " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    	for(j = 0; j < jumlahKolom; j++){
        cout << setw(3) << arr[j][i] << " ";
    }
    cout << endl;
    }
	return 0;
}

=======================================================================================

2).
#include <iostream>
#include <iomanip>
using namespace std;
int main(){
    
	int arr[100][100], jumlahBaris, jumlahKolom, i, j, baris, kolom;
	
	cout<< "==============================================\n";
	cout<< "Program Bilangan Yang Habis Dibagi 3, 5, dan 7\n";
	cout<< "==============================================\n";
	cout<< "Nama  : Ichlashul 'Amal Santosa\n";
	cout<< "Nim   : 1227050054\n";
	cout<< "Kelas : Informatika - B\n\n";

    cout<<"Input jumlah baris: "; cin>>jumlahBaris;
    cout<<"Input jumlah kolom: "; cin>>jumlahKolom;
    cout << endl;

    for(i = 0; i < jumlahBaris; i++){
        for(j = 0; j < jumlahKolom; j++){
            cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
            cin >> arr[i][j];
        }
        cout << endl;
    }

    cout << "Hasil input nilai : " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    for(j = 0; j < jumlahKolom; j++){
        cout << setw(3) << arr[i][j] << " ";
    }
    cout << endl;
    }

    cout << "\nHasil bilangan yang habis dibagi 3,5,7 : " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    for(j = 0; j < jumlahKolom; j++){
        if(arr[i][j] % 3 == 0 || arr[i][j] % 5 == 0 || arr[i][j] % 7 == 0){
        cout << setw(3) << arr[i][j] << " ";
        }
    }
    cout << endl;
    }

    
    cout << endl;
    return 0;
}

## OUTPUT
1).
=======================================
Program Mencetak Matrix Transpos
=======================================
Nama  : Ichlashul 'Amal Santosa
Nim   : 1227050054
Kelas : Informatika - B

Input jumlah baris: 2
Input jumlah kolom: 3

Baris 1, kolom 1 = 10
Baris 1, kolom 2 = 20
Baris 1, kolom 3 = 30

Baris 2, kolom 1 = 30
Baris 2, kolom 2 = 20
Baris 2, kolom 3 = 10

Hasil matriks:
 10  20  30
 30  20  10

Ubah kolom jadi baris dan baris jadi kolom:
 10  30
 20  20
 30  10

================================================================================

2).
==============================================
Program Bilangan Yang Habis Dibagi 3, 5, dan 7
==============================================
Nama  : Ichlashul 'Amal Santosa
Nim   : 1227050054
Kelas : Informatika - B

Input jumlah baris: 2
Input jumlah kolom: 3

Baris 1, kolom 1 = 12
Baris 1, kolom 2 = 13
Baris 1, kolom 3 = 14

Baris 2, kolom 1 = 21
Baris 2, kolom 2 = 31
Baris 2, kolom 3 = 41

Hasil input nilai :
 12  13  14
 21  31  41

Hasil bilangan yang habis dibagi 3,5,7 :
 12  14
 21
