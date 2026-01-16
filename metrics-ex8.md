# Exercice 8 : (Repo 2): Write unit test for the bank domain.

Voici mes tests unitaires dans le fichier `BankAccountTest.java` : 

```
@Test

public void DespositTest()
{
	BankAccount compteBancaire = new BankAccount();
	compteBancaire.depositMoney(100);
	assertEquals(100.0, compteBancaire.getBalance(), 0.001);
}

  

@Test
public void DepositNegativeTest()
{
	BankAccount compteBancaire = new BankAccount();
	compteBancaire.depositMoney(-100);
	assertEquals(0, compteBancaire.getBalance(), 0.001);
}

  

@Test
public void WithdrawTooMuchMoney()
{
	BankAccount compteBancaire = new BankAccount();
	compteBancaire.depositMoney(100);
	compteBancaire.withdrawMoney(200);
	assertEquals(100, compteBancaire.getBalance(), 0.001);
}

}
```

Il passe tous correctement et l'on a bien les deux différent types de tests.
