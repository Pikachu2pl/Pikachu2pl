package kalkulator123;

import java.util.Scanner;
import java.util.Connection;
import java.util.DriverManager;
import java.util.ResultSet;
import java.util.SQLEception;
import java.util.Statement;

public class Kalkulator1234 {

public static void main(String[] args) {
	// TODO Auto-generated method stub
	
	Scanner scan = new Scanner(System.in);
	System.out.println("Wybierz pierwszą liczbe do działania");
	int x = scan.nextInt();
	scan.nextLine();
	System.out.println("Podaj drugą liczbe");
	int y = scan.nextInt();
	scan.nextLine();
	System.out.println("Wybierz które z podanych zrobić :");
	System.out.println("[1] Dodawanie");
	System.out.println("[2] Odejmowanie");
	System.out.println("[3] Mnożenie");
	System.out.println("[4] Dzielenie x przez y");
	String z = scan.nextLine();
	int wynik = 0;
	if (z.equals("1")) {
		wynik=x+y;
	}
	else if (z.equals("2")) {
		wynik=x-y;
	}
	else if (z.equals("3")) {
		wynik=x*y;
	}
	else if (z.equals("4")) {
		wynik=x/y;
	}
	else {System.out.println("Blad");
							}
	System.out.println(wynik);
	
	Class.forName("org.sqlite.JDBC");
	java.sql.Connection connection = null;
	connection = java.sql.DriverManager.getConnection("jdbc:sqlite:historia kalkulatora1234.db");
	java.sql.Statement statement = connection.createStatement();
	statement.setQueryTimeout(30); //set timeout to 30 sec.
	statement.executeUpdate("INSERT INTO Results values('+X[i]','"+s")");//!!!
	
	
	
	if(connection !=null)
		connection.close();
					
	scan.close();
}
}
