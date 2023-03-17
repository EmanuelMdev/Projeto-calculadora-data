import java.util.Scanner;
public class somadehorarios {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		
		System.out.println("Que dia é hoje? (Ex: 23 de janeiro)");
		String dia = input.nextLine();
		
		System.out.println("Digite a hora (entrada)");
		int h1 = input.nextInt();
		
		while (h1 > 23) {
			System.out.println("Invalido, digite novamente");
			h1 = input.nextInt();
		}
		while (h1 < 0) {
			System.out.println("Invalido, digite novamente");
			h1 = input.nextInt();
		}
		System.out.println("Digite os minutos (entrada)");
		int m1 = input.nextInt();
		
		while (m1 > 59) {
			System.out.println("Invalido, digite novamente");
			m1 = input.nextInt();
		}
		while (m1 < 0) {
			System.out.println("Invalido, digite novamente");
			m1 = input.nextInt();
		}
		System.out.println("Digite a hora (saída)");
		int h2 = input.nextInt();
		
		while (h2 < 0) {
			System.out.println("Invalido, digite novamente");
			h2 = input.nextInt();
		}
		while (h2 > 23) {
			System.out.println("Invalido, digite novamente");
			h2 = input.nextInt();
		}
		  while (h2 < h1) {
		    	System.out.println("Invalido, digite novamente");
		    	h2 = input.nextInt();
		    }
		  
		System.out.println("Digite os minutos (saída)");
		int m2 = input.nextInt();
		
		while (m2 > 59) {
			System.out.println("Invalido, digite novamente");
			m2 = input.nextInt();
		}
		while (m2 < 0) {
			System.out.println("Invalido, digite novamente");
			m2 = input.nextInt();
		}
		int htotal = (h1 - h2) * -1;
		int mtotal = (m1 - m2);
		
		if (m1 < m2) {
			mtotal = mtotal * -1;
		}
		
		if (mtotal > 59) {
			htotal = htotal + 1;
		} 
		if (htotal > 4) {
			htotal = htotal - 4;
			System.out.println("Dia " + dia + " você trabalhou mais do que seu horario um total de " + htotal +"hr" + " e "+ mtotal + " min");
		} else {
			System.out.println("Dia " + dia + " você trabalhou por " + htotal +"hr" + " e "+ mtotal + " min");
		}
	}
}