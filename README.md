package Practice_lab;

public class BankAccount {
	String name;
	String acctype;
	int amt;
	static int  totalAccounts=0;
	BankAccount(String name)
	{
		this.name=name;
		this.acctype="saving";
		this.amt=0;
		 totalAccounts++;
	}
	BankAccount(String name,int dep)
	{
		this.name=name;
		this.acctype="saving";
		this.amt=dep;
		 totalAccounts++;
	}
	BankAccount(String name, int dep, String acctype) {
        this.name = name;
        this.acctype = acctype;
        this.amt = dep;
        totalAccounts++;
	}
	
	void Deposite(int amount)
	{
		amt=amt+amount;
		System.out.println("name="+name);
		System.out.println("amount deposited="+amt);
	}
	void Deposite(int amount,String type)
	{
		amt=amt+amount;
		System.out.println("name="+name);
		System.out.println("amount deposited="+amt);
		System.out.println("account type="+type);
	}
	
	static void totalacc()
	{
		System.out.println("total number of accounts="+totalAccounts);
	}
	public static void main(String []args)
	{
		BankAccount a1=new BankAccount("pranav");
		BankAccount a2=new BankAccount("pranav",1000);
		BankAccount a3=new BankAccount("pranav",1000,"cash");
		a1.Deposite(1000);
		a2.Deposite(5000,"cash");
		 BankAccount.totalacc();
	}
	
}
