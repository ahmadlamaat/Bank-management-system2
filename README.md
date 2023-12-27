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
