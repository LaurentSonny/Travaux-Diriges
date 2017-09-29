# Travaux-Diriges
Tous les TD
TD 1
// Code pour le calcul du volumme d'un pavé droit
import java.util.Scanner;

public class Class_1 {	
	public static void main(String [] args) {
		double longueur = -1;
		double largeur = -1;
		double hauteur = -1;
		Scanner scan = new Scanner(System.in);
		System.out.println("Calculons le volume d'un pavé droit");
		while (longueur <= 0) {
			System.out.println("La longueur doit etre strictement positive ");
			System.out.println("Longueur:\n");
			longueur= scan.nextDouble();
		}
		while (largeur <= 0) {
			System.out.println("La largeur doit etre strictement positive ");
			System.out.println("Largeur:\n");
			 largeur = scan.nextDouble();		
		}
		while (hauteur <= 0) {
			System.out.println("La hauteur doit etre strictement positive ");
			System.out.println("Hauteur:\n");
			 hauteur = scan.nextDouble();
		}
		double volume = longueur*largeur*hauteur;

		System.out.println("Whoa le volume du pavÃ© c'est: " + volume +" fuck yeah!" );
		scan.close();
	}
}	

//Code pour le calcul d'un polynome du second degré
import java.util.Scanner;

public class Class_1 {	
	public static void main(String [] args) {
    Integer a,b,c,delta;
		Scanner scan = new Scanner(System.in);
		System.out.println(" a : \n");
		a = scan.nextInt();
		System.out.println(" b : \n");
		b = scan.nextInt();
		System.out.println(" c : \n");
		c = scan.nextInt();
		delta = (b*b -4*a*c);
		if (delta > 0) {
			System.out.println(" Il y a deux solutions :" + (b- Math.sqrt(delta))/2*a + " et " + (b+ Math.sqrt(delta))/2*a);
		}
		else if (delta < 0) {
			System.out.println(" Il n'y a pas de solution réelle");			
		}
		else {
			System.out.println(" Il y a une seule solution : " + -b /(2*a));
		}
  }
}
