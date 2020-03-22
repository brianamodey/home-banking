# Calculo de IVA
Calculo de IVA para aplicacion Web




\*Proyecto en etapa inicial\\





codigo en el cual se hace la creacion de una factura por medio de java netbeans 
primero se trae la libreria Scanner luego se piden los datos del usuario capturando con variables String se hace un metodo calcular iva donde se hace la operacion para calcular el total que es multiplicar el costo del producto con la cantidad del producto, luego se hace el iva que es el total multiplicado por 21 y dividido entre 100 despues se suma el total mas el iva y en un system.out.println se muestra el total de la suma; tambien se crea un metodo factura dentro de este ahi un system.out.println mostrando todos los datos que digito del usuario con su factura mas el iva.

EXCEPCIONES:
en el momento que el usuario entra en la opcion de digitar cantidad se crea un while donde lo que digito el usuario es menor a 1, mandaria un system.out.println diciendo que digite valores validos ya que si no se pondria esta excepcion a la hora de multiplicar costo por cantidad daria 0 y su factura seria 0 y la misma operacion con costo de unidad.

public class main {
 static String direc,nom,tel;
       static int cantidad,id, habitaciones;
       static double costo;
        static double iva, total;
        static double tot;
        static String personas;
 
    public static void main(String[] args) {
   
       Scanner sc= new Scanner (System.in);
         System.out.println("digite nombre: ");
        nom=sc.next();
        System.out.println("digite direccion: ");
        direc=sc.next();
        System.out.println("digite telefono: ");
        tel=sc.next();
        System.out.println("digite identificacion: ");
        id=sc.nextInt();  
       System.out.println("digite cantidad");
        cantidad=sc.nextInt();
        while(cantidad<1){
            System.out.println("digite valores validos " );
            cantidad=sc.nextInt();
        }
        System.out.println("digite costo unidad");
        costo=sc.nextInt();
     
        while(costo<1){
            System.out.println("digite valores validos " );
            costo=sc.nextInt();
        }
       factura();
       calcularIva();
    }

    public static void factura(){
   

 
    System.out.println("su factura es " + "\n" +" nombre "  + nom + "\n" + "direccion " + direc + "\n" + "telefono " + tel + "\n" + "idenficacion " + id + "\n" + "costo unidad "+ costo +"\n" );
 }
    public static void calcularIva(){
         total = costo*cantidad;
        iva=(total*21)/100;
        tot=total+iva;
        System.out.println("costo total " + tot);
    }
}
