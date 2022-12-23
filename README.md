# Ujian-Akhir-Semester_Dasar-Pemograman_1227050017
<br>Mata Kuliah 	: Dasar Pemograman
<br>Nama		      : Alwan Maulana Firdaus
<br>NIM		        :	1227050017
<br>Jurusan		    :[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 


## Array Dua Dimensi
<br>1. Menampilkan banyaknya baris dan kolom, kemudian diisi dengan suatu nilai. Setelah itu, menampilkan perubahan dari baris menjadi kolom dan kolom menjadi baris
<br>2. Menampilkan deret aritmatika bilangan yag tidak habis dibagi 3, 5, 7. Input baris pertama merupakan banyaknya baris sedangkan baris kedua merupakan banyaknya kolom. Batas input adalah 0-20 . Output merupakan bilangan yang tidak habis dibagi 3, 5, 7.


## Source Code
<code>
#include <iostream>

using namespace std;

void garis(){
	cout<<"---------------------"<<endl;
}

main(){
	int row,clm,x,y,z,i;
	cout<<"Banyak Baris: ";
	baris:
	cin>>row;
	if(row>20){
		cout<<"Oops mohon masukkan nilai dari 1-20!"<<endl;
		goto baris;
	}
	cout<<"Banyak kolom : ";
	cin>>clm;
	if(clm>20){
		cout<<"Oops mohon masukkan nilai dari 1-20!!"<<endl;
		goto baris;
	}
	garis();
	
	int array[row][clm];
    cout<<"Berikan nilai pada array!"<<endl;
    garis();
    for (x=1; x<=row; x++){
    	for(y=1; y<=clm; y++){
    		cout<<" Baris ke-"<<x<<" Kolom ke-"<<y<<": \n";
    		cin>>array[x][y];
		}
		garis();
	}	
	
	cout<<"Array awal : \n";
	garis();
	for(x=1;x<=row;x++){
		for(y=1;y<=clm;y++){
				cout<<" "<<array[x][y];
		}
		cout<<endl;
	}
	garis();
	
	int hasil[x * y];
	int kali=0;
	for(x=1;x<=row;x++){
		for(y=1;y<=clm;y++){
			if(array[x][y]%3 != 0 && array[x][y]%5 != 0 && array[x][y]%7 != 0){
				hasil[kali]=array[x][y];
				kali++;
			}
		}
	}
	
	cout<<"Hasilnya yang tidak bisa dibagi 3, 5, 7 adalah : ";
	for(int i = 0; i < kali; i++){
		cout<<hasil[i];
		if(i < kali -1){
			cout<<", ";
		}else{
			cout<<".";
		}
	}
}
</code>

## Output
![uas 2](https://user-images.githubusercontent.com/98698495/208585623-49ec562a-5156-4af8-96db-ef3e68e52760.png)
![uas 2 1](https://user-images.githubusercontent.com/98698495/208585642-618615f9-cd27-4fc6-bad1-7bd9594ab3b9.png)
