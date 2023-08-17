# Welcome to GitHub Desktop!

This is your README. READMEs are where you can communicate what your project is and how to use it.

Write your name on line 6, save it, and then head back to GitHub Desktop.



Qno (1.) C++ Program to Find Largest Among Three Numbers

#include <iostream>

using namespace std;

int main()
{
    int a,b,c;
    cout<<"Enter the three numbers a ,b & c "<<endl;
    cin>>a>>b>>c;
    if (a>b && a>c){
        cout<<"Largest number is a="<<a<<endl;
        
    }
    else if(b>c && b>c){
        cout<<"Largest number is b="<<b<<endl;
    }
    else{
        cout<<"Largest number is c="<<c<<endl;
    }
    
}

Qno.(2) C++ Program To Find If A Character Is Vowel Or Consonant

#include <iostream>

using namespace std;

int main()
{
    char ch;
    cin>>ch;
    if (ch=='a'|| ch=='A'|| ch=='e'|| ch=='E'||
        ch=='i'|| ch=='I'|| ch=='o'|| ch=='O'||
        ch=='u'|| ch=='U'){
            cout<<"Given character is vowel"<<endl;
            
        }
        else{
            cout<<"Given character is consonant"<<endl;
        }
}

Qno.(3)  C++ program to print fibonacci series 

#include <iostream>

using namespace std;

int main()
{
    int n;
    cin>>n;
    int a=0;int b=1;
    cout<<a<<" "<<b<<" ";
    for(int i=0;i<=n;i++){
        int nextnumber=a+b;
        cout<<nextnumber<<" ";
        a=b;
        b=nextnumber;
    }
}

Qno.(4) C++ program to check whether a number is prime or not.

#include<iostream>
using namespace std;

int main() {
  int n;
  cin>>n;
bool isprime =true;
for(int i=2;i<n;i++){
    if(n%i==0){
        isprime=false;
        break;
    }
}
if(isprime==false){
    cout<<"Not prime"<<endl;
}
else{
    cout<<"is prime number"<<endl;
}
}


---->Alternative method to check whether a number is prime or not(using function)

#include<iostream>
using namespace std;

// Function check whether a number
// is prime or not
bool isPrime(int n)
{
	// Corner case
	if (n <= 1)
		return false;

	// Check from 2 to square root of n
	for (int i = 2; i <n; i++){
		if (n % i == 0)
			return false;
}
	return true;
}

// Driver Code
int main()
{
    int n;
    cout<<"Enter the number "<<endl;
    cin>>n;
	isPrime(n) ? cout << "yes it is prime \n" : cout << "No it is not prime \n";
	return 0;
}

Qno.(5) C++ program to check leap year .

#include<iostream>
using namespace std;
int main(){
    int year;
    cout<<"Enter the Year you want to check whether it is leap year or not "<<endl;
    cin>>year;
    if(year%400==0 || (year%100!=0 && year%4==0)){ //leap year ka matlab jo 4 ya 400 se divide ho jaye but for centuary year 100 se divide na ho 
        cout<<"Yes it is Leap Year "<<endl;

    }
    else{
    cout<<"No It's not a leap year"<<endl;
    }

}

Qno.(6) C++ program to print multiplication of table of n

#include<iostream>


using namespace std;
int main(){
    int n;
    cout<<"Enter the number ";
    cin>>n;
    
    for(int i=1;i<=10;i++){
            
            cout<<n*i<<endl;
    }
        
}

Qno.(7) C++ Program to Find the Sum of Natural Numbers.

#include<iostream>


using namespace std;
int main(){
    int n;
    cout<<"Enter the number ";
    cin>>n;
    int sum=0;
    for(int i=1;i<=n;i++){
            sum=sum+i;
            
    }
        cout<<"The sum of n Natural Number is "<<sum<<endl;
}

Qno(8). C++ Program To Find Factorial Of A Number.

#include<iostream>


using namespace std;
int main(){
    int n;
    cout<<"Enter the number ";
    cin>>n;
    int fact=1;
    for(int i=1;i<=n;i++){
           fact =fact*i;
            
    }
        cout<<"The factorial of n is "<<fact<<endl;
}
Qno.(9) C++ Program to Reverse Digits of a Number

#include<iostream>


using namespace std;
int main(){
    int n;
    cout<<"Enter the number ";
    cin>>n;
    int r=0;
    while(n>0){
           r=r*10;
           r=r+(n%10);
           
           n=n/10;
    }
        cout<<"The reversed number is "<<r<<endl;
}
							(or)
Qno.(10) Given a signed 32-bit integer x, return x with its digits reversed . If reversing x causes the value to go outside
the signed 32-bit integer range[-2^32, 2^32 -1] the return 0 Write a c++ program for this ......

#include<iostream>
#include <limits.h> // To use INT_MIN OR INT_MAX we use header file this 

using namespace std;
int main(){
    int n;
    cout<<"Enter the number ";
    cin>>n;
    int ans=0;
    while(n!=0){
           int digit=n%10;
           if( (ans>INT_MAX/10) || (ans<INT_MIN/10)){
            return 0;
           }
            ans=(ans*10) + digit;
            n=n/10;
    }
        cout<<ans<<endl;
}

---> GCD of Two Numbers in C++ (Using Euclid Algorithm easiest way to find gcd of any two natural number)

#include<iostream>
using namespace std;
int gcd(int a,int b){
    while(b!=0){
    int rem=a%b;
    a=b;
    b=rem;
}
return a;
}
int main(){
    int a,b;
    cout<<"Enter the two numbers ";
    cin>>a>>b;
    cout<<"The GCD of "<< a<<" " << b <<" is "<<gcd(a,b)<<endl;
    //cout<<gcd(a,b)<<endl;
    return 0;
}

---> C++ Program To Find LCM of Two Numbers (Using Euclid Algorithm easiest way to find gcd of any two natural number)

#include<iostream>
using namespace std;
int gcd(int a,int b){					
    while(b!=0){					----------------------------------------		
    int rem=a%b;					|        				|
    a=b;						|					|
    b=rem;						|					|
}					                |     // using formula a*b = lcm*hcf	|
return a;						|					|
}							|					|
int main(){						|					|
    int a,b,lcm;					|					|
    cout<<"Enter the two numbers ";			|---------------------------------------|
    cin>>a>>b;
    lcm=(a*b)/gcd(a,b);
    cout<<"The GCD of "<< a<<" " << b <<" is "<<lcm<<endl;
    //cout<<gcd(a,b)<<endl;
    return 0;
}

---> C++ Program to Check Whether a Number is Palindrome or Not 

#include<iostream>
using namespace std;
int main(){
 int n,temp;
 cout<<"Enter the number ";
 cin>>n;
 int ans=0;						//here i will use the concept of revere number "every palindrome is equallly when we take 
 temp=n;						reverse of it" ....
 while(n!=0){
    int digit =n%10;
    ans=(ans*10)+digit ;
    n=n/10;
    
 }
 cout<<ans<<endl;
    if (temp==ans){
        cout<<"yes It is a palindrome number "<<endl;
    }
    else 
    cout<<"Not a palindrome number "<<endl;
}

---> C++ program to make a mini Calculator using ("+,-,*,/,%)

#include <iostream>
using namespace std;

int main()
{
        int a,b;
        cout<<"Enter the value of a :"<<endl;
        cin>>a;
        
        cout<<"Enter the value of b :"<<endl;
        cin>>b;
        
        char op;
        cout<<"Enter the Operation you want to perform:"<<endl;
        cin>>op;
        
        switch(op){
            case '+': cout<<"The Value of a+b is :"<<(a+b)<<endl;
            break;
            
            case '-': cout<<"The value of a-b is : "<<(a-b)<<endl;
            break;
            
            case '*': cout<<"The Value of a*b is :"<<(a*b)<<endl;
            break;
            
            case '/': cout<<"The value of a/b is :"<<(a/b)<<endl;
            break;
            
            case '%': cout<<"The value of a%b is :"<<(a%b)<<endl;
            break;
            
            deafult : cout<<"Please Enter a Valid operation "<<endl;
            
            
        }
      return0;  
}


---> C++ program to calculate no. of notes required for an amount (100,50,20,10 notes )

#include<iostream>
using namespace std;

int main()
{
    int n;
    cin>>n;

    switch(1)
    {
        case 1 : if(n == 0) exit(0);
                 cout<<"no of 100 notes are "<<n/100<<endl;
                 n = n % 100;
        case 2 : if(n == 0) exit(0);
                 cout<<"no of 50 notes are "<<n/50<<endl;
                 n = n % 50;
        case 3 : if(n == 0) exit(0);
                 cout<<"no of 20 notes are "<<n/20<<endl;
                 n = n % 20;
        case 4 : if(n == 0) exit(0);
                 cout<<"no of 1 notes are "<<n/1<<endl;
                 n = n % 1;
    }
    return 0;
} 

---> C++ program to check whether a number is Even or Odd (using Function)

#include<iostream>
using namespace std;

bool isEven(int a){
    if(a%2==0){
        return 1;
    }
    else{
        return 0;
    }
}

int main()
{
    int num;
    cout<<"Enter the number you want to check  :"<<endl;
    cin>>num;
    
    if(isEven(num)){
        cout<<"Number is Even"<<endl;
        
    }
    else{
        cout<<"Number is Odd "<<endl;
    }
} 

--> C++ program to calculate nCr using function

#include<iostream>
using namespace std;

int factorial(int n){
    int fact=1;
    for(int i=1;i<=n;i++){
        fact =fact*i;
    }
    return fact;
}

int nCr(int n,int r ){
    int num=factorial(n);
    int denom=factorial(r)*factorial(n-r);
    return num/denom;
}
int main()
{
    int n,r;
    cin>>n>>r;
    cout<<"The value of nCr is "<<nCr(n,r)<<endl;
    return 0;
} 

--> C++ Program to print Number 1 to n using Functions 

#include <iostream>
using namespace std;

void printCounting(int n){
    for(int i=1;i<=n;i++){
        cout<< i <<" ";
        
    }
    
}

int main()
{
    int n;
    cout<<"Enter the number : "<<endl;
    cin>>n;
    printCounting(n);

    return 0;
}

--> C++ program to calculate the nth term using the concept of AP (Arithmetic Progression example=3n+7 )

#include <iostream>
using namespace std;

int nthTerm(int n){
    int ans=((3*n)+7);
    

    return ans;
}
int main()
{
    int n;
    cout<<"Enter the number :"<<endl;
    cin>>n;
    int answer =nthTerm(n);
    cout<<"The nth term of the given AP 3n+7 is : "<<answer<<endl;

    return 0;
}

--> C++ program to calculate no. of Digits in a given Number (Using Function)

#include <iostream>
using namespace std;

int countDigit(int n)
{
	if (n == 0)
		return 1;
	int count = 0;
	while (n != 0) {
		n = n / 10;
		++count;
	}
	return count;
}


int main()
{
    	int n;
    	cout<<"Enter the number you want to check :"<<endl;
    	cin>>n;
	
	cout << "Number of digits : " << countDigit(n);
	return 0;
}

--> C++ program to find the Nth Fibonacci number (example for n=5 answer is 3 using 0,1,1,2,3,5,8,13........)

#include <iostream>
using namespace std;

int fib(int n)
{
	int a = 0, b = 1, c, i;
	if (n == 1)
		return 0;
	for (i = 2; i < n; i++) {
		c = a + b;
		a = b;
		b = c;
	}
	return b;
}


int main()
{
	int n;
	cout<<"Enter the nth term of Fibonacci Series which you want to diplay :";
	cin>>n;
    
	cout <<"The "<< n <<"th term is :"  <<fib(n);
	return 0;
}

--> 







