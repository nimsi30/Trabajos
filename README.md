# Trabajos
import javax.swing.JOptionPane;
public class Try_1 {
	String mensaje;

	{

    	String valorCadena=JOptionPane.showInputDialog(null,"Qué tabla de multiplicar desea");

    	try{

    		int valorEntero=Integer.parseInt(valorCadena);

    		mensaje= "Tabla del "+valorCadena+"\n";

    		for(int i=1;i<=10;i++){


    			mensaje=mensaje+i+"x"+valorCadena+"="+(i*valorEntero)+"\n";

    		}

    	}catch(NumberFormatException ex){

    		mensaje="No es un entero";

    	}

    	JOptionPane.showMessageDialog(null,mensaje);

    }

    public static void main(String[] args) {

        new Try_1();

    }

}  
public class Try_2 {
    public static void main(String arg[])
    {
        int [] array = new int[20];
        try
        {

	         String s = null;
	         s.equals("QQQQ");
        }
        catch(ArrayIndexOutOfBoundsException excepcion)
        {
	         System.out.println(" Error de índice en un array");
        }
        catch(ArithmeticException excepcion)
        {
	         System.out.println(" Error de índice en un array");
        }
        catch(Exception excepcion)
        {
	         System.out.println("Se ha generado un error que no es de índices, ni Aritmético");
	         System.out.println("El objeto error es de tipo " + excepcion);
        }
    }
}
import java.util.Scanner;
public class Try_3 {
	 public static void main(String[] args) {
	    	Scanner sc = new Scanner(System.in);
		    String n = "";

		    String mensaje = "";
		    	
		    	
		    		
		    	try{
		    		System.out.println("Escriba la calificación con número");	
		    		n=sc.nextLine();
		    		int califNum=Integer.parseInt(n);


		    		String calif;

		    		switch(califNum){

		    			
		    			case 0: calif="NA";break;

		    			case 1: calif="NA";break;

		    			case 2: calif="NA";break;

		    			case 3: calif="NA";break;

		    			case 4: calif="NA";break;

		    			case 5: calif="NA";break;

		    			case 6: calif="S";break;

		    			case 7: calif="S";break;

		    			case 8: calif="B";break;

		    			case 9: calif="MB";break;

		    			case 10: calif="MB";break;

		    			default: calif="Inválida";break;
				

		    		}

		    		mensaje="La calificación es: "+calif; 

		    	}catch(NumberFormatException ex){

		    		mensaje="No escribió un número";

		    	}

		    	System.out.println(mensaje);
		    	
		    	
		}



		}  
import java.util.InputMismatchException;
import java.util.Scanner;
public class Try_4 {
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
	    int [] array = {4,2,6,7};
	    int n;
	    boolean repetir = false;
	    do{
	         try{
	                repetir = false;
	                System.out.print("Introduce un número entero > 0 y < " + array.length + " ");
	                n = sc.nextInt();
	                System.out.println("Valor en la posición " + n + ": " + array[n]);
	         }catch(InputMismatchException e){
	                   sc.nextLine();
	                   n = 0;
	                   System.out.println("Debe introducir un número entero ");
	                   repetir = true;
	         }catch(IndexOutOfBoundsException e){
	                  System.out.println("Debe introducir un número entero > 0 y < " + array.length + " ");
	                  repetir = true;
	         }catch(Exception e){ 
	                   System.out.println("Error inesperado " + e.toString());
	                   repetir = true;
	         }
	     }while(repetir);
	}
}
import java.util.InputMismatchException;
import java.util.Scanner;

public class Try_5 {

	public static void main(String[] args) {
	     Scanner sc = new Scanner(System.in);
	     int n1, n2;
	     try {
	            System.out.print("Introduce un número: ");
	            n1 = sc.nextInt();
	            try {
	                    System.out.print("Introduce otro número: ");
	                    n2 = sc.nextInt();
	                    System.out.println(n1 + " / " + n2 + " = " + n1/(double)n2);
	            }catch (InputMismatchException e) {
	                       sc.nextLine();
	                       n2 = 0;
	                       System.out.println("Debe introducir un número");
	            }catch (ArithmeticException e) {
	                       sc.nextLine();
	                       n2 = 0;
	                       System.out.println("No se puede dividir por cero");
	            }
	     }catch (InputMismatchException  e) {
	                sc.nextLine();
	                n1 = 0;
	                System.out.println("Debe introducir un número");
	     }
	}

}
import java.util.Calendar;
	import java.util.GregorianCalendar;
	import java.util.InputMismatchException;
	import java.util.Scanner;
public class try_6 {
	

		public static void main(String[] args) {
			Scanner sc = new Scanner(System.in);
		    int n;
			int añoNacimiento = 0;
		    try{
		    	Calendar fecha = new GregorianCalendar();
		    	int año = fecha.get(Calendar.YEAR);
		    		    	
	            System.out.print("Introduce la edad que cumpliras este año: ");
	            n = sc.nextInt();
	            añoNacimiento = año-n; 
	            System.out.println("naciste en el año " + añoNacimiento);
	            
	     }catch(InputMismatchException e){
	                  sc.nextLine();
	                  n = 0;
	                  System.out.println("Debe introducir un número entero " + e.toString());
	     }finally{
	    	 System.out.println("\nFin del proceso");
	     }

	}
	}
public class Try_7 {
	

		public static void main(String[] args) {
			int cantidad  = 0;
			int cantidad2 = 0;
			double resultado = 0;
			cantidad  = 0; 
			cantidad2 = 10;
			
			try {
				resultado =  (cantidad2*100)/cantidad;
				System.out.println("la cantidad "+cantidad2+" es el "+resultado+"% de "+cantidad);
			} catch (ArithmeticException e) {
				System.out.println("Error la cantidad total no debe de ser 0 \n"+e);
			}finally{
				System.out.println("\nFin del proceso");
			}
			
		}

	}
import javax.swing.*;
public class Try_8 {
	public static void main(String args[]){
		String numero;
		int num;
		try {
			numero=JOptionPane.showInputDialog(null, "Ingrese un numero para ser sumado con 3",numero, JOptionPane.QUESTION_MESSAGE);
			num=Integer.parseInt(numero);

			num+=3;
			JOptionPane.showMessageDialog(null,"Excalente, el resultado de 3 +"+numero+" = "+num,"Error",JOptionPane.INFORMATION_MESSAGE);
			
		}catch(NumberFormatException ex){
			JOptionPane.showMessageDialog(null,"Atencion a ingresado un caracter NO numerico","Error",JOptionPane.ERROR_MESSAGE);
		}
		System.exit(0);
	}
 
}
import javax.swing.JOptionPane;
public class Try_9 {
	public static void main(String args[]){
		
		String strNumero1 = JOptionPane.showInputDialog("Ingrese el numero 1");
		String strNumero2 = JOptionPane.showInputDialog("Ingrese el numero 2");
		try{
			int numero1 = Integer.parseInt(strNumero1);
			int numero2 = Integer.parseInt(strNumero2);
			int suma = numero1 + numero2;
			
			JOptionPane.showMessageDialog(null,"La suma es: "+suma);
			
		}catch(NumberFormatException ex){
			JOptionPane.showMessageDialog(null,"Error solo numeros");
		}finally{
			System.out.println("Ese es el final y siempre se ejecuta ");
		}
	}

}
public class Try_10 {
	public static void main(String args[]){
		System.out.println("Inicio del programa");
		metodoX();
		System.out.println("Final del programa");
	}
public static void metodoX(){
	try {
		int x = Integer.parseInt("3");
		System.out.println("Valor de x = "+x);
	}catch (Exception e){
		e.printStackTrace();
	}
	System.out.println("Se produjo un error");

}


}
import java.util.Scanner;
public class Try_11 {
	public static void main(String args[]){
	    Scanner sc = new Scanner(System.in);
		int distancia = 1;
		int velocidad=0;
		int tiempo=0;
		System.out.println("Ingresa el valor de la distancia");
		distancia = sc.nextInt();
		System.out.println("Ingresa el valor del tiempo");
		tiempo = sc.nextInt();
		
		
		try {
			System.out.println("El valor de la velocidad es: ");
			
			velocidad = distancia/tiempo;
			
			System.out.println(velocidad);
			
		} catch (ArithmeticException e) {
			System.out.println("Error la velocidad no puede ser "+velocidad+" no se puede dividi entre 0 ");
		}finally{
			System.out.println("Fin del proceso");
		}
		
		}
}
import java.util.Scanner;
public class Try_12 {
	public static void main(String args[]){
		Scanner sc = new Scanner(System.in);
		int densidad =0;
		int masa=0;
		int volumen = 0;
		System.out.println("Ingresa el valor de la masa");
		masa = sc.nextInt();
		System.out.println("Ingresa el valor del volumen");
		volumen = sc.nextInt();
		
		
		try {
			System.out.println("Programa para calcular la densidad de un material");
			
			densidad= masa/volumen;
			System.out.println("densidad = "+densidad+" gr / cm3");
		} catch (ArithmeticException e) {
			System.out.println("Error la masa no puede ser "+masa);
		}finally{
			System.out.println("fin del proceso");
		}
	}
import java.util.Scanner;

public class Try_13 {
	public static void main(String args[]){
		Scanner sc = new Scanner(System.in);
		int tiempo=0;
		int velocidad=0;
		int distancia=1;
		
		System.out.println("Ingresa el valor de la distancia");
		distancia = sc.nextInt();
		System.out.println("Ingresa el valor de la velocidad");
		velocidad = sc.nextInt();
		try {
			System.out.println("Programa para calcular la velocidad - Formula Tiempo=Distancia/Velocidad");
			tiempo=distancia/velocidad;
			System.out.println("El tiempo es. "+tiempo);
		} catch (ArithmeticException e) {
			System.out.println("Error la velocidad no puede ser "+velocidad+" no se puede dividi entre 0 ");
		}finally{
			System.out.println("Fin del proceso");
		}
		
		
	}

}

