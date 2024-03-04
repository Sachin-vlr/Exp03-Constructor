# Exp03-Constructor
## Aim: 
To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.

## Algorithm:

### Step1:
Initialize the program with the system library

### Step2:
Define the Employee Class and set it as public

### Step3:
Define the variables

### Step4:
Write a parameterized constructor under the class Employee

### Step5:
Define a function to calculate the salary

### Step6:
Define the display() function to print the output

## Program:
```c#
using System;

namespace ex3
{
    public class Employee
    {
        string name, designation;
        int noofexp;
        double bs,hra,ta,insuranceamount,grosspay;

        public Employee(string name,string designation,int noofexp,double bs,double insuranceamount)
        {
            this.name = name;
            this.designation = designation;
            this.noofexp = noofexp;
            this.bs = bs;
            this.insuranceamount = insuranceamount;
            


            hra = 0.1 * bs;
            ta = 0.2 * bs;
            grosspay = 0.15 * bs;
            
        }

        public double CalculateSalary()
        {
            return bs + hra + ta + insuranceamount - grosspay;
        }

        public void Display()
        {
            Console.WriteLine("Employee Name: " + name);
            Console.WriteLine("Employee Designation: " + designation);
            Console.WriteLine("Employee No of Experience: " + noofexp);
            Console.WriteLine("Employee Basic Salary: " + bs);
            Console.WriteLine("Employee Insurance Amount: " + insuranceamount);
            Console.WriteLine("Employee HRA: " + hra);
            Console.WriteLine("Employee TA: " + ta);
            Console.WriteLine("Employee GROSSPAY: " + grosspay);
            Console.WriteLine("Employee Salary: " + CalculateSalary());
        }

    }
    class Program
    {
        static void Main(string[] args)
        {
                Console.WriteLine("Enter employee name:");
                string name = Console.ReadLine();

                Console.WriteLine("Enter employee designation:");
                string designation = Console.ReadLine();

                Console.WriteLine("Enter employee number of years of experience:");
                int noofexp = Convert.ToInt32(Console.ReadLine());

                Console.WriteLine("Enter employee basic salary:");
                double bs = Convert.ToDouble(Console.ReadLine());

                Console.WriteLine("Enter employee insurance amount:");
                double insuranceamount = Convert.ToDouble(Console.ReadLine());

                Employee emp1 = new Employee(name, designation, noofexp, bs, insuranceamount);
                emp1.Display();
        }
    }
}
```

## Output:

![image](https://github.com/Sachin-vlr/Exp03-Constructor/assets/113497666/25326b95-8f8d-462e-bee4-8621f8d2b3a2)

## Result:
Thus, a C# program is written to calculate the salary of an employee using a constructor is implemented and the output is verified.
