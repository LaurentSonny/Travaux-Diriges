# Travaux-Diriges
import java.util.Scanner;

public class Class_3 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		// Exercice 4.1
		double[][] tab = new double[3][4];
		double moyenne = 0;
		Scanner scan = new Scanner(System.in);
		for (int i = 0; i < tab[1].length; ++i) {
			for (int j = 0; j < tab.length; ++j) {
				tab[j][i] = (int) (Math.random() * 10);
			}
		}
		for (int i = 0; i < tab[1].length; ++i) {
			for (int j = 0; j < tab.length; ++j) {
				System.out.print("|" + tab[j][i]);
			}
			System.out.print("|\r\n");
		}
		moyenne = moyenne(tab);
		int valeurs = tab.length * tab[0].length;
		Integer inferieurs = denombrement(tab, moyenne);
		Integer superieurouegal = valeurs - denombrement(tab, moyenne);
		double[] echantillon_inferieur = new double[inferieurs];
		double[] echantillon_superieur_egal = new double[superieurouegal];
		System.out.println("La moyenne est : " + moyenne);
		recherche(tab, Math.floor(moyenne));
		echantillon_inferieur(tab, moyenne, echantillon_inferieur);
		echantillon_superieur_egal(tab, moyenne, echantillon_superieur_egal);
		System.out.print("Tableau inferieur : |");
		for (int j = 0; j < echantillon_superieur_egal .length; ++j) {
			System.out.print(echantillon_superieur_egal [j] + "|" );
		}
		System.out.print("\r\nTableau supérieur : |");
		for (int j = 0; j < tab.length; ++j) {
			System.out.print(echantillon_inferieur[j] + "|" );
		}
	}

	public static double moyenne(double tableau[][]) {
		double M = 0;
		for (int i = 0; i < tableau[1].length; ++i) {
			for (int j = 0; j < tableau.length; ++j) {
				M += tableau[j][i];
			}
		}
		return (M / (tableau[1].length * tableau.length));
	}

	public static double recherche(double tableau[][], double moyenne) {
		for (int i = 0; i < tableau[1].length; ++i) {
			for (int j = 0; j < tableau.length; ++j) {
				if (tableau[j][i] == moyenne) {
					System.out.println("Les coordonnées de la moyenne sont : [" + j + ";" + i + "]");
					return (0);
				}
			}
		}
		System.out.println("La moyenne n'est pas dans le tableau.");
		return (0);
	}

	public static Integer denombrement(double tableau[][], double moyenne) {
		Integer inferieurs = 0;
		for (int i = 0; i < tableau[1].length; ++i) {
			for (int j = 0; j < tableau.length; ++j) {
				if (tableau[j][i] < moyenne)
					++inferieurs;
			}
		}
		return inferieurs;
	}

	public static double[] echantillon_inferieur(double tableau[][], double moyenne, double[] inf) {
		Integer increment = 0;
		for (int i = 0; i < tableau[1].length; ++i) {
			for (int j = 0; j < tableau.length; ++j) {
				if (tableau[j][i] < moyenne) {
					inf[increment] = tableau[j][i];
					++increment;
				}
			}
		}
		return inf;
	}

	public static double[] echantillon_superieur_egal(double tableau[][], double moyenne, double[] sup) {
		Integer increment = 0;
		for (int i = 0; i < tableau[1].length; ++i) {
			for (int j = 0; j < tableau.length; ++j) {
				if (tableau[j][i] >= moyenne) {
					sup[increment] = tableau[j][i];
					++increment;
				}
			}
		}
		return sup;
	}
	
	public static double tri(double tableau[][], int valeurs) {
		double [] tableau_a_plat = new double [valeurs];
		
		return 0;
	}
	

}

