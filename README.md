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
        // code for option written by another member
        }
	if(opt1==2)
        {
	//code for option written by another member
        }
	if(opt==3)
        {
	break;
        }
