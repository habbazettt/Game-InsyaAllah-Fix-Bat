#include <iostream>
#include <conio.h>
#include <windows.h>
#include <cstdlib>
using namespace std;

#define KEY_UP 72
#define KEY_DOWN 80
#define KEY_LEFT 75
#define KEY_RIGHT 77

void setcolor(unsigned short color)
{
    HANDLE hCon = GetStdHandle(STD_OUTPUT_HANDLE);

    SetConsoleTextAttribute(hCon, color);
}

struct player
{
    string namaPlayer;
    int duitPlayer;
    string genderPlayer;
   	
};


int main() {
    int pil, noSatu, noDua, noTiga;
	int duit = 2000;
	int bet;
    
    
    int panjangPeta = 20; // x
    int lebarPeta = 16; // y
    
    int posisiKarakterY = 0;
    int posisiKarakterX = 1;
    
    cout << "tekan arah untuk memulai permainan";
    
    int peta[lebarPeta][panjangPeta] = {
        {1,1,5,4,4,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,1,1,1,8,1,1,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,1,1,8,6,8,1,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,1,8,6,6,6,8,1,1,1,1},
        {1,1,5,4,4,1,1,1,1,1,8,6,6,6,6,6,8,1,1,1},
        {5,1,5,4,4,1,1,1,1,8,5,5,6,6,6,5,5,8,1,1},
        {4,4,4,4,4,4,4,1,1,1,6,5,5,5,5,5,6,1,1,1},
        {4,4,4,4,4,4,4,1,1,1,6,5,5,5,5,5,6,1,1,1},
        {1,1,1,1,1,4,4,1,1,1,6,5,4,4,4,5,6,1,1,1},
        {1,1,1,1,1,4,4,1,1,1,1,1,4,4,4,1,1,1,1,1},
        {1,1,1,1,1,4,4,4,4,4,4,4,4,4,4,1,1,1,1,1},
        {1,1,1,1,1,4,4,4,4,4,4,4,4,4,4,1,1,1,1,1},
        {1,1,1,1,1,1,1,1,1,4,4,1,1,1,1,1,1,1,1,1},
        {1,1,1,1,1,1,1,1,1,4,4,1,1,1,1,1,1,1,1,1},
    };
    
    
    int arrowKey = 0;
    
    /*
    #define KEY_UP 72
    #define KEY_DOWN 80
    #define KEY_LEFT 75
    #define KEY_RIGHT 77
    */
    
    while(1) {
        // Input Keyboard
        
        char input;
        input = getch();
        
        //cout << "Masukan arrow key ";
        //cin >> arrowKey;
        //cout << "Arrow key yang dimasukan " << arrowKey << "\n";
        
        // Aturan menggerakkan karakter ke atas
        if(input==KEY_UP  && (peta[posisiKarakterY-1][posisiKarakterX] == 1 || peta[posisiKarakterY-1][posisiKarakterX] == 4) && posisiKarakterY >= 0) {
            // Gerakkan karakter ke atas
            posisiKarakterY = posisiKarakterY-1;
        }
        
        // Aturan menggerakkan karakter ke bawah
        if(input== KEY_DOWN && (peta[posisiKarakterY+1][posisiKarakterX] == 1 || peta[posisiKarakterY+1][posisiKarakterX] == 4) && posisiKarakterY < lebarPeta) {
            // Gerakkan karakter ke atas
            posisiKarakterY = posisiKarakterY+1;
        }
        
        // Aturan menggerakkan karakter ke kiri
        if(input ==KEY_LEFT && (peta[posisiKarakterY][posisiKarakterX-1] == 1 || peta[posisiKarakterY][posisiKarakterX-1] == 4) && posisiKarakterX >= 0) {
            // Gerakkan karakter ke atas
            posisiKarakterX = posisiKarakterX-1;
        }
        
        // Aturan menggerakkan karakter ke kanan
        if(input ==KEY_RIGHT && (peta[posisiKarakterY][posisiKarakterX+1] == 1 || peta[posisiKarakterY][posisiKarakterX+1] == 4) && posisiKarakterX < panjangPeta) {
            // Gerakkan karakter ke atas
            posisiKarakterX = posisiKarakterX+1;
        }
        
        if(input == 'q') {
          break;
        } else if (input == 'i') {
        	cout << "ABOUT ME!" << endl;
        	cout << "=======================" << endl;
        	cout << "=Player Name : Montel =" << endl;
			cout << "=Rp.2000              =" << endl;
			cout << "=Gender : Cowok       =" << endl;
			cout << "=======================" << endl;
			continue;
        	}
        system("cls");
        
        // Render grafik
        for(int y=0; y<lebarPeta; y++) {
            for(int x=0; x<panjangPeta; x++) {
                
                if(posisiKarakterX == x && posisiKarakterY == y) {
                	setcolor(13);
                    cout << "*" << " ";
                    setcolor(7);
                } else if(peta[y][x]==1){
                	setcolor(12);
                    cout << peta[y][x] << " ";
                    setcolor(7);
                }
                
                else if(peta[y][x]==5){
                	setcolor(5);
                    cout << peta[y][x] << " ";
                    setcolor(7);
                }
                
                else if(peta[y][x]==8){
                	setcolor(16);
                    cout << peta[y][x] << " ";
                    setcolor(7);
                }
                
                else if(peta[y][x]==4){
                	setcolor(2);
                    cout << peta[y][x] << " ";
                    setcolor(7);
                }
                
                else if(peta[y][x]==6){
                	setcolor(9);
                    cout << peta[y][x] << " ";
                    setcolor(7);
                }
                if(posisiKarakterX==13 && posisiKarakterY==10){
                	
                	while(true){
					system ("cls");
					noSatu = (rand() % 9) + 1;
					noDua = (rand() % 9) + 1;
					noTiga = (rand() % 9) + 1;
					cout << "=========================================" << endl;
				    cout << "=========================================" << endl;
				    cout << "==                                     ==" << endl;
				    cout << "==           ODIN IN VALHALLA          ==" << endl;
				    cout << "==                                     ==" << endl;
				    cout << "=========================================" << endl;
				    cout << "=========================================" << endl;
				    cout << "\n";
									
					cout<<"MARI HABISKAN UANGMU! HAHA"<<endl;
					cout<<"=========================="<<endl;				
					cout<<"Duit : "<<duit<<endl;
					cout<<"Angka Pertama : "<<noSatu<<endl;
					cout<<"==============="<<endl;
					cout<<"Angka Kedua :  "<<noDua<<endl;
					cout<<"==============="<<endl;
					cout<<"Angka Ketiga : "<<noTiga<<endl;
					cout<<"==============="<<endl;
					cout<<"Bet : ";
					cin>>bet;
					
					
					if(duit >= bet){
					if(noSatu != noDua && noTiga){
						duit -= bet;
						}else if(noSatu == noDua && noTiga){
						duit += bet*2;}
						
					}else if(duit == 0){
						cout<<"Cabut dah lu"<<endl;
						continue;				
					}
							}
                	
				}
            }
            cout << "\n";
        }
    }

       
    return 0;
}
