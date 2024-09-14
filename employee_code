package com.tka.collection;

public class Employee {
	
	private int empid;
	private String empnm;
	private double empsal;
	public Employee() {
		super();
		// TODO Auto-generated constructor stub
	}
	public Employee(int empid, String empnm, double empsal) {
		super();
		this.empid = empid;
		this.empnm = empnm;
		this.empsal = empsal;
	}
	public int getEmpid() {
		return empid;
	}
	public void setEmpid(int empid) {
		this.empid = empid;
	}
	public String getEmpnm() {
		return empnm;
	}
	public void setEmpnm(String empnm) {
		this.empnm = empnm;
	}
	public double getEmpsal() {
		return empsal;
	}
	public void setEmpsal(double empsal) {
		this.empsal = empsal;
	}
	@Override
	public String toString() {
		return "Employee [empid=" + empid + ", empnm=" + empnm + ", empsal=" + empsal + "]";
	}
	

}
package com.tka.collection;

import java.util.ArrayList;
import java.util.Iterator;

public class EmployeeData
{
	static ArrayList<Employee> arraylist=new ArrayList();
	
static public void addEmployee(Employee e)
	{
		arraylist.add(e);
		System.out.println("Employee Added");
	}
static public void displayAll()
{
	Iterator<Employee> it=arraylist.iterator();
	while(it.hasNext())
		System.out.println(it.next());
}
static public void searchEmployee(int empid)
{
	int flg=0;
	for(Employee e:arraylist)
	{
		if(empid==e.getEmpid())
		{
			flg=1;
			System.out.println(e);
			break;
		}
	}
	if(flg==0)
		System.out.println("Not found");
}
static public void updateEmployee(int empid,double empsal)
{
	
	for(Employee e:arraylist)
	{
		if(empid==e.getEmpid())
		{
			e.setEmpsal(empsal);
			System.out.println("Salary updated");
			break;
		}
	}
}
static public void deleteEmployee(int empid)
{
	int flg=0;
	for(Employee e:arraylist)
	{
		if(empid==e.getEmpid())
		{
			arraylist.remove(empid);
			System.out.println("Record deleted");
			break;
		}
	}
}
}
package com.tka.collection;

import java.util.Scanner;

public class MainEmp {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		
		Scanner sc =new Scanner(System.in);
		System.out.println("Enter empid,empnm,empsal");
		Employee employee=new Employee(sc.nextInt(),sc.next(),sc.nextDouble());
		EmployeeData.addEmployee(employee);
	
		System.out.println("All Employees");
		EmployeeData.displayAll();
		
		System.out.println("Enter empid to search");
		EmployeeData.searchEmployee(sc.nextInt());
		
		System.out.println("Enter id and sal to be updated");
		EmployeeData.updateEmployee(sc.nextInt(),sc.nextDouble());
		
		System.out.println("Enter id to delete");
		EmployeeData.deleteEmployee(sc.nextInt());
	}

}
