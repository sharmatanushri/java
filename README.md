[Program-1  Program to find Factorial](#assi-1)

[Program-2  Program to check armstrong number](#assi-2)

[Program-3  Program to perform arithmatic operation on numbers using classes and objects](#assi-3)

[Program-4  Program to perform addition of distances where each distance is given in m,cm,mm(test result in  by creation of object in main class](#assi-4)

[Program-5  Program to perform addition of distances where each distance is given in m,cm(test result in  by creation of object in main class](#assi-5)

[Program-6  Program to perform addition of times where each time is given in hr,min,sec(test result in  by creation of object in main class](#assi-6)



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

## assi-3
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package com.mycompany.pilani;

import java.util.Scanner;

/**
 *
 * @author IBM17
 */
public class ArithmaticOpNo {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        calc obj=new calc();
        obj.input();
        obj.calculate();
        obj.output();
         
    }
    
}

class calc
{   int a,b;
    int sum,sub,mult;
    double div;
    void input()
    {
        Scanner sc=new Scanner(System.in);
        System.out.println("ENTER 1ST OPERAND:");

        a=sc.nextInt();
        System.out.println("ENTER 2nd OPERAND:");
        b=sc.nextInt();
        
    }
    void calculate()
    {
        sum=a+b;
        sub=a-b;
        mult=a*b;
        div=(double)a/b;
    }
    
    void output()
    {
        System.out.println("Addition = " + sum);
        System.out.println("Subtraction = " + sub);
        System.out.println("Multiplication = " + mult);
        System.out.println("division = " + div);
    }
}
```
<img width="746" height="350" alt="image" src="https://github.com/user-attachments/assets/2cc592d7-2105-4133-8303-5b686da8f28a" />

## assi-4
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package com.mycompany.pilani;

import java.util.Scanner;



/**
 *
 * @author IBM17
 */
public class dis_main {

    public static void main(String[] args) {
        System.out.println("Hello World!");
        Dist o1=new Dist();
        Dist o2=new Dist();
        Dist o3=new Dist();
        o1.input();
        o2.input();
        o1.generalise();
        o2.generalise();

        o3.add(o1,o2);
        o3.generalise();
        o3.output();
    }
}

class Dist{
    int m;
    int cm;
    int mm;
     void input(){
         Scanner sc=new Scanner(System.in);
         System.out.println(" Enter mtr");
         m=sc.nextInt();
         System.out.println(" Enter cm");
         cm=sc.nextInt();
         System.out.println(" Enter mm");
         mm=sc.nextInt();
         
         
     }
     
    void output(){
         System.out.println(" mtr="+m);
         System.out.println(" cm="+cm);
          System.out.println(" mm="+mm);
    }
    
    void add(Dist d1,Dist d2){
        m=d1.m+d2.m;
        cm=d1.cm+d2.cm;
        mm=d1.mm+d2.mm;}
    void generalise()
    {
        if(mm>=10)
        {
            cm=cm+mm/10;
            mm=mm%10;
     
        }
        if(cm>=100)
        {
            m=m+cm/100;
            cm=cm%100;
                  
        }
    }
        
       
        
    }
```
<img width="866" height="613" alt="image" src="https://github.com/user-attachments/assets/7257188b-a300-42a6-b559-0610ba294b0f" />

## assi-5
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package com.mycompany.pilani;

import java.util.Scanner;

/**
 *
 * @author IBM17
 */
public class DisAddMCm {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        System.out.println("Hello World!");
        Dist1 o1=new Dist1();
        Dist1 o2=new Dist1();
        Dist1 o3=new Dist1();
        o1.input();
        o2.input();
        o1.generalise();
        o2.generalise();

        o3.add(o1,o2);
        o3.generalise();
        o3.output();
    }
    
}
class Dist1{
    int m;
    int cm;
    
     void input(){
         Scanner sc=new Scanner(System.in);
         System.out.println(" Enter mtr");
         m=sc.nextInt();
         System.out.println(" Enter cm");
         cm=sc.nextInt();
       
         
         
     }
     void output(){
         System.out.println(" mtr="+m);
         System.out.println(" cm="+cm);
          
    }
    
    void add(Dist1 d1,Dist1 d2){
        m=d1.m+d2.m;
        cm=d1.cm+d2.cm;
    }
    void generalise()
    {
        
        if(cm>=100)
        {
            m=m+cm/100;
            cm=cm%100;
                  
        }
    }
        
       
        
    }

```
<img width="828" height="559" alt="image" src="https://github.com/user-attachments/assets/28ddc39a-2e57-4cab-88d4-347966bf717d" />

## assi-6
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package com.mycompany.pilani;

import java.util.Scanner;

/**
 *
 * @author IBM17
 */
public class AddTime {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
         Time t1 = new Time();
        Time t2 = new Time();
        Time t3 = new Time();

        t1.input();
        t2.input();

        t3.add(t1, t2);
        t3.generalise();
        t3.output();
    }
    
}

class Time{
    
    
    int hr;
    int min;
    int sec;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter hours:");
        hr = sc.nextInt();

        System.out.println("Enter minutes:");
        min = sc.nextInt();

        System.out.println("Enter seconds:");
        sec = sc.nextInt();
    }

    void add(Time t1, Time t2) {
        hr = t1.hr + t2.hr;
        min = t1.min + t2.min;
        sec = t1.sec + t2.sec;
    }

    void generalise() {

        if (sec >= 60) {
            min = min + sec / 60;
            sec = sec % 60;
        }

        if (min >= 60) {
            hr = hr + min / 60;
            min = min % 60;
        }
    }

    void output() {
        System.out.println("Time = " + hr + " hr " + min + " min " + sec + " sec");
    }
}

```
<img width="962" height="630" alt="image" src="https://github.com/user-attachments/assets/1e619e2d-0cfc-4c62-8a48-765829fd8479" />










