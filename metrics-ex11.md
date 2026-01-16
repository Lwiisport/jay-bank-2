# Exercice 11 (Repo 2) : Cucumber for BankAccount.

Après avoir créer les fichiers nécessaires, nous pouvons maintenant écrire les tests: 

``` 
@Given("I have a new bank account")
public void i_have_a_new_bank_account() {

	// TODO: create a new bank account with initial balance 0
	account = new BankAccount();

}

  

@When("I check its balance")
public void i_check_its_balance() {

	// TODO: read the balance from the account and store it in observedBalance
	observedBalance = account.getBalance();

}

  

@Then("the balance should be {int}")
public void the_balance_should_be(Integer expected) {

	// TODO: assert that observedBalance equals expected
	// Example: assertEquals(expected.intValue(), observedBalance);
	assertEquals(expected.intValue(), (int)observedBalance);

}
```

après `mvn test`, le scénario apparaît dans les `output` et passe correctement.
