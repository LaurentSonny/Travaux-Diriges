# Travaux-Diriges
Tous les TD {

public class Class_6 {

	public static void part1(String[] args) {
		Guitare guitare1;
		GuitareElectrique guitareelec1;
		guitare1 = new Guitare("guitare", 6, "gling");
		guitareelec1 = new GuitareElectrique("guitare electrique", 6, "gling");
		guitare1.jouer();
		guitareelec1.jouer()
public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
			System.out.println(son.toUpperCase());
		}
	}

}
;
		guitareelec1.jouer();

	}

	public static void main(String[] args) {
		Instrument[] tabguitare = new Instrument[4];
		for (int i = 0; i < tabguitare.length - 2; ++i) {
			tabguitare[i] = new Guitare("guitare " + i, 6, "ayy");
		}
		for (int i = 2; i < tabguitare.length; ++i) {
			tabguitare[i] = new GuitareElectrique("guitare electrique " + i, 4, "rho");
		}
		for (int i = 0; i < tabguitare.length; ++i) {
			tabguitare[i].nom();
			tabguitare[i].jouer();
		}
	}

}

public interface Instrument {

	public void jouer();
	public void nom();

}



public class Guitare implements Instrument {
	int nombrecordes;
	String son;
	String nom;

	public Guitare(String nom, int nombrecordes, String son) {
		this.nom = nom;
		this.son = son;
		this.nombrecordes = nombrecordes;
	}

	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
			System.out.println(son);
		}
	}

	public void nom() {
		System.out.println(nom);
	}
}


public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
			System.out.println(son.toUpperCase());
		}
	}
public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
			System.out.println(son.toUpperCase());
		}
	}
public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
public class GuitareElectrique extends Guitare {

	public GuitareElectrique(String nom, int nombrecordes, String son) {
		super(nom, nombrecordes, son);
		// TODO Auto-generated constructor stub
	}
	public void jouer() {
		for (int i = 0; i < nombrecordes; ++i) {
			System.out.println(son.toUpperCase());
		}
	}

}

			System.out.println(son.toUpperCase());
		}
	}

}


}

			System.out.println(son.toUpperCase());
		}
	}

}


}

}
