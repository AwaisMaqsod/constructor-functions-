//# constructor-functions-
//constructor and functions of parent class accessing in child class by inheritance,Oop c++. 
// inhertance constructor and function accessing 
#include<iostream>
#include<string>
using namespace std;
class Teacher{
	private:
		string name_OfTeacher;
		int teacher_id;
		char code_word;
	public:
		
		Teacher (char x, int y){//parametrise construstor
			code_word=x;
			teacher_id=y;
	 		cout<<"Enter Teacher's name : "<<endl;
            getline(cin,name_OfTeacher);
}
         void show_DT(){
         	cout<<". "<<name_OfTeacher<<endl;
         	cout<<".. "<<code_word<<endl;
         	cout<<"... "<<teacher_id<<endl;
       }};
class student:public Teacher{
private:
	string name;
	char s_code;
	public:
		student(char z,char m, int n):Teacher(m,n){
			s_code=z;
		cout<<"Enter the name of student : "<<endl;
		cin>>name;
			
		}
		void show_DS(){
			Teacher::show_DT();
			cout<<", "<<s_code<<endl;
            cout<<",, "<<name<<endl;
		}
	
};


int main(){

student s1('s','t',2080245);
s1.show_DS();
 	
	
	return 0;
}
