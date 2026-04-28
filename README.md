[Program-1  Program to perform arithmatic operation on numbers using classes and objects](#assi-1)

[Program-2  Program to perform addition of distances where each distance is given in m,cm,mm(test result in  by creation of object in main class](#assi-2)

[Program-3  Program to perform addition of distances where each distance is given in m,cm(test result in  by creation of object in main class](#assi-3)

[Program-4  Program to perform addition of times where each time is given in hr,min,sec(test result in  by creation of object in main class](#assi-4)

[Program-5  Program to perform addition of times where each time is given in hr,min(test result in  by creation of object in main class](#assi-5)

[Program-6  Colect codes of five programs in c language and convert to java using object and classes in single program](#assi-6)

[Program-7  Write a class with four methods input,output,reverse,output reverse that is to perform operation on 1-D array](#assi-7)

[Program-8  Write class to perform matrix operation- addition,multiplication, transpose, sum of rows,sum of columns,diagonal sum](#assi-8)

[Program-9  Write program using 3 classes to print 1 too 100 in all 3  with and without  thread(analyse the output) repeat same using Runnable interface](#assi-9)

[Program-10 Using concept multithreading  the output of all three threads is unpredictable and all the threads  must be synchronised(using join method)](#assi-10)

[Program 11-program for addition of 2 Numbers using swing](#assi-11)

[Program 12-program for making calculator using swing](#assi-12)

[Program 13-program for matrix addition using swing](#assi-13)

[Program 14-create student registration for 10 elements sav ethat to applet, servalet, databasetable using JDBC connectivity](#assi-14)

[Program 15- Create one JFrame apply 10 buttons on that after clicking on each button a new structure is created(circle, oval, rectangle etc)](#assi-15)

[Program 16- Just using mouse event create a frame like paint brush with selection of colour and width](#assi-16)












## assi-1
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

## assi-2
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

## assi-4
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
public class TimeAddHrMin {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      
         Time1 t1 = new Time1();
        Time1 t2 = new Time1();
        Time1 t3 = new Time1();

        t1.input();
        t2.input();

        t3.add(t1, t2);
        t3.generalise();
        t3.output();
    
    }
    
}
class Time1{
    
    
    int hr;
    int min;
   

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter hours:");
        hr = sc.nextInt();

        System.out.println("Enter minutes:");
        min = sc.nextInt();

    
    }

    void add(Time1 t1, Time1 t2) {
        hr = t1.hr + t2.hr;
        min = t1.min + t2.min;
            }

    void generalise() {

        

        if (min >= 60) {
            hr = hr + min / 60;
            min = min % 60;
        }
    }

    void output() {
        System.out.println("Time = " + hr + " hr " + min + " min " );
    }
}
```
<img width="899" height="502" alt="image" src="https://github.com/user-attachments/assets/e4ff7edd-f955-4b81-97a8-1265910b947f" />

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
public class CombinedBase {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("\n--- Armstrong Number Check ---");
        ArmnocheckC a1 = new ArmnocheckC();
        a1.input(sc);
        a1.isarm();

        System.out.println("\n--- Factorial Program ---");
        FactorialC f = new FactorialC();
        f.input(sc);
        f.output();

        System.out.println("\n--- Fibonacci Series ---");
        FibonacciC fi = new FibonacciC();
        fi.input(sc);
        fi.series();

        System.out.println("\n--- Palindrome Check ---");
        PalindromeC p1 = new PalindromeC();
        p1.input(sc);
        p1.ispalin();

        System.out.println("\n--- Pyramid Pattern ---");
        PyramidC p = new PyramidC();
        p.input(sc);
        p.display();

        System.out.println("\n--- Swap Two Numbers ---");
        SwapnoC s = new SwapnoC();
        s.input(sc);
        s.output();
        s.swap();
        System.out.println("After swapping:");
        s.output();

        sc.close();
    }
}

class ArmnocheckC {
    int num;

    void input(Scanner sc) {
        System.out.println("Enter a number:");
        num = sc.nextInt();
    }

    void isarm() {
        int digits = countd(num);

        if (armsum(num, digits) == num)
            System.out.println("Number is Armstrong");
        else
            System.out.println("Number is NOT Armstrong");
    }

    int countd(int num) {
        if (num == 0)
            return 0;
        return 1 + countd(num / 10);
    }

    int armsum(int num, int digits) {
        if (num == 0)
            return 0;
        return (int) Math.pow(num % 10, digits) + armsum(num / 10, digits);
    }
}

class FactorialC {

    int num;
    int facto;

    void input(Scanner sc) {
        System.out.println("Enter number:");
        num = sc.nextInt();
        facto = fact(num);
    }

    int fact(int num) {
        if (num == 0 || num == 1)
            return 1;
        return num * fact(num - 1);
    }

    void output() {
        System.out.println("Factorial is: " + facto);
    }
}

class FibonacciC {

    int terms;

    void input(Scanner sc) {
        System.out.println("Enter number of terms:");
        terms = sc.nextInt();
    }

    void series() {

        int first = 0;
        int second = 1;
        int next;

        for (int i = 0; i < terms; i++) {
            System.out.print(first + " ");
            next = first + second;
            first = second;
            second = next;
        }

        System.out.println();
    }
}

class PalindromeC {

    int num;

    void input(Scanner sc) {
        System.out.println("Enter number to check:");
        num = sc.nextInt();
    }

    void ispalin() {
        if (num == reverse(num, 0))
            System.out.println("Number is Palindrome");
        else
            System.out.println("Number is NOT Palindrome");
    }

    int reverse(int n, int r) {
        if (n == 0)
            return r;

        return reverse(n / 10, r * 10 + n % 10);
    }
}

class PyramidC {

    int length;

    void input(Scanner sc) {
        System.out.println("Enter length of pyramid:");
        length = sc.nextInt();
    }

    void display() {

        for (int i = 1; i <= length; i++) {

            for (int j = i; j < length; j++) {
                System.out.print(" ");
            }

            for (int k = 1; k <= i; k++) {
                System.out.print("* ");
            }

            System.out.println();
        }
    }
}

class SwapnoC {

    int n1, n2;

    void input(Scanner sc) {
        System.out.println("Enter two numbers:");
        n1 = sc.nextInt();
        n2 = sc.nextInt();
    }

    void swap() {
        n1 = n1 + n2;
        n2 = n1 - n2;
        n1 = n1 - n2;
    }

    void output() {
        System.out.println("n1: " + n1);
        System.out.println("n2: " + n2);
    }
}
```
<img width="1185" height="923" alt="image" src="https://github.com/user-attachments/assets/0b5e6f4f-c359-4a28-88cf-b519a919225d" />

## assi-7
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
public class ArrayOp {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
    Arrayre o=new Arrayre();
    o.input();
    o.output();
    o.reverse();
    o.outputrev();
    }
    
}

class Arrayre{
    
    int arr[]=new int[5];
    int revarr[]=new int[5];
    void input()
    {   Scanner sc=new Scanner(System.in);
        System.out.print("Enter 5 elements in array: ");
        for (int i=0;i<5;i++)
        {   
        
            arr[i]=sc.nextInt();
    }}
    void output()
    {
        System.out.print("Original array is ");
        for(int i=0;i<5;i++)
        {
            System.out.print(arr[i]+" ");
           
        }
        System.out.println();
    
    } 
    void reverse()
    {   
        for(int i=0;i<5;i++)
        {revarr[i]=arr[5-i-1];
        }
            
        
    }
    void outputrev(){
        System.out.print("Reverse array is ");
        for(int i=0;i<5;i++)
        {
            System.out.print(revarr[i]+" ");
        }
    }
    
}
```
<img width="837" height="380" alt="image" src="https://github.com/user-attachments/assets/0a6b4101-cea9-4ffc-99a6-2ba7000ceb5e" />

## assi-8
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package pilani;
import java.util.Scanner;

/**
 *
 * @author IBM1
 */
public class MatrixMain {
    public static void main(String args[]){
        System.out.println("program strated");
    Matrix m=new Matrix();
    m.input();
    m.output();
    Matrixop o=new Matrixop();
    o.add(m);
    o.resoutput();
    o.mult(m);
    o.resoutput();
    o.transpose(m);
    o.sumOfClms(m);
    o.sumOfRows(m);
    o.sumOfDiagonal(m);
    
    
}}
class Matrix{
 int [][]m1=new int[3][3];
 int[][] m2=new int[3][3];
 
 

 Scanner sc= new Scanner(System.in);
 
 void input()
 {
  for(int i=0;i<3;i++)
 {for(int j=0;j<3;j++)
 { System.out.println("Enter element of 3*3 matrix m1:"+"m1["+i+"]["+j+"] : ");
     m1[i][j]=sc.nextInt();
      System.out.println("Enter elements of 3*3 matrix m2:"+"m2["+i+"]["+j+"] : ");
     m2[i][j]=sc.nextInt();
      }}
     
 }
 void output()
 {
     System.out.println(" m1 is : ");
     for(int i=0;i<3;i++)
     {
         for(int  j=0;j<3;j++){
             System.out.print(m1[i][j]+" ");
         }System.out.println();
     }
   System.out.println(" m2 is : ");
     for(int i=0;i<3;i++)
     {
         for(int  j=0;j<3;j++){
             System.out.print(m2[i][j]+" ");
         }System.out.println();
     }
     
 }
 
}
class Matrixop{
     Scanner sc= new Scanner(System.in);
    int[][]res=new int[3][3];
    void add(Matrix m)
    {   for(int i=0;i<3;i++)
    {for(int j=0;j<3;j++)
    {
       res[i][j]=m.m1[i][j]+m.m2[i][j]; }
       
    }}
    void resoutput(){
    System.out.println(" result : ");
     for(int i=0;i<3;i++)
     {
         for(int  j=0;j<3;j++){
             System.out.print(res[i][j]+" ");
         }System.out.println();
     }}
    void mult(Matrix m)
    {
        for(int i=0;i<3;i++)
        {
            for(int j=0;j<3;j++)
            {   res[i][j]=0;
                for(int k=0;k<3;k++)
                {
                    res[i][j]+=m.m1[i][k]*m.m2[k][j];
                }
            }
        }
    }
    void transpose(Matrix m)
    {   System.out.println("transpose of matrix:m1 or m2");
        
        String mt;
        mt=sc.next();
        int [][] mtr;
        if(mt.equals("m1"))
        //mt=="m1" check if they pt to same string obj not suitable here
        {
            mtr=m.m1;
        }
        else
            mtr=m.m2;
    
        
        for(int i=0;i<3;i++)
        {
            for(int j=0;j<3;j++)
            {
                System.out.print(mtr[j][i]+" ");
            } System.out.println();
        }
    }
    void sumOfRows(Matrix m)
    {
        
        System.out.println(" enter matrix to find sum of row m1 or m1");
        String ms;
        ms=sc.next();
        int [][] msr;
        if(ms.equals("m1"))
        {
                msr=m.m1;            
    
         }
        else
            msr=m.m2;
        for(int i=0;i<3;i++)
        {   int sum=0;
            for(int j=0;j<3;j++)
            {
               sum+=msr[i][j];
            }   System.out.println("Sum of row"+(i+1)+"="+sum);
        }
    } 
    
    void sumOfClms(Matrix m)
    {
        
        System.out.println(" enter matrix to find sum of clmns of m1 or m1");
        String ms;
        ms=sc.next();
        int [][] msc;
        if(ms.equals("m1"))
        {
                msc=m.m1;            
    
         }
        else
            msc=m.m2;
        for(int i=0;i<3;i++)
        {   int sum=0;
            for(int j=0;j<3;j++)
            {
               sum+=msc[j][i];
            }   System.out.println("Sum of columns"+(i+1)+"="+sum);
        }
    } 
    void sumOfDiagonal(Matrix m)
    { System.out.println(" enter matrix to find sum of diagonal of m1 or m1");
        String ms;
        ms=sc.next();
        int [][] msd;
        if(ms.equals("m1"))
        {
                msd=m.m1;            
    
         }
        else
            msd=m.m2;
        
        int df=0;
        int ds=0;
        for(int i=0;i<3;i++)
        {   
            for(int j=0;j<3;j++)
            {  if(i==j)
               df+=msd[i][j];

            }          ds+=msd[i][3-i-1]; 
        }
        System.out.println("first diagonal"+"="+df);
        System.out.println("second diagonal"+"="+ds);
        
        
    }  
    }

```
<img width="497" height="894" alt="image" src="https://github.com/user-attachments/assets/c7a28466-75f2-4355-87f0-6f552028b272" />

## assi-9
```
public class Mainred {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Thread1 t1=new Thread1();
         Thread2 t2=new Thread2();
          Thread3 t3=new Thread3();
          t1.fun();
          t2.fun();
          t3.fun();
    }
    
}
 class Thread1 {
    void fun(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 1:"+i);
            }}
}
class Thread2 {
    void fun(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 2:"+i);
            }}
    
}
class Thread3 {
    void fun(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 3:"+i);
            }}
    
}

public class CombinedT 
    {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        TThread1 t1=new TThread1();
         TThread2 t2=new TThread2();
          TThread3 t3=new TThread3();
          t1.start();
          t2.start();
          t3.start();
    }
    
}
   class TThread1 extends Thread {
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 1:"+i);
            }}
}
class TThread2 extends Thread  {
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 2:"+i);
            }}
    
}
class TThread3 extends Thread  {
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 3:"+i);
            }}
    
}
public class Threadinter{ 
        public static void main(String[] args) {
        // TODO code application logic here
        TIThread1 t1=new TIThread1();
        TIThread2 t2=new TIThread2();
        TIThread3 t3=new TIThread3();
        Thread th1=new Thread(t1);
        Thread th2=new Thread(t2);
        Thread th3=new Thread(t3);
        
          th1.start();
          th2.start();
          th3.start();
    }}
    

   class TIThread1 implements Runnable {
    @Override
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 1:"+i);
            }}
}
class TIThread2 implements Runnable  {
    @Override
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 2:"+i);
            }}
    
}
class TIThread3 implements Runnable  {
    @Override
    public void run(){
    for(int i=0;i<100;i++)
    {
    System.out.println("THREAD 3:"+i);
            }}
    
}
```
<img width="1011" height="900" alt="image" src="https://github.com/user-attachments/assets/8a4245e6-939a-4561-9482-4ad8c5d73d2e" />
<img width="662" height="904" alt="image" src="https://github.com/user-attachments/assets/1725296b-dc59-4271-ba97-506377bc13ac" />
<img width="283" height="815" alt="image" src="https://github.com/user-attachments/assets/fbd271a7-acc4-41fb-be11-324f141ffdb1" />

## assi-10
```
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package pilani;

/**
 *
 * @author IBM1
 */
public class Threadinter{ 
        public static void main(String[] args) {
        // TODO code application logic here
        Cthread t1=new Cthread("t1");
        Cthread t2=new Cthread("t2");
        Cthread t3=new Cthread("t3");
        Thread th1=new Thread(t1);
        Thread th2=new Thread(t2);
        Thread th3=new Thread(t3);
        try {
            // Start T1 and immediately wait for it to complete
            th1.start();
            th1.join(); 

            // T2 will only start after T1 has died
            th2.start();
            th2.join();

            // T3 will only start after T2 has died
            th3.start();
            th3.join();

        } catch (InterruptedException e) {
            System.out.println("Main thread was interrupted.");
        }
        
        System.out.println("Main execution finished.");
    }
}
    
    

   class Cthread implements Runnable {
        private String name;
        Cthread(String name)
        {this.name=name;}
    @Override
    public void run(){
        
    for(int i=0;i<10;i++)
    {
        System.out.println(name+"processing"+i);
        try{ 
            Thread.sleep(50);

    }
    catch (InterruptedException e){
            
            e.printStackTrace();
            }}
    System.out.println("successfull completed"+name);
    
            }
   
   }

```
<img width="363" height="733" alt="image" src="https://github.com/user-attachments/assets/43978f76-3d5a-438d-8214-e6c6aa832805" />
## assi-11
```
import javax.swing.*;

public class Add {
    public static void main(String[] args) {
        JFrame f = new JFrame("Addition");

        JLabel l1 = new JLabel("Enter Number 1:");
        JLabel l2 = new JLabel("Enter Number 2:");
        JLabel l3 = new JLabel("Result:");

        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JTextField t3 = new JTextField();

        JButton b = new JButton("Add");

        l1.setBounds(30, 30, 120, 30);
        t1.setBounds(160, 30, 100, 30);

        l2.setBounds(30, 70, 120, 30);
        t2.setBounds(160, 70, 100, 30);

        b.setBounds(90, 110, 80, 30);

        l3.setBounds(30, 150, 120, 30);
        t3.setBounds(160, 150, 100, 30);

        f.add(l1); 
        f.add(t1);
        f.add(l2); 
        f.add(t2);
        f.add(b);
        f.add(l3); 
        f.add(t3);

        // Button action
        b.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b1 = Integer.parseInt(t2.getText());
            t3.setText(String.valueOf(a + b1));
        });

        f.setSize(320, 250);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
<img width="379" height="303" alt="image" src="https://github.com/user-attachments/assets/cf347de9-ec15-4109-8607-9019723d0fe6" />


## assi-12
```
import javax.swing.*;
import java.awt.event.*;

public class Calculator {
    public static void main(String[] args) {
        JFrame f = new JFrame("Calculator");

        JLabel l1 = new JLabel("Enter Number 1:");
        JLabel l2 = new JLabel("Enter Number 2:");
        JLabel l3 = new JLabel("Result:");

        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JTextField t3 = new JTextField();

        JButton add = new JButton("+");
        JButton sub = new JButton("-");
        JButton mul = new JButton("*");
        JButton div = new JButton("/");

        l1.setBounds(30, 30, 120, 30);
        t1.setBounds(160, 30, 100, 30);

        l2.setBounds(30, 70, 120, 30);
        t2.setBounds(160, 70, 100, 30);

        l3.setBounds(30, 110, 120, 30);
        t3.setBounds(160, 110, 100, 30);

        add.setBounds(30, 160, 50, 30);
        sub.setBounds(90, 160, 50, 30);
        mul.setBounds(150, 160, 50, 30);
        div.setBounds(210, 160, 50, 30);

        f.add(l1); f.add(t1);
        f.add(l2); f.add(t2);
        f.add(l3); f.add(t3);

        f.add(add); f.add(sub); f.add(mul); f.add(div);

        add.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            t3.setText(String.valueOf(a + b));
        });

        sub.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            t3.setText(String.valueOf(a - b));
        });

        mul.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            t3.setText(String.valueOf(a * b));
        });

        div.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            t3.setText(String.valueOf(a / b));
        });

        f.setSize(320, 250);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
<img width="379" height="304" alt="image" src="https://github.com/user-attachments/assets/b3bf50e8-939b-48b2-901a-a48b365acde5" />

## assi-13
```
import javax.swing.*;
import java.awt.event.*;

public class MatrixAdd {
    public static void main(String[] args) {

        JFrame f = new JFrame("Dynamic Matrix Addition");

        JLabel sizeLabel = new JLabel("Enter Size:");
        JTextField sizeField = new JTextField();
        JButton create = new JButton("Create Matrix");

        sizeLabel.setBounds(50, 20, 100, 30);
        sizeField.setBounds(150, 20, 50, 30);
        create.setBounds(220, 20, 130, 30);

        f.add(sizeLabel);
        f.add(sizeField);
        f.add(create);

        create.addActionListener(e -> {
            int n = Integer.parseInt(sizeField.getText());

            JTextField[][] A = new JTextField[n][n];
            JTextField[][] B = new JTextField[n][n];
            JTextField[][] C = new JTextField[n][n];

            JLabel l1 = new JLabel("Matrix A");
            JLabel l2 = new JLabel("Matrix B");
            JLabel l3 = new JLabel("Result");

            l1.setBounds(50, 70, 100, 20);
            l2.setBounds(250, 70, 100, 20);
            l3.setBounds(450, 70, 100, 20);

            f.add(l1); f.add(l2); f.add(l3);

            int x = 50, y = 100;

            for(int i=0;i<n;i++){
                for(int j=0;j<n;j++){
                    A[i][j] = new JTextField();
                    A[i][j].setBounds(x + j*50, y + i*40, 40, 30);
                    f.add(A[i][j]);
                }
            }

            x = 250;
            for(int i=0;i<n;i++){
                for(int j=0;j<n;j++){
                    B[i][j] = new JTextField();
                    B[i][j].setBounds(x + j*50, y + i*40, 40, 30);
                    f.add(B[i][j]);
                }
            }
            
            x = 450;
            for(int i=0;i<n;i++){
                for(int j=0;j<n;j++){
                    C[i][j] = new JTextField();
                    C[i][j].setBounds(x + j*50, y + i*40, 40, 30);
                    C[i][j].setEditable(false);
                    f.add(C[i][j]);
                }
            }

            JButton add = new JButton("Add");
            add.setBounds(250, y + n*50, 80, 30);
            f.add(add);

            add.addActionListener(ev -> {
                for(int i=0;i<n;i++){
                    for(int j=0;j<n;j++){
                        int a = Integer.parseInt(A[i][j].getText());
                        int b = Integer.parseInt(B[i][j].getText());
                        C[i][j].setText(String.valueOf(a + b));
                    }
                }
            });

            f.repaint();
        });

        f.setSize(700, 500);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
<img width="857" height="616" alt="image" src="https://github.com/user-attachments/assets/296fc531-8481-4ad3-97b7-128a31a6d9f4" />































