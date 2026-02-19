[Program-1  Program to find Factorial](#assi-1)

[Program-2  Program to check armstrong number](#assi-2)

## assi-1
```
# 
package com.mycompany.pilani;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */

/**
 *
 * @author IBM17
 */
  import java.util.Scanner;
public class FactorialMain{ public static void main(String []args)
{Factorial f=new Factorial();
f.input();
f.output();
}}
class Factorial{
    int num;
    int facto;
    int fact(int num)
    {
        if(num==0 ||num==1)
        {
            return 1;
        }
        else
        return num*fact(num-1);
    }
    void input()
    {Scanner sc=new Scanner(System.in);
    System.out.println("enter number: ");
    num=sc.nextInt();
    facto=fact(num);
    }
    void output()
    {
      System.out.println("factorial is   "+facto);
    }
}
    
```
<img width="797" height="453" alt="image" src="https://github.com/user-attachments/assets/ab6cd1ff-fbb7-4e5e-8c41-7c344fc0c7c8" />

## assi-2
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package com.mycompany.pilani;

import java.util.Scanner;

/**
 *
 * @author IBM17
 */

public  class ArmMain 
{       public static void main(String args[])
        {Armnocheck a1= new Armnocheck();
        a1.input();
        a1.isarm();
        }
}
class Armnocheck
{
   int num;
   void isarm()
   {    int digits= countd(num);
        if(armsum(num,digits)==num)
            System.out.println(" no is armstrong");
        else
            System.out.println(" no isnot armstrong");
    }
   void input()
     { Scanner sc=new Scanner(System.in);
       System.out.println("enter a no:");
       num=sc.nextInt();
     }
   int countd(int num)
       {
           if(num==0)
                return 0;
           return 1+countd(num/10);
       }
   int armsum(int num,int digits)
       {
           if(num==0)
                return 0;
           return (int)Math.pow(num%10,digits)+armsum(num/10,digits);
        }
}

```
<img width="795" height="482" alt="image" src="https://github.com/user-attachments/assets/b71caddd-08ec-4204-8ddf-8a32ab86ef6c" />

