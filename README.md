case 2:
		cout<<"enter daily spending limit : ";
		cin>>dailySpendingLimit;
		cout<<"enter weekly spending limit : ";
		cin>>weeklySpendingLimit;
		break;

  oid deposit() 
{
	double amount;
	cout<<"enter amout to be deposited : ";
	cin>>amount;
    if (amount > 0) {
            initialBalance1 = initialBalance1 + amount;
        cout << "Deposit successful. Current balance: " << initialBalance1 << endl;
    } else {
        cout << "Invalid deposit amount. Please enter a positive value." << endl;
    }
} 

void withdraw(double amount) {
    if (amount > 0 && amount <= initialBalance1 && amount <= dailySpendingLimit) {
        initialBalance1 = initialBalance1 - amount;
        cout << "Withdrawal successful. Current balance: " << initialBalance1 << endl;
        dailySpendingLimit -= amount;
        weeklySpendingLimit -= amount;
    } else if (amount <= 0) {
        cout << "Invalid withdrawal amount. Please enter a positive value." << endl;
    } else if (amount > initialBalance1) {
        cout << "Insufficient funds for withdrawal. Current balance: " << initialBalance1 << endl;
    } else {
        cout << "Exceeded daily spending limit. Current daily limit: " << dailySpendingLimit << endl;
    } 


    #include<iostream>
#include<string>
using namespace std;

double initialBalance1;
double dailySpendingLimit;
double weeklySpendingLimit;
int password[4];

void displayAccount(string &accountHolder, int accountNumber, double balance)
{
    cout << " Account Holder: " << accountHolder << endl;
    cout << " Account Number: " << accountNumber << endl;
    cout << " Balance: Rs" << balance << endl;
    cout<<endl;
}


int savingsacc()
{
    int selection, deposit=0, finalamount = 0;
    cout<<"  ------------------------------------SELECT A PACKAGE------------------------------------"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"  --------------------------------------1 YEAR PLANS-------------------------------------- "<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"1. 50000-70000 deposit, 5% interest"<<endl;
    cout<<"2. 70000-100000 deposit, 10% interest"<<endl;
    cout<<"3. 100000-150000 deposit, 12% interest"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"  --------------------------------------2 YEAR PLANS--------------------------------------"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"4. 50000-70000 deposit, 5% interest"<<endl;
    cout<<"5. 70000-100000 deposit, 10% interest"<<endl;
    cout<<"6. 100000-150000 deposit, 12% interest"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"  --------------------------------------5 YEAR PLANS--------------------------------------"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<"7. 50000-70000 deposit, 5% interest"<<endl;
    cout<<"8. 70000-100000 deposit, 10% interest"<<endl;
    cout<<"9. 100000-150000 deposit, 12% interest"<<endl<<endl;
    cout<<"  ----------------------------------------------------------------------------------------"<<endl;
    cout<<" Select an option : ";
    cin>>selection;
    cout<<endl;
    switch(selection)
{
    case 1:
    while(deposit<50000 || deposit>70000)
    {
        cout<<"enter desired deposit (50000-70000) : ";
        cin>>deposit;
        if(deposit<50000 || deposit>70000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (0.05*deposit);
    cout<<"your final amount at end of 1 year is : "<<finalamount;
    break;

    case 2:
    while(deposit<70000 || deposit>100000)
    {
        cout<<"enter desired deposit (70000-100000) : ";
        cin>>deposit;
        if(deposit<70000 || deposit>100000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (0.1*deposit);
    cout<<"your final amount at end of 1 year is : "<<finalamount;
    break;

    case 3:
    while(deposit<100000 || deposit>150000)
    {
        cout<<"enter desired deposit (100000-150000) : ";
        cin>>deposit;
        if(deposit<100000 || deposit>150000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (0.12*deposit);
    cout<<"your final amount at end of 1 year is : "<<finalamount;
    break;

    case 4:
    while(deposit<50000 || deposit>70000)
    {
        cout<<"enter desired deposit (50000-70000) : ";
        cin>>deposit;
        if(deposit<50000 || deposit>70000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (2*(0.05*deposit));
    cout<<"your final amount at end of 2 year is : "<<finalamount;
    break;

    case 5:
    while(deposit<70000 || deposit>100000)
    {
        cout<<"enter desired deposit (70000-100000) : ";
        cin>>deposit;
        if(deposit<70000 || deposit>100000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (2*(0.1*deposit));
    cout<<"your final amount at end of 2 year is : "<<finalamount;
    break;

    case 6:
    while(deposit<100000 || deposit>150000)
    {
        cout<<"enter desired deposit (100000-150000) : ";
        cin>>deposit;
        if(deposit<100000 || deposit>150000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (2*(0.12*deposit));
    cout<<"your final amount at end of 2 year is : "<<finalamount;
    break;

    case 7:
    while(deposit<50000 || deposit>70000)
    {
        cout<<"enter desired deposit (50000-70000) : ";
        cin>>deposit;
        if(deposit<50000 || deposit>70000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (5*(0.05*deposit));
    cout<<"your final amount at end of 1 year is : "<<finalamount;
    break;

    case 8:
    while(deposit<70000 || deposit>100000)
    {
        cout<<"enter desired deposit (70000-100000) : ";
        cin>>deposit;
        if(deposit<70000 || deposit>100000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (5*(0.1*deposit));
    cout<<"your final amount at end of 2 year is : "<<finalamount;
    break;

    case 9:
    while(deposit<100000 || deposit>150000)
    {
        cout<<"enter desired deposit (100000-150000) : ";
        cin>>deposit;
        if(deposit<100000 || deposit>150000)
        {
            cout<<"invalid input"<<endl;
        }
    }
    finalamount = deposit + (5*(0.12*deposit));
    cout<<"your final amount at end of 2 year is : "<<finalamount;
    break;

}
}


void deposit() 
{
	double amount;
	cout<<"enter amout to be deposited : ";
	cin>>amount;
    if (amount > 0) {
            initialBalance1 = initialBalance1 + amount;
        cout << "Deposit successful. Current balance: " << initialBalance1 << endl;
    } else {
        cout << "Invalid deposit amount. Please enter a positive value." << endl;
    }
}

void withdraw(double amount) {
    if (amount > 0 && amount <= initialBalance1 && amount <= dailySpendingLimit) {
        initialBalance1 = initialBalance1 - amount;
        cout << "Withdrawal successful. Current balance: " << initialBalance1 << endl;
        dailySpendingLimit -= amount;
        weeklySpendingLimit -= amount;
    } else if (amount <= 0) {
        cout << "Invalid withdrawal amount. Please enter a positive value." << endl;
    } else if (amount > initialBalance1) {
        cout << "Insufficient funds for withdrawal. Current balance: " << initialBalance1 << endl;
    } else {
        cout << "Exceeded daily spending limit. Current daily limit: " << dailySpendingLimit << endl;
    }
}



int transfer(int &amount)
 {
    int bank;
	char name;	
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  1. HBL"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  2. JBL"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  3. Ishfaq Bank"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  4. Rana Bank"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  5. MetroBoomin Bank"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
 	cout<<"  Choose the bank : "<<endl;
 	cin>>bank;
 	switch(bank)
 	{
 		int ibn, pintransfer;
 		char surechoice;
 		case 1: 
 		cout<<"Enter IBAN of the reciever:"<<endl;
 		cin>>ibn;
 		cout<<"Do you want to proceed with the transaction ? (y/n) : ";
 		cin>>surechoice;
 		if(surechoice == 'y')
 		{
 			cout<<"transfer successful";
 			
			                 
 			
		 }
		 else if (surechoice == 'n')
		 {
		 	cout<<"transaction cancelled";
		 }
		 else
		 {
		 	cout<<"invalid input";
		 }
		
 		break;
 		case 2: 
 		cout<<"Enter IBAN of the reciever:"<<endl;
 		cin>>ibn;
 		cout<<"Do you want to proceed with the transaction ? (y/n) : ";
 		cin>>surechoice;
 		if(surechoice == 'y')
 		{
 			cout<<"transfer successful";
 			
		 }
		 else if (surechoice == 'n')
		 {
		 	cout<<"transaction cancelled";
		 }
		 else
		 {
		 	cout<<"invalid input";
		 }
		
 		break;
 		case 3: 
 		cout<<"Enter IBAN of the reciever:"<<endl;
 		cin>>ibn;
 		cout<<"Do you want to proceed with the transaction ? (y/n) : ";
 		cin>>surechoice;
 		if(surechoice == 'y')
 		{
 			cout<<"transfer successful";
 			
		 }
		 else if (surechoice == 'n')
		 {
		 	cout<<"transaction cancelled";
		 }
		 else
		 {
		 	cout<<"invalid input";
		 }
		
 		case 4: 
 		cout<<"Enter IBAN of the reciever:"<<endl;
 		cin>>ibn;
 		cout<<"Do you want to proceed with the transaction ? (y/n) : ";
 		cin>>surechoice;
 		if(surechoice == 'y')
 		{
 			cout<<"transfer successful";
 			
		 }
		 else if (surechoice == 'n')
		 {
		 	cout<<"transaction cancelled";
		 }
		 else
		 {
		 	cout<<"invalid input";
		 }
		
 		break;
 		case 5: 
 		cout<<"Enter IBAN of the reciever:"<<endl;
 		cin>>ibn;
 		cout<<"Do you want to proceed with the transaction ? (y/n) : ";
 		cin>>surechoice;
 		if(surechoice == 'y')
 		{
 			cout<<"transfer successful";
 			
		 }
		 else if (surechoice == 'n')
		 {
		 	cout<<"transaction cancelled";
		 }
		 else
		 {
		 	cout<<"invalid input";
		 }
		
 		break;
	}
	
 }

 int billpay()
{
	  int option;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  Types of Bill Payments"<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  1. Internet Bill Payment."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  2. Electricity Bill Payment."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  3. Gas Bill Payment."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  4. Mobile Topup."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  5. M-tag Payment."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  6. Donation."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  7. Taxation."<<endl;
	  cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	  cout<<"  select an option"<<endl;
	cin>>option;

	switch(option)
	{
		case 1:
			int option1;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  1. Stormfiber"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  2. PTCL"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  3. Transworld"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  4. wateen"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  5. Qubee"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  Chose your internet operator"<<endl;
			cin>>option1;
			switch(option1)
			{
				int amount;
				case 1:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
			    case 2:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
				case 3:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
				case 4:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
				case 5:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
		   }
		break;
		case 2:
			int amount;
			cout<<"Enter the Amount of Bill you want to pay: "<<endl;
			cin>>amount;
			cout<<amount<<"has been successfully paid!"<<endl;
			initialBalance1 = initialBalance1 - amount;
		break;
		case 3:
		    
			cout<<"Enter the Amount of Bill you want to pay: "<<endl;
			cin>>amount;
			cout<<amount<<"has been successfully paid!"<<endl;
			initialBalance1 = initialBalance1 - amount;
		break;
		case 4:
		    int option;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  1. Telenor"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  2. Ufone"<<endl;	
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  3. Jazz"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  4. ZONG"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
			cout<<"  5. Mobilink"<<endl;
			cout<<"  ----------------------------------------------------------------------------------------"<<endl;
		    cout<<"  Select your Mobile phone operator : "<<endl;
			cin>>option;
			switch(option)
			{
			     	case 1:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
					case 2:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
					case 3:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
					case 4:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
					case 5:
					
					cout<<"Enter the amount you want to pay: "<<endl;
					cin>>amount;
					cout<<amount<<"has been successfully paid!"<<endl;
					initialBalance1 = initialBalance1 - amount;
					break;
					
				}	
		break;
		case 5:
			
    	cout<<"Enter the amount you want to pay: "<<endl;
		cin>>amount;
		cout<<amount<<"has been successfully paid!"<<endl;
		initialBalance1 = initialBalance1 - amount;
		break;
		case 6:
					
		cout<<"Enter the amount you want to donate "<<endl;
		cin>>amount;
		cout<<amount<<"has been successfully paid!"<<endl;
		initialBalance1 = initialBalance1 - amount;
		break;
		case 7:
					
		cout<<"Enter the amount of tax you want to pay: "<<endl;
		cin>>amount;
		cout<<amount<<"has been successfully paid!"<<endl;
		initialBalance1 = initialBalance1 - amount;
	    break;
	    					
								
	}
	
	  
}

int main()
{
	int opt1, amount;
	while(opt1 !=3)
	{
	
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  1. Create an account"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  2. Log into existing account"<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  3. Next menu "<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  choose an option : ";
	cin>>opt1;
	cout<<endl;
	if(opt1==1)
	{
	string holdername1;
    int accountNumber1;

    cout << "Enter account holder name: ";
    cin>>holdername1;

    cout << "Enter allotted account number: ";
    cin >> accountNumber1;

    cout << "Set a 4-digit pin for your account: ";
    for(int s=0;s<4;s++)
	{
		cin>>password[s];
	}

    cout << "Enter initial balance: ";
    cin >> initialBalance1;

    cout << "\nAccount created successfully. "<<endl<<"Details : "<<endl;
    displayAccount(holdername1, accountNumber1, initialBalance1);
	}


	else if(opt1==2)
	{
	string holdername2;
    int accountNumber2;
	int password2[4];
	cout << "Enter account holder name: ";
    cin>>holdername2;
    
    cout << "Enter allotted account number: ";
    cin >> accountNumber2;
    
    cout << "Enter 4 digit account pin : ";
	for(int t=0;t<4;t++)
	{
		cin>>password2[t];
	}
	int u=0;
	bool f=true;
	for(u=0;u<4;u++)
	{
    if(password2[u] != password[u])
    {
		f=false;
	}
	}
	if (f==true)
	{
		cout<<"correct pin"<<endl<<endl;
	}
	else
	{
		cout<<"Incorrect pin"<<endl<<endl;
	}
	

	}
	else if(opt1 == 3)
	{
		break;
	}
}

int opt2=0;
while(opt2 != 8)
{
	cout<<endl;
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  1. Start savings account \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  2. Set daily spending limit \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  3. Deposit money \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  4. Withdraw money \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  5. Transfer money \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  6. Bill payments \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  7. Check balance \n";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  8 Exit \n ";
	cout<<"  ----------------------------------------------------------------------------------------"<<endl;
	cout<<"  Choose an option : ";
	cin>>opt2;
	cout<<endl;

	int pin[4];

	switch(opt2)
	{

		case 1:
		savingsacc();
		break;

		case 2:
		cout<<"enter daily spending limit : ";
		cin>>dailySpendingLimit;
		cout<<"enter weekly spending limit : ";
		cin>>weeklySpendingLimit;
		break;

		case 3:
		deposit();
		break;

		case 4:
		{
		double fundswithdraw;
		cout<<"Enter password : ";
		for(int v=0;v<4;v++)
	{
		cin>>pin[v];
	}
	bool nn=true;
	for(int w=0;w<4;w++)
	{
    if(pin[w] != password[w])
		{
		nn=false;
		}
		if(nn==true)
		{
		cout<<"enter amount to withdraw : ";
		cin>>fundswithdraw;
		initialBalance1 = initialBalance1 - fundswithdraw;
		withdraw(fundswithdraw);
		}
		else
		{
			cout<<"incorrect pin";
		}
	}
		}
		break;
	

		case 5:
		{
		{
		cout<<"Enter password : ";
		for(int g=0;g<4;g++)
	{
		cin>>pin[g];
	}
	bool jj=true;
	for(int l=0;l<4;l++)
	{
    if(pin[l] != password[l])
		{
		jj=false;
		}
	}
	if(jj==true)
	{
		cout<<"enter amount to transfer : ";
		cin>>amount;
		transfer(amount);
		initialBalance1=initialBalance1-amount;
	}

		}
		break;

		case 6:
		{
		bool hh=true;
		cout<<"Enter password : ";
		for(int b=0;b<4;b++)
	{
		cin>>pin[b];
	}
	for(int y=0;y<4;y++)
	{
    if(pin[y] != password[y])
		{
			hh=false;
		}
	}
	if(hh == true)
	{
		billpay();
	}
	else
	{
		cout<<"Wrong Password\n";
	}
		}
		break;


		case 7:
		{
		cout<<"Enter password : ";
		for(int q=0;q<4;q++)
	{
		cin>>pin[q];
	}
	bool bb=true;
	for(int bb=0;bb<4;bb++)
	{
    if(pin[bb] != password[bb])
		{
		bb=false;
		}
	}
	if(bb==true)
	{
		cout<<"correct password"<<endl;
		cout<<"Balance = "<<initialBalance1<<endl<<endl;
	}
	else
	{
		cout<<"Incorrect pin"<<endl<<endl;
	}

		}
		break;




	}
	
}

	}
	cout<<"Exited";
}


}
