#include<iostream>
using namespace std;
class bank_account{
    private:
    string name;
    int acc_no;
    string acc_type; //saving,current etc.
    int balance;
    public:
    void setDetails(string name,int acc_no,string acc_type,int balance){
        this->name=name;
        this->acc_no= acc_no;
        this->acc_type= acc_type;
        this->balance= balance;
    }
    int bal;
    void deposit(int x){
        bal= balance + x;
        cout<<"Balance of the account after depositing the money:"<< bal <<endl;
    }
    void withdraw(int y){
        if(balance> 100){
            bal=balance - y;
            cout<<"Balance of the account after withdrawing the money:"<< bal <<endl;
        }
    }
    void display(){
        cout<<"Name: "<<name<<endl<<"Balance: "<<bal;
    }
};
int main(){
    bank_account b;
    b.setDetails("Aishna",2318240,"Saving",2300);
    int x;
    cout<<"Enter aamount to be deposited: ";
    cin>>x;
    b.deposit(x);
    int y;
    cout<<"Enter amount to be withrawn: ";
    cin>>y;
    b.withdraw(y);
    b.display();
}
