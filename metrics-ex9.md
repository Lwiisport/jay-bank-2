# Exercice 9 (repo 2) : Increase coverage with JaCoCo.

Le coverage de la classe `BankAccount` est à 2%. Je vais donc rajouter un test sur une classe : 

```
@Test

public void GetInitMoney(){
	BankAccount compteBancaire = new BankAccount();
	assertEquals(0, compteBancaire.getInitMoneyAmount(), 0.001);
}
```

On voit que le coverage augmente à 4% et que les valeurs changent, par exemple les méthodes `missed` passe de `58` à `57`. Le coverage devient donc meilleur.
