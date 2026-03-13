[Program-1  Program to perform arithmatic operation on numbers using classes and objects](#assi-1)

[Program-2  Program to perform addition of distances where each distance is given in m,cm,mm(test result in  by creation of object in main class](#assi-2)

[Program-3  Program to perform addition of distances where each distance is given in m,cm(test result in  by creation of object in main class](#assi-3)

[Program-4  Program to perform addition of times where each time is given in hr,min,sec(test result in  by creation of object in main class](#assi-4)

[Program-5  Program to perform addition of times where each time is given in hr,min(test result in  by creation of object in main class](#assi-5)

[Program-6  Colect codes of five programs in c language and convert to java using object and classes in single program](#assi-6)

[Program-7  Write a class with four methods input,output,reverse,output reverse that is to perform operation on 1-D array](#assi-7)








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
















