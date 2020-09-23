# function_ovl
#include <iostream>
#include <string>
#include <iomanip>
using namespace std;
void DisplayMenu();
float Area(const float radius);
float Area(const float width, float height);
float Area(double based, double high);
int main()
{
	char Choice;
	bool Flag = true;
	do
	{
		DisplayMenu();
		cin>>Choice;
	if(Choice == '1'){
		float radius;
		cout<<"\nEnter radius : ";
		cin >> radius;
		cout<<"Area of Circle = " << fixed;
		cout<<setprecision(2)<<Area(radius)<<endl;
	}
	else if (Choice == '2'){
		float width, height;
		cout<<"\nEnter width and height : ";
		cin>>width>>height;
		cout<<"Area of Rectangle = " << fixed;
		cout<<setprecision(2)<<Area(width, height)<<endl;
		cout<<endl;
	}
	else if (Choice == '3'){
		float based, high;
		cout<<"\nEnter based and high : ";
		cin>>based>>high;
		cout<<"Area of Triangle = " << fixed;
		cout<<setprecision(2)<<Area(based, high)<<endl;
		cout<<endl;
	}
	else if (Choice == '4') Flag = false;
	else {
		cout<<"\nYou choose out of rangs is ";
		cout<<"not process.\n";
	 }
	} while(Flag);
	cout<<"\nExit\n";

	return 0;
}
float Area(const float radius)
{
	return(3.14159F * radius * radius);
}
float Area(const float width, float height)
{
	return(width * height);
}
float Area(double based, double high)
{
	return( 0.5 * based * high);
}
void DisplayMenu()
{
	cout<<endl;
	cout<<"Program Calculate Area"<<endl;
	cout<<"1.Circle"<<endl;
	cout<<"2.Rectangle"<<endl;
	cout<<"3.Triangle"<<endl;
	cout<<"4.Exit"<<endl;
	cout<<"Enter your choose number : ";

}
