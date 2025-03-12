# Stack
this repo contain all the codes related to stack  <br>
Author-Raksha Shrimanwar
<br>
1.Stack implementation through array
<br>

#include<iostream>
using namespace std;
class Stack{
    public:
    
    int top;
    int *arr;
    int size;

   
    Stack(int size)
    {
        this->size=size;
        arr=new int (size);
        top=-1;
    }

    void push(int element)
    {
        if(size-top>1)
        {
            top++;
            arr[top]=element;
        }
        else{
            cout<<"stack overflow"<<endl;
        }
    }

    void pop()
    {
        if(top>=0)
        {
            top--;
        }
        else{
            cout<<"stack underflow"<<endl;

        }
    }

    void peek()
    {
        if(top>=0)
        {
            cout<<"topmost element of the stack is:"<<arr[top]<<endl;

        }
        else{
            cout<<"your stack is empty"<<endl;
        }
    }

    bool isEmpty()
    {
        if(top>=0)
         {return false;}
        else{
            return true;
        }

    }
};
int main()
{
    Stack st(5);
    st.push(23);
    st.push(200);
    st.push(12);
    st.push(1);

    st.peek();

    st.pop();
    st.pop();

    st.peek();

   if(st.isEmpty())
   {
       cout<<"stack is empty"<<endl;
   }
   else{
    cout<<"stack is not empty"<<endl;
   }
    
    return 0;
}

