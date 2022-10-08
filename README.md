# part-7_Practical-3

package part7;

import java.util.*;

class AccountHolder {
	int age;
	double netincome;
	int experience;
	String citizenship;

	AccountHolder(int age, double netincome, int experience, String citizenship) {
		this.age = age;
		this.netincome = netincome;
		this.experience = experience;
		this.citizenship = citizenship;
	}

	public String eligibility() {
		if (age >= 21 && age <= 60 && netincome >= 15000 && experience >= 1 && citizenship.equals("Indian")) {
			return "Eligible";
		} else {
			return "Not Eligible";
		}
	}
}

public class Practial_3 {

	public static void main(String[] args) {

		ArrayList<AccountHolder> obj = new ArrayList<AccountHolder>();

		int i = 1;

		while (i < 6) {
			Scanner sc = new Scanner(System.in);
			System.out.println("Enter the age:");
			int age = sc.nextInt();
			System.out.println("Enter the Net monthly Income:");
			double netincome = sc.nextDouble();
			System.out.println("Enter the Total work Experience:");
			int exp = sc.nextInt();
			System.out.println("Enter the citizenship:");
			String citizenship = sc.next();
			obj.add(new AccountHolder(age, netincome, exp, citizenship));
			i++;
		}

		for (int j = 1; j < obj.size() + 1; j++) {
			System.out.println("AccHolder " + j + " is " + obj.get(j - 1).eligibility());
		}
	}

}
