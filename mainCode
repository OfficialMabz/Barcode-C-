//Barcode-system
//Barcode system for stores

/******************************************************************************

            This is a barcode system for Herts Store
Where the user would insert the barcode and get their item list with total price
               Coder name: Mahbubur Rahman
               Student ID: 18027470.

*******************************************************************************/
#include <iostream>
#include <string>
#include <stdlib.h>
#include <ctime>
#include <iomanip>

using namespace std;

void Menu (){
    // Below information will be presented in table format to show the product information

    cout << setw(5) << "Barcode" << setw(15) << "ITEM" << setw(15) << "Price(GB)" << endl << endl;
    cout << setw(5) << "0120001" << setw(15) << "Milk" << setw(15) << "10.50" << endl;
    cout << setw(5) << "0120002" << setw(15) << "Bread" << setw(15) << "5.50" << endl;
    cout << setw(5) << "0120003" << setw(15) << "Chocolate" << setw(15) << "8.00" << endl;
    cout << setw(5) << "0120004" << setw(15) << "Towel" << setw(15) << "12.10" << endl;
    cout << setw(5) << "0120005" << setw(15) << "Toothpaste" << setw(15) << "6.75" << endl;
    cout << setw(5) << "0120006" << setw(15) << "Soap" << setw(15) << "5.20" << endl;
    cout << setw(5) << "0120007" << setw(15) << "Pen" << setw(15) << "2.00" << endl;
    cout << setw(5) << "0120008" << setw(15) << "Biscuits" << setw(15) << "4.45" << endl;
    cout << setw(5) << "0120009" << setw(15) << "Lamp" << setw(15) << "20.50" << endl;
    cout << setw(5) << "01200010" << setw(15) << "Battery" << setw(15) << "10.00" << endl;

    cout << endl;
    cout<<endl;
}

void showMessage(){
    // welcome message
    cout << "**************************************************" << endl;
    cout << "** WELCOME TO HERTS SUPERMARKET CHECKOUT SYSTEM **" << endl;
    cout << "**      Enter the barcode of the item           **" << endl;
    cout << "**************************************************" << endl;

}

int content()
{

    float total = 0.0;
    string barcode;
//the welcome message
    showMessage();
    Menu();


    //the barcode lists
    string barcodeList [10] = {"0120001", "0120002", "0120003", "0120004", "0120005", "0120006", "0120007", "0120008","0120009", "01200010"};


// until the user presses f do the following
	while(barcode != "f"){

	    //the message will be asked repeatedly for user input until it is f
            cout << "Enter a barcode (press f to exit): ";
			cin >> barcode;

			bool check = false;

			//below information checks whether the barcode is valid or invalid
			for (int i=0; i<10; i++){
                    // it compares the user input to the arrays stored in barcodeList.
                if(barcodeList[i]==barcode){

                    check=true;
                }
			}
			if (check) {
			    //if the barcode matches the arrays show this
                cout << "vaild barcode: " << barcode << endl;
			} else {
			    //if the barcode does not match the barcodeList array show this
                cout << "invaild barcode! Enter again:" << endl;
			}


			//below is if statements to check the barcode user input to each of the barcodeList one by one.
			//if it matches the total will be incremented each time
			if (barcode == barcodeList[0])
            {
                total+= 10.50;
            }
            else if (barcode == barcodeList[1] )
                {total+=5.50;
                }
            else if (barcode == barcodeList[2] )
                {total+=8.00;
                }
            else if (barcode == barcodeList[3] )
                {total+=12.10;
                }
             else if (barcode == barcodeList[4] )
                {total+=6.75;
                }
            else if (barcode == barcodeList[5] )
                {total+=5.20;
                }
            else if (barcode == barcodeList[6] )
                {total+=2.00;
                }
            else if (barcode == barcodeList[7] )
                {total+=4.45;
                }
            else if (barcode == barcodeList[8] )
                {total+=20.50;
                }
            else if (barcode == barcodeList[9] )
                {total+=10.00;
                }

		}
		//here is the total calculation
		float cash = 0.0;
		cout<< "" <<endl;
		cout << "your total is " << std::fixed << std::setprecision(2) << total << endl; // this shows the total
		cout << "cash: ";
		cin >> cash;
		cout << endl;
		float change1 = cash - total; // calculation for the change of the user cash - total.
		cout << "change: " << change1 << endl;

		//below if statement checks whether the cash given is enough for the total
		//otherwise it will ask for more cash and will return changes
		if(cash<total){
            cout << -change1 << " more needed :";
            float cash2;
            cin >> cash2;
            float change2 = cash2 + change1;
            cout <<"change: " << change2 << endl;
		}

    return 0;

}
int main()
{
    //the bool is used to repeat the program depending on the users input
    bool repeat = true;
    while (repeat)
    {
        //this presents all the information in content
        content();
        //then asks the user question
        cout << "Next Customer y/n: " << endl;
        char answer;
        cin >> answer;
        //if the user input is y then repeat the process as the bool will be true.
        repeat = answer == 'y';

    }
    //if the bool is false "in other word n" then exit the loop and show this.
    cout << "Thank you for shopping at Herts Store!!" << endl;

    return 0;
}

