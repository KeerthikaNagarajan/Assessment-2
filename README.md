# Assessment-2
### Question 1
```
1.Using inheritance, one class can acquire the properties of others. Consider the following Animal class:
class Animal{
    void walk(){
        System.out.println("I am walking");
    }
}
This class has only one method, walk. Next, we want to create a Bird class that also has a fly method. We do this using extends keyword:
class Bird extends Animal {
    void fly() {
        System.out.println("I am flying");
    }
}
Finally, we can create a Bird object that can both fly and walk.
public class Solution{
   public static void main(String[] args){

      Bird bird = new Bird();
      bird.walk();
      bird.fly();
   }
}
The above code will print:
I am walking
I am flying
This means that a Bird object has all the properties that an Animal object has, as well as some additional unique properties.
  You must add a sing method to the Bird class, then modify the main method accordingly so that the code prints the following lines:
I am walking
I am flying I am singing
```
### Code:
```
class Animal{
    void walk(){
        System.out.println("I am walking");
    }
}
class Bird extends Animal {
    void fly(){
        System.out.print("I am flying");
    }
    void sing(){
        System.out.print(" I am singing");
    }
}
public class Solution
{
    public static void main(String[] args){
        Bird bird = new Bird();
        bird.walk();
        bird.fly();
        bird.sing();
    }
}
```
### Output:
<img width="155" alt="1" src="https://user-images.githubusercontent.com/93427089/226132792-13f99a15-d0d4-4d77-a79f-2efb052e466b.png">

### Question 2
```
2. Create a class named 'Member' having the following members:
Data members
1 - Name
2 - Age
3 - Phone number
4 - Address
5 - Salary
It also has a method named 'printSalary' which prints the salary of the members.
Two classes 'Employee' and 'Manager' inherits the 'Member' class. The 'Employee' and 'Manager' classes have data members 'specialization' and 'department' respectively. Now, assign name, age, phone number, address and salary to an employee and a manager by making an object of both of these classes and print the same.
```
### Code:
```
class Member {
    String name;
    int age;
    String phoneNumber;
    String address;
    double salary;

    public void printSalary() {
        System.out.println("Salary: " + salary);
    }
}

class Employee extends Member {
    String specialization;
}

class Manager extends Member {
    String department;
}

public class Main {
    public static void main(String[] args) {
        Employee employee = new Employee();
        employee.name = "John Smith";
        employee.age = 25;
        employee.phoneNumber = "1234567890";
        employee.address = "123 Main St, Anytown USA";
        employee.salary = 50000.00;
        employee.specialization = "Java Developer";

        Manager manager = new Manager();
        manager.name = "Jane Doe";
        manager.age = 35;
        manager.phoneNumber = "0987654321";
        manager.address = "456 Elm St, Anytown USA";
        manager.salary = 100000.00;
        manager.department = "Engineering";

        System.out.println("Employee:");
        System.out.println("Name: " + employee.name);
        System.out.println("Age: " + employee.age);
        System.out.println("Phone Number: " + employee.phoneNumber);
        System.out.println("Address: " + employee.address);
        System.out.println("Salary: " + employee.salary);
        System.out.println("Specialization: " + employee.specialization);

        System.out.println("\nManager:");
        System.out.println("Name: " + manager.name);
        System.out.println("Age: " + manager.age);
        System.out.println("Phone Number: " + manager.phoneNumber);
        System.out.println("Address: " + manager.address);
        System.out.println("Salary: " + manager.salary);
        System.out.println("Department: " + manager.department);
    }
}
```
### Output:
<img width="212" alt="2" src="https://user-images.githubusercontent.com/93427089/226132810-e1a19509-4e20-4e40-bad9-f2b5fcb1cb86.png">

### Question 3
```
 3.Write a program that would print the information (name, year of joining, salary, address) of three employees by creating a class named 'Employee'. The output should be as follows:
Name        Year of joining        Address
Robert            1994                64C- WallsStreat
Sam                2000                68D- WallsStreat
John                1999                26B- WallsStreat
```
### Code:
```
class employee
{
    public void ename(String name)
    {
        System.out.print(name);
    }
    public void eyear(int year)
    {
        System.out.print(year);
    }
    public void eadd(String add)
    {
        System.out.print(add);
    }
}

public class Mainemployee
{
    public static void main(String[] args)
    {
        System.out.print("Name\t");
        System.out.print("\tYear of joining\t");
        System.out.print("\t\tAddress\t");
        System.out.println();
        employee emp1=new employee();
        emp1.ename("Robert\t\t\t");
        emp1.eyear(1994);
        emp1.eadd("\t\t\t64C-WallsStreet");

        System.out.println();
        employee emp2=new employee();
        emp2.ename("Sam\t\t\t\t");
        emp2.eyear(2000);
        emp2.eadd("\t\t\t68D-WallsStreet");

        System.out.println();
        employee emp3=new employee();
        emp3.ename("John\t\t\t");
        emp3.eyear(1999);
        emp3.eadd("\t\t\t26B-WallsStreet");

    }
}
```
### Output:
<img width="306" alt="3" src="https://user-images.githubusercontent.com/93427089/226132824-e7cadddd-484b-4000-99c1-dc04aa3bd246.png">

### Question 4
```
4.Define a method to calculate power of a number raised to other i.e. ab using recursion where the numbers 'a' and 'b' are to be entered by the user
```
### Code:
```
import java.util.Scanner;
public class Power {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the base number: ");
        int base = scanner.nextInt();
        System.out.print("Enter the exponent number: ");
        int exponent = scanner.nextInt();

        int result = power(base, exponent);
        System.out.printf("%d^%d = %d", base, exponent, result);
    }

    public static int power(int base, int exponent) {
        if (exponent == 0) {
            return 1;
        } else {
            return base * power(base, exponent - 1);
        }
    }
}
```
### Output:
<img width="181" alt="4" src="https://user-images.githubusercontent.com/93427089/226132833-6ac92470-e04b-47cd-90a1-6f94d0652bfe.png">

### Question 5
```
5.The Matrix class has methods for each of the following:
1 - get the number of rows
2 - get the number of columns
3 - set the elements of the matrix at given position (i,j)
4 - adding two matrices. If the matrices are not addable, "Matrices cannot be added" will be displayed.
5 - multiplying the two matrices
```
### Code:
```
import java.util.Scanner;
public class TwoMatrix {
    public static void main(String [] args){
        int r1,r2,c1,c2;
        int [][]Arr1;
        int [][]Arr2;
        Matrix m=new Matrix();
        System.out.println("Enter no of rows for matrix 1: ");
        r1=m.rows();
        System.out.println("Enter no of columns for matrix 1: ");
        c1=m.columns();
        System.out.println("Enter no of rows for matrix 2: ");
        r2=m.rows();
        System.out.println("Enter no of columns for matrix 2: ");
        c2=m.columns();
        Arr1=m.setmatix(r1,c1);
        Arr2=m.setmatix(r2,c2);
        System.out.println("Sum of two matrics: ");
        m.add(Arr1,Arr2,r1,c1,r2,c2);
        System.out.println("Product of two matrics: ");
        m.product(Arr1,Arr2,r1,c1,r2,c2);
    }
}
class Matrix {
    public int rows(){
        Scanner sc= new Scanner(System.in);
        return sc.nextInt();
    }
    public int columns(){
        Scanner sc= new Scanner(System.in);
        return sc.nextInt();
    }
    public int[][] setmatix(int r1, int c1){
        int [][]Arr1= new int[50][50];
        Scanner sc= new Scanner(System.in);
        for(int i=0;i<r1;i++) {
            for (int j = 0; j < c1; j++) {
                Arr1[i][j] = sc.nextInt();
            }
        }
        return Arr1;
    }
    public void add(int [][] Arr1,int [][] Arr2,int r1,int c1,int r2,int c2){
        int [][]sum=new int[50][50];
        if((r1==r2)&&(c1==c2)){
            for(int i=0;i<r1;i++)
            {
                for(int j=0;j<c1;j++){
                    sum[i][j]=Arr1[i][j]+Arr2[i][j];
                }
            }
        }
        else{
            System.out.println("Cannot able to add the matrices!!");
        }
        for(int i=0;i<r1;i++){
            for(int j=0;j<c1;j++){
                System.out.print(sum[i][j]+" ");
            }
            System.out.print("\n");
        }
        System.out.print("\n");
    }
    public void product(int [][] Arr1,int [][] Arr2,int r1,int c1,int r2,int c2){
        int [][] Ans=new int[50][50];
        if((r1==r2)&&(c1==c2)){
            for(int i=0;i<r1;i++)
            {
                for(int j=0;j<c1;j++){
                    for(int k=0;k<r1;k++){
                        Ans[i][j]=Ans[i][j]+(Arr1[i][k]*Arr2[k][j]);
                    }
                }
            }
        }
        else{
            System.out.println("Cannot able to add the matrices!!");
        }
        for(int i=0;i<r1;i++){
            for(int j=0;j<c1;j++){
                System.out.print(Ans[i][j]+" ");
            }
            System.out.print("\n");
        }
        System.out.print("\n");
    }
}
```
### Output:
<img width="214" alt="5" src="https://user-images.githubusercontent.com/93427089/226132844-4a7e17b4-ac16-4cd3-bc50-e6b764051946.png">


