//# CG-Temps-Game


#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

   

using namespace std;
   int c = 500;


int main()
{


    
    int n; // the number of temperatures to analyse
    cin >> n; cin.ignore();
    for (int i = 0; i < n; i++) {
        int t; // a temperature expressed as an integer ranging from -273 to 5526
        cin >> t; cin.ignore();

 

       int temp[n];
 temp[i] = t;

 if (temp[i] == 0){
            c = 0;
            cout << "0" << endl;
           }
           
else if (temp[i] < 0 && c < 0) {  
    if (temp[i] > c){
        c = temp[i];
    }
}

else if (temp[i] > 0 && c > 0){
  if (temp[i] < c){
        c = temp [i];
  }
}
else if (temp[i] > 0 && c < 0){
  if (temp[i] >= c - (c * 2)){
        c = temp [i];
}
}
else if (temp[i] < 0 && c > 0){
  if (temp[i] > c - (c * 2)  ){
        c = temp [i];
  }
}
 

    }
     cout << c << endl;
      // Write an answer using cout. DON'T FORGET THE "<< endl"
    // To debug: cerr << "Debug messages..." << endl;

}

