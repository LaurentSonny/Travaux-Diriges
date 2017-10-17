# Travaux-Diriges
TD 4
public class Class_4 {
	
	public static void main(String[] args) {
		int[] tableau = Generateur(10);
		int long_tab=tableau.length-1;
		System.out.print("Tableau non trié : ");
		Affichage(tableau);
		tableau=Trier(tableau,0,long_tab);
		System.out.print("Tableau trié : ");
		Affichage(tableau);
	}

	public static int [] Trier(int[] tableau, int debut, int fin) {
		int milieu = debut + ((int) ((fin - debut) / 2));
		if (fin - debut == 1) {
			int tampon = 0;
			if (tableau[debut] > tableau[fin]) {
				tampon = tableau[debut];
				tableau[debut] = tableau[fin];
				tableau[fin] = tampon;
				return (tableau);
			}
		}
		else {
			return (Trier(tableau, debut, milieu));
		}
		return (Trier(tableau, milieu, fin));
	}

	public static void Affichage(int[] tableau) {
		System.out.print("|");
		for (int i : tableau) {
			System.out.print(i + "|");
		}
		System.out.print("\r\n");
	}

	public static int[] Generateur(int longueur) {
		int[] tab = new int[longueur];
		for (int i = 0; i < longueur; ++i) {
			tab[i] = (int) (Math.random() * 10);
		}
		return (tab);
	}
}
