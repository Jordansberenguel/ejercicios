# ejercicios
public class Ejer3 {

    public static void main(String[] args) throws IOException {
        
        BufferedReader in = new BufferedReader(new InputStreamReader(System.in));        
        int cont1=0,cont2=0, cont3=0, ca1=5, ca2=15, ca3=25;
        int acu1=0, acu2=0, acu3=0;
        int edad=0, mt=0;
        String tecla_repetir;
        
            
     do{         
       System.out.println("Ingresa tu edad: ");
               
         do{
             edad = Integer.parseInt(in.readLine());
             if(edad<0||edad>100)
            System.out.print("Valor incorrecto. Ingresalo nuevamente.: ");  
            
         }  
        while(edad <0|| edad >100);         
                     
           if(edad >= 0 && edad <=10){ 
            acu1=acu1+ca1;             
           cont1=cont1+1;
           
          }          
          if(edad >= 11 && edad <=18){ 
           acu2=acu2+ca2;             
           cont2=cont2+1;
           
          }
          if(edad>18){ 
           acu3=acu3+ca3;             
           cont3=cont3+1;         
          
        }  
            mt=acu1+acu2+acu3;
          do{
              System.out.print("Confirmar si hay o no más personas que desean entrada a la feria ? (S/N): ");
                tecla_repetir = in.readLine();
          }
          while (!tecla_repetir.equalsIgnoreCase("s") && !tecla_repetir.equalsIgnoreCase("n"));
        } while (tecla_repetir.equalsIgnoreCase("s"));
              
         System.out.println("Cantidad de entradas vendidas rango de 0 a 10 = " + cont1);
         System.out.println("Cantidas de entradas vendidas rango de 11 a 18  = " + cont2 );
         System.out.println("Cantidad de entradas vendidas de 19 a mas = " + cont3);
         System.out.println("Monto acumulado de ventas = " + "S/" + mt);
      
   }
}
