#include <iostream>
using namespace std;

const int MAX = 5;
int array[MAX] = {2, 8, 7};
int size;
int ind;
int val;


int sizeAr (){
    int ukuranArray = 0;
    for (int i = 0; i < MAX; i++) {
        if (array[i] != 0) {
            ukuranArray++;
        } else {
            break;
        }
    }
    return ukuranArray;
}

void insertAt (int index, int value) {
    int size = sizeAr();
    int pos;
        if (size >= index ) {
            for (int i = size; i > index-1; i--){
                array[i] = array[i-1];
            }
            array[index-1] = value;
        }
        else {
            pos = index-size;
            array[index-pos] = value;
        }
    cout <<"Berhasil ditambahkan."<<endl <<endl;
}

void tampilArray () {
    size = sizeAr();
    // Tampilkan Isi Array
        cout << "Isi Array  : ";
        for(int i = 0; i < size; i++) {
            cout << array[i] << "  ";
        }}

void hapus(int index){
    size = sizeAr();
    int ind = index-1;
    array[ind] = 0;
    for(int i = ind; i < size; i++ ){
        array[i] = array[i+1];
    }
    cout << "Index ke-"<<index <<" berhasil dihapus."<<endl <<endl;
}

void cariArray(int value){
    size = sizeAr();
    bool ketemu;
    for(int i = 0; i<size; i++){
        if(array[i]==value) {
            cout<<"element ditemukan di index :"<<i<<endl;
            ketemu = true;
            break;
        } };
    if(!ketemu){
            cout<<"element tidak ditemukan.";
        }
}

void bubbleSort (){
    int temp;
    size = sizeAr();
    for(int i = 0; i < size-1; i++){
        for(int j = 0; j < size-1; j++){
            if(array[j] > array[j+1]){
                temp = array[j];
                array[j] = array[j+1];
                array[j+1] = temp;
            }
        }
    }
    cout<<"Array sudah diurutkan." <<endl<<endl;
}

void selectionSort(){
    size = sizeAr();
    int temp, pos;
    for(int i = 0; i < size; i++){
        temp = array[i];
        pos = i;
        for(int j = i; j < size; j++){
            if(array[j]<temp){
                temp=array[j];
                pos =j;
            }
        }
        array[pos]=array[i];
        array[i] =temp;
    }
    cout<<"Array Sudah Diurutkan"<<endl<<endl;
}

int main()
{

    int pilih;

     menu :
    cout << "=== DAFTAR MENU ===" <<endl;
    cout << "1. Insert Array" <<endl;
    cout << "2. Delete Array" <<endl;
    cout << "3. Edit Array" <<endl;
    cout << "4. Cek Apakah Array kosong" <<endl;
    cout << "5. Mengecek apakah Array Full" <<endl;
    cout << "6. Searching Element di Array" <<endl;
    cout << "7. Sorting Elemen Di Array (Buble sort)" <<endl;
    cout << "8. Sorting Elemen  Di Array (Selection Sort)" <<endl;
    cout << "9. Exit"<<endl;


    cout << "Pilih MENU : " <<endl;
    cin >> pilih;

switch (pilih) {
    case 1:
        cout<<endl << "== INSERT ARRAY ==" << endl;
        tampilArray();

        // ========== INSERT ARRAY =============
            cout << endl;
            cout << "Array ke berapa yang akan diinsert? : ";
            cin >> ind;

            while (ind > 5) {
                cout << "Index yang dipilih salah/terlalu banyak, pilih ulang! : ";
                cin >> ind;
            }

            cout << "Masukkan value yang akan diinsert! : ";
            cin >> val;
            insertAt(ind, val);

        tampilArray();
        cout << endl << "=================" <<endl <<endl;

        // break;
    goto menu;

    case 2:

        cout <<"== HAPUS ARRAY =="<< endl;
        tampilArray();
        cout<<endl;
        cout <<"Index Array yang akan dihapus : ";
        cin >> ind;
        hapus(ind);
        tampilArray();
        cout<<endl << "=================" << endl;
    goto menu;

    case 3:
        cout<<"== EDIT ARRAY ==" <<endl<<endl;
        tampilArray();
        cout<<endl;
        cout<<"Index array yang akan diubah : "; cin>>ind;
        cout<<"Value index yang dipilih : "<< array[ind-1] <<endl;
        cout<<"Value diubah menjadi : "; cin>>val;
        array[ind-1] = val;
        cout<<"Edit Array Berhasil."<<endl;
        tampilArray();
        cout<< endl;
    goto menu;

    case 4:
        cout<<"== CEK APAKAH ARRAY KOSONG =="<<endl<<endl;
        tampilArray();
        cout<<endl;
        size = sizeAr();
        if (size > 0) {
            cout<<"Array tidak kosong"<<endl;
        } else {
            cout<<"Array Kosong"<<endl;
        }
    goto menu;
    case 5:
        cout<<"== CEK APAKAH ARRAY FULL =="<<endl<<endl;
        tampilArray();
        cout<<endl;
        size = sizeAr();
        if(size == MAX){
            cout<<"Array Penuh"<<endl;
        }
        else {cout<<"Array tidak penuh"<<endl<<endl;}
    goto menu;

    case 6:

        cout <<"== Meancari Element dalam Array =="<<endl<<endl;
        cout<<"Masukkan Element yang akan dicari :";
        cin>>val;
        cariArray(val);
        cout<<endl<<endl;
    goto menu;

    case 7:
        cout<<"== Bubble Sorting =="<<endl<<endl;
        tampilArray();
        cout<<endl<<endl;
        bubbleSort();
        tampilArray();
    goto menu;

    case 8:
        cout<<endl<<"== Selection Sort =="<<endl<<endl;
        tampilArray();
        cout<<endl<<endl;
        selectionSort();
        tampilArray();
        cout<<endl;
    goto menu;

    case 9:
        cout << "==== TELAH KELUAR ====";
    break;
    }

    return 0;
}
