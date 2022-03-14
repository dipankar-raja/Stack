# Stack
//Stack using Java
import java.io.*;
import java.util.Scanner;
class stack
{
   
        int top;
        int item[]=new int[10];
}

class stack1
{
   
   
    void push(stack ps,int x)
    {
            if(ps.top==9)
            {
                    System.out.println("\nSTACK OVERFLOW");
                   
            }
            else
            ps.item[++(ps.top)]=x;
    }
    int pop(stack ps)
    {
            if(ps.top==-1)
            {
                    System.out.println("\nSTACK UNDERFLOW");
                    return 0;
            }
            else
            return(ps.item[ps.top--]);
    }
    void display(stack s)
    {
            int k;
            System.out.println("\n\n\tOUTPUT==>>");
            for(k=s.top;k>0;k--)
            System.out.println("\t"+s.item[k]);
    }
}

class ds
{
    public static void main(String args[])
    {
        stack ps=new stack();
        stack1 s=new stack1();
        Scanner sc=new Scanner(System.in);
        //s.push(ps,2);
        int i,j,n=8;
        while(n>=0)
            {
                     System.out.println("\nPress 1 for push=");
                    System.out.println("\nPress 2 for pop=");
                    System.out.println("\nPress 3 for display=");
                   System.out.println("\nPress 4 for exit=");
                    System.out.println("\nEnter Choice=");
                    i=sc.nextInt();
               
                System.out.println("\n\n\t\t\t\t<<==STACK==>>\n\n");
                switch(i)
                {
                    case 1:    System.out.println("\nEnter element=");
                                j=sc.nextInt();
                               s.push(ps,j);
                               break;
                    case 2:     System.out.println("\nThe remove element is="+s.pop(ps));
                            break;
                    case 3:     s.display(ps);
                               break;
                   
                    default:System.out.println("\n\bWRONG CHOICE");
                    }
        n--;
        }
           

    }

}
