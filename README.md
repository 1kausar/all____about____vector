# all____about____vector

#include <iostream>
#include<bits/stdc++.h>
#include<vector>

using namespace std;

int main()
{

  vector<int>a; 
  /**************some element put in vector and print it****

  a.push_back(1);
  a.push_back(2);
  a.push_back(3);
  
 
 a[1]=100;
  
  for(int i=0 ; i<a.size() ; i++)
  {
      cout<<a[i]<<" ";
  }
  */////////////////////////////////////////////// 
  
 /********Taken input from User and print it********** 
  int n;
  cin>>n;
  for(int i=0 ; i<n ; i++)
  {
     int e;
     cin>>e;            //input from user;
     a.push_back(e);
  }
  //another proces of taking input from user::
  vector<int> v(size);
  for(int i=0 ; i<size ; i++)
  {
                       
      cin>>v[i];                 
 }
  
  // a.clear();     //clear vector
 // a.resize(10);   // vector resize
   vector<int> temp;
   temp=a;         // copy all element into temp vector
    for(int i=0 ; i<temp.size() ; i++)
  {
      cout<<temp[i]<<" ";
  }
  */////////////////////////////////////////////
  
  /********print vector usng etarater******
   
 int n;
  cin>>n;
  for(int i=0 ; i<n ; i++)
  {
     int e;
     cin>>e;            
     a.push_back(e);
  }


   vector<int>:: iterator temp; 
   

 for(temp=a.begin(); temp!=a.end() ; temp++)
 {
     cout<<*temp<<" ";
 }
 *//////////////////////////////
    
 /***************vector print using for each loop****
   
  int n;
  cin>>n;
  for(int i=0 ; i<n ; i++)
  {
     int e;
     cin>>e;            
     a.push_back(e);
  }
  for(auto u : a)
  {
      cout<<u<<" ";
  }
  
 */////////////////////////////////////////////////
 
 /******sort all element using sort()********
  
  
 int n;
  cin>>n;
  for(int i=0 ; i<n ; i++)
  {
     int e;
     cin>>e;            
     a.push_back(e);
  }
  sort(a.begin() , a.end());
    for(auto u : a)
  {
      cout<<u<<" ";
  }
  cout<<endl;
  cout<<"sort a paticular idext to index::"<<endl;
  sort(a.begin()+1 , a.end()+5);
  cout<<"after reverse a vector"<<endl;
  reverse(a.begin(),a.end());
  for(auto u : a)
  {
      cout<<u<<" ";
  }
  
  *////////////////////////////////////////////////////
  
 /******************** cps academy***********
  #include<bits/stdc++.h>
using namespace std;
int main ()
{
    vector<int> v;
 
    v.push_back( 1 );
    v.push_back( 2 );
    v.push_back( 3 );
 
    cout << v[0] << " " << v[1] << " " << v[2] << endl; /// 1 2 3
 
    v[1] = 3;
    cout << v[0] << " " << v[1] << " " << v[2] << endl; /// 1 3 3
 
    cout << v.size() << endl; /// 3
    for ( int i = 0; i < v.size(); i++ ) cout << v[i] << " "; /// 1 3 3
    cout << endl;
 
    vector <int> v1 = { 2, 3, 4 };
 
    cout << v1.size() << endl; /// 3
    for ( int i = 0; i < v1.size(); i++ ) cout << v1[i] << " "; /// 2 3 4
    cout << endl;
 
    v.clear();
    cout << v.size() << endl; /// 0
    cout << v.empty() << endl; /// 1
    cout << v1.empty() << endl; /// 0
 
    v1.resize(5);
    cout << v1.size() << endl; /// 5
    for ( int i = 0; i < v1.size(); i++ ) cout << v1[i] << " "; /// 2 3 4 0 0
    cout << endl;
 
    vector<int> a(5);
 
    cout << a.size() << endl; /// 5
    for ( int i = 0; i < a.size(); i++ ) cout << a[i] << " "; /// 0 0 0 0 0
    cout << endl;
 
    a = v1;
 
    for ( auto u : a ) cout << u << " "; /// 2 3 4 0 0
    cout << endl;
 
    vector<int>::iterator it;
    for ( it = a.begin(); it != a.end(); it++ ) cout << *it << " "; /// 2 3 4 0 0
    cout << endl;
 
    a = { 3, 4, 5, 1, 2 };
 
    sort ( a.begin(), a.end() ); ///O(n*log2(n))
 
    for ( auto u : a ) cout << u << " "; /// 1 2 3 4 5
    cout << endl;
 
    sort ( a.rbegin(), a.rend() );
 
    for ( auto u : a ) cout << u << " "; /// 5 4 3 2 1
    cout << endl;
 
 
    a = { 3, 4, 5, 1, 2 };
    sort ( a.begin(), a.end(), greater<int>() );
 
    for ( auto u : a ) cout << u << " "; /// 5 4 3 2 1
    cout << endl;
 
    a = { 3, 4, 5, 1, 2 };
 
    reverse( a.begin(), a.end() );
 
    for ( auto u : a ) cout << u << " "; /// 2 1 5 4 3
    cout << endl;
 
    cout << a.back() << endl; /// 3
    a.pop_back(); /// O(1) complexity.
    cout << a.back() << endl; /// 4
 
 
    a = { 3, 4, 5, 1, 2 };
    cout << *a.begin() << endl; /// 3
 
    a.erase( a.begin() ); /// O(n) complexity.
    for ( auto u : a ) cout << u << " "; /// 4 5 1 2
    cout << endl;
 
    a.erase( a.begin()+2 );
    for ( auto u : a ) cout << u << " "; /// 4 5 2
    cout << endl;
 
    a = { 1, 1, 2, 2, 2, 3, 3 };
    unique( a.begin(), a.end() );
 
    for ( auto u : a ) cout << u << " "; /// 1 2 3 2 2 3 3
    cout << endl;
 
 
    a = { 1, 1, 2, 2, 2, 3, 3 };
    int n = unique( a.begin(), a.end() ) - a.begin();
 
    cout << n << endl; /// 3
    for ( int i = 0; i < n; i++ ) cout << a[i] << " "; /// 1 2 3
    cout << endl;
 
    a = { 2, 3, 1, 5 };
    cout << max_element( a.begin(), a.end() ) - a.begin() << endl; /// 3
    cout << *max_element( a.begin(), a.end() ) << endl; /// 5
    
    *////////////////////////////////////////////////////
 
    return 0;
}
  

    return 0;
}
