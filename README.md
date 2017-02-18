Session 2
Assignment 6

1) Write a program to accept two numbers from stdin and find all the odd as well as even numbers present in between them.

import java.util.*;		//header containing all utilities
public class acad
{
	public static void main(String[] args) 
	{
		Scanner s = new Scanner(System.in);
		int num1=s.nextInt();		//getting the num1 from user
		int num2=s.nextInt();		//getting the num2 from user
		ArrayList<Integer> evennumbers = new ArrayList<Integer> ();
    //declaration of array list to store even numbers 
		ArrayList<Integer> oddnumbers = new ArrayList<Integer> ();	
    //declaration of array list to store odd numbers
		for(int i=num1;i<=num2;i++)
		{
			if(i%2==0)	//condition to check for even values
			{
				evennumbers.add(i);
			}
			else
			{
				oddnumbers.add(i);
			}
		}
		System.out.println("Even Numbers in the given range are :");
		Collections.sort(evennumbers);
		for(int x:evennumbers)
		{
			System.out.println(x);	//display even numbers
		}
		System.out.println("Odd Numbers in the given range are :");
		Collections.sort(oddnumbers);	//display odd numbers
		for(int y:oddnumbers)
		{
			System.out.println(y);
		}
	}
}

2) Joe is scared to go to school. When her dad asked the reason, Joe said she is unable to complete the task given by her teacher. The task was to find the “first 10 multiples” of the number entered from stdin.

import java.util.*;			//header to include all utilities
public class acad 
{
	public static void main(String[] args)
	{
		Scanner s = new Scanner(System.in);
		System.out.println("Enter the number for first 10 multiples: ");
		int num=s.nextInt();  //Input the number to get the first 10 multiples
		int tables[] = new int[10];	//to store result
		for(int i=0;i<10;i++)		//for the given range
		{
			tables[i] = num*(i+1);
		}
		System.out.println("The "+num+" tables is:");
		for(int j=0;j<10;j++)		// to display the first 10 multiples
		{
			System.out.println(num+" * "+(j+1)+" = "+tables[j]);
		}
	}
}

3) Write a program consisting method sum () and demonstrate the concept of method overloading using this method.

import java.util.*;
public class acad
{
	public static void main(String[] args)
	{
		Scanner s = new Scanner(System.in);
		int num1=s.nextInt();	//getting num1 from user
		int num2=s.nextInt();	//getting num2 from user
		int num3 =s.nextInt();	//getting num3 from user
		sum(num1,num2);			//calling method sum with two variables
		sum(num1,num2,num3);	//calling method sum with three variables
	}
	static void sum(int num1,int num2) //method to add two variables
	{
		int sum1;
		sum1=num1+num2;
		System.out.print("Sum of first two variables: ");
		System.out.println(sum1);		//printing the sum of two numbers
	}
	static void sum(int num1,int num2,int num3) //method to add three variables	
	{
		int sum2;
		sum2=num1+num2+num3;
		System.out.print("Sum of all three variables: ");
		System.out.println(sum2);			//print the sum of three numbers
	}
}
