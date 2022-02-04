/* Write a C++ program to create an array of pointers. Invoke functions using array objects.*/
#include<iostream>
using namespace std;
class sample
{
    char c;
    public:
    void read()
    {
        cout<<"Enter a character ";
        cin>>c;
    }
    void display()
    {
        cout<<"Character : "<<c<<endl;
    }
};
int main()
{
    int i;
    sample *ptobj;
    sample obj;
    
    ptobj = new sample[5];
    obj.read();
    obj.display();
    cout<<"Calling the function using pointer object"<<endl;
    for(i=0;i<5;i++)
    {
        ptobj->read();
        ptobj->display();
    }
    return 0;
}
