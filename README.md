# project-1
#include<iostream>
#include<string>
using namespace std;
struct product
{
	string name;
	long code;
	float first_price;
	float second_price;
	int quntity;
	int discount;
};
void print_arry(product x[], int y)
{
	for (int i = 0; i < y; i++)
	{
		cout << "product name is " << x[i].name << endl;
		cout << "product code " << x[i].code << endl;
		cout << "product buy price =" << x[i].first_price << endl;
		cout << "product sell price =" << x[i].second_price << endl;
		cout << "product quantity =" << x[i].quntity << endl;
		cout << "product discount =" << x[i].discount <<"%" << endl;
	}
}
void get_name(product x[],int y)
{
	string name;
	cout << "enter searsh name"<< endl;
	cin >> name;
	for (int i = 0; i < y; i++)
	{
		if(x[i].name == name)
		{
			cout << "found"<<endl;
			cout << "product name is " << x[i].name << endl;
			cout << "product code " << x[i].code << endl;
			cout << "product buy price " << x[i].first_price << endl;
			cout << "product sell price =" << x[i].second_price << endl;
			cout << "product quantity =" << x[i].quntity << endl;
			cout << "product discount =" << x[i].discount << "%" << endl;
		}
	}
}
void code_searsh(product x[],int y) 
{
	long code;
	cout << "enter searsh code"<< endl ;
	cin >> code ;
	for (int i = 0; i < y; i++)
	{
		if (x[i].code == code)
		{
			cout << "found"<< endl;
			cout << "product name is " << x[i].name << endl;
			cout << "product code " << x[i].code << endl;
			cout << "product buy price " << x[i].first_price << endl;
			cout << "product sell price =" << x[i].second_price << endl;
			cout << "product quantity =" << x[i].quntity << endl;
			cout << "product discount =" << x[i].discount << "%" << endl;
		}
		
	}
}
void profit(product x[], int y) 
{
	int prof = 0;
	int total_prof;
	for (int i = 0; i < y; i++) 
	{
		prof = x[i].second_price - x[i].first_price;
		total_prof = prof * x[i].quntity;

		cout << "product name is " <<x[i].name << endl;
		cout << "product code "<<x[i].code << endl;
		cout << "product buy price " << x[i].first_price << endl;
		cout << "product sell price" << x[i].second_price << endl;
		cout << "product quantity" << x[i].quntity << endl;
		cout << "product discount =" << x[i].discount << "%" << endl;
		cout << "total profit = " << total_prof << endl;
	}
	
}
void updateinfo(product  x[] , int y) 
{
	for (int i = 0; i > -1; i++)
	{
		int choise;
		cout << "to update name plz enter 1     " << endl;
		cout << "to update code plz enter 2     " << endl;
		cout << "to update buy pice plz enter 3 " << endl;
		cout << "to update sell pice plz enter 4" << endl;
		cout << "to update quntity plz enter 5  " << endl;
		cout << "to update discount plz enter 6 " << endl;
		cout << "to exit enter 7                " << endl;
		cin >> choise;

		string oldname;
		 switch(choise)
		 {
		 case 1:
			 
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new name " << endl;
					 cin >> x[i].name;
				 }

			 }
			
			break;

		 case 2:
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new code  " << endl;
					 cin >> x[i].code;
				 }

			 }

			 break;

		 case 3:
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new buy price  " << endl;
					 cin >> x[i].first_price;
				 }

			 }

			 break;

		 case 4:
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new sell price  " << endl;
					 cin >> x[i].second_price;
				 }

			 }

			 break;

		 case 5:
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new quntity " << endl;
					 cin >> x[i].quntity;
				 }

			 }

			 break;

		 case 6:
			 cout << "plz enter name to search for" << endl;
			 cin >> oldname;
			 for (int i = 0; i < y; i++)
			 {
				 if (oldname == x[i].name)
				 {
					 cout << "enter new discount " << endl;
					 cin >> x[i].discount;
				 }

			 }

			 break;

		 case 7:
			 i = -2;

		default:
			cout << "plz enter number from 1 to 7 " << endl;
			break;
		 }
	}
}

int main() 
{
	const int size = 3;
	product x[size];
	cout << "plz fill the array"<< endl;
	for (int i = 0; i < size; i++)
	{
		cout << "plz enter name"<< endl;
		cin >> x[i].name;
		cout << "plz enter code" << endl;
		cin >> x[i].code;
		cout << "plz enter first price" << endl;
		cin >> x[i].first_price;
		cout << "plz enter sell price" << endl;
		cin >> x[i].second_price;
		cout << "plz enter quntity" << endl;
		cin >> x[i].quntity;
		cout << "plz enter discount" << endl;
		cin >> x[i].discount;
	}
	
	for (int i = 0; i > -1; i++)
	{	int n;
		cout << "to print array plz enter 1    " << endl;
		cout << "to search by name plz enter 2 " << endl;
		cout << "to srearch by code plz enter 3" << endl;
		cout << "to find the profit plz enter 4" << endl;
		cout << "to update info plz enter 5    " << endl;
		cout << "to exit enter 6               " << endl;
		cin >> n;
			switch (n)
			{
			case 1:
				print_arry(x, size);
				break;

			case 2:
			get_name(x , size);
			break;

			case 3:
			code_searsh(x , size);
			break;

			case 4:
				profit(x, size);
			break;

			case 5:
				updateinfo(x, size);
				break;

			case 6:
			return 0;

			
			default:
			cout << "plz enter number from 1 to 4 "<< endl;
			break;

			}
	}	
	return 0;
	
}
