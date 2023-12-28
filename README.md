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
}
