# Clase de Programación Orientada a Objetos
### Unidad 3

public class Auto {
    private String marca;
    private String modelo;
    private String tipo;
    
    //constructores

    public Auto() {
    }

    public Auto(String marca, String modelo, String tipo) {
        this.marca = marca;
        this.modelo = modelo;
        this.tipo = tipo;
    }
    

    
    //setter and getter
    public String getMarca() {
        return marca;
    }

    public void setMarca(String marca) {
        this.marca = marca;
    }

    public String getModelo() {
        return modelo;
    }

    public void setModelo(String modelo) {
        this.modelo = modelo;
    }

    public String getTipo() {
        return tipo;
    }

    public void setTipo(String tipo) {
        this.tipo = tipo;
    }

    @Override
    public String toString() {
        return "Auto{" + "marca=" + marca + ", modelo=" + modelo + ", tipo=" + tipo + '}';
    }
    
    
    
}
#######SUBCLASE SEDAN

package Automovil;

public class Sedan extends Auto {
    private String volumen;
    private int puertas;
    
    //constructores

    public Sedan() {
    }

    public Sedan(String volumen, int puertas, String marca, String modelo, String tipo) {
        super(marca, modelo, tipo);
        this.volumen = volumen;
        this.puertas = puertas;
    }

    Sedan(String sedan, String honda_Civic_del_Sol, String c) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    } 
    
    //setter and getter

    public String getVolumen() {
        return volumen;
    }

    public void setVolumen(String volumen) throws Exception {
        if(volumen.trim().isEmpty()){
            throw new Exception ("ES OBLIGATORIO ESPECIFICAR");
            
        }
        this.volumen = volumen;
    }

    public int getPuertas() {
        return puertas;
    }

    public void setPuertas(int puertas) throws Exception {
            if((puertas >=2 && puertas <=4)){
                throw new Exception ("Por favor seleccione numero de puertas");
            }
        this.puertas = puertas;
    }

    @Override
    public String toString() {
        return super.toString() + "Sedan{" + "volumen=" + volumen + ", puertas=" + puertas + '}';
    }


   
    
}
######SUBCLASE DEPORTIVO
public class Deportivo extends Auto {
    private String puertas;
    private String descapotable;
    
    //constructores

    public Deportivo() {
    }

    public Deportivo(String puertas, String descapotable, String marca, String modelo, String tipo) {
        super(marca, modelo, tipo);
        this.puertas = puertas;
        this.descapotable = descapotable;
    }
    
    
    //setter and getter

    public String getPuertas() {
        return puertas;
    }

    public void setPuertas(String puertas) {
        this.puertas = puertas;
    }

    public String getDescapotable() {
        return descapotable;
    }

    public void setDescapotable(String descapotable) {
        this.descapotable = descapotable;
    }

    @Override
    public String toString() {
        return super.toString () + "Deportivo{" + "puertas=" + puertas + ", descapotable=" + descapotable + '}';
    }
    
    
}
#######SUBCLLASE MOTOCICLETA
package Automovil;

public class Motocicleta extends Auto {
    private String color;
    private String velocidad;
    private String motor;
    
    //constructores

    public Motocicleta() {
    }

    public Motocicleta(String marca, String modelo, String tipo) {
        super(marca, modelo, tipo);
    }

    public Motocicleta(String color, String velocidad, String motor, String marca, String modelo, String tipo) {
        super(marca, modelo, tipo);
        this.color = color;
        this.velocidad = velocidad;
        this.motor = motor;
    }

    
    //setter and getter
    public String getColor() {
        return color;
    }

    public void setColor(String color) throws java.lang.Exception {
        if(color.trim().isEmpty()){
            throw new Exception ("Seleccione un color");
            
        }
        this.color = color;
    }

    public String getVelocidad() {
        return velocidad;
    }

    public void setVelocidad(String velocidad) throws java.lang.Exception {
        if(velocidad.trim().isEmpty()){
            throw new Exception ("ES OBLIGATORIA UNA RESPUESTA");
            
        }
        this.velocidad = velocidad;
    }

    public String getMotor() {
        return motor;
    }

    public void setMotor(String motor) throws java.lang.Exception {
        if(motor.trim().isEmpty()){
            throw new Exception("ES OBLIGATORIO RESPODER");
            
        }
        this.motor = motor;
    }

    private Exception Exception(String seleccione_un_color) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

}
####SUBCLASE CAMIONETA
package Automovil;

/**
 *
 * @author danie
 */
public class Camioneta extends Auto {
    private String tamano;
    private String color;
    
    //constr

    public Camioneta() {
    }

    public Camioneta(String tamano, String color, String marca, String modelo, String tipo) {
        super(marca, modelo, tipo);
        this.tamano = tamano;
        this.color = color;
    }
    
    
    //getter and setter

    public String getTamano() {
        return tamano;
    }

    public void setTamano(String tamano) throws java.lang.Exception {
        if (tamano.trim().isEmpty()){
            throw Exception ("POR FAVOR ESPECIFIQUE UN TAMANO");          
        }
        this.tamano = tamano;
    }

    public String getColor() {
        return color;
    }

    public void setColor(String color) throws java.lang.Exception {
        if(color.trim().isEmpty()){
            throw new Exception ("ESCOJA UN COLOR");
            
        }
        this.color = color;
    }

    @Override
    public String toString() {
        return super.toString() + "Camioneta{" + "tamano=" + tamano + ", color=" + color + '}';
    }

    private Exception Exception(String por_favor_especifique_un_tamano) {
        throw new UnsupportedOperationException("Especificar"); //To change body of generated methods, choose Tools | Templates.
    }
    
    
}
#########TEST MENU
package Automovil;

import java.util.Scanner;
import java.util.logging.Level;
import java.util.logging.Logger;

public class Test {

    public static void main(String[] args) {
        Scanner in = new Scanner (System.in);
        String opcion; 
    do{
        System.out.println("--BIENVENIDO AL MUNDO DEL AUTO--");
        System.out.println("¿QUÉ ACCION QUIERE REALIZAR?");
        System.out.println("[P]PAGAR AUTO");
        System.out.println("[V]VER AUTOMOVILES");
        System.out.println("[S]SALIR DE LA PAGINA");
        
        System.out.println("Ingresar opcion");
        opcion = in.nextLine();
        System.out.println(opcion.toLowerCase());
        
        switch(opcion.toLowerCase()) {
            case "p" :
                int cantidad;
                System.out.println("Ingresar cantidad a pagar");
                cantidad = in.nextInt();
                    System.out.println("Usted pagó: " + cantidad);
                        break;
            case "v":
                int ver;
         do{       
                System.out.println("Seleccionar tipo de automovil que desea ver");
                System.out.println("[1] SEDAN");
                System.out.println("[2] DEPORTIVO");
                System.out.println("[3] MOTOCICLETA");
                System.out.println("[4] CAMIONETA");
                System.out.println("[5] REGRESAR AL MENU PRINCIPAL");
                ver = in.nextInt();
                    switch(ver){
                        case 1:
                            Sedan s1 = new Sedan();
                            s1.setMarca("X");
                            s1.setModelo("2010");
                            s1.setTipo("Lujo");
            {
                try {
                    s1.setPuertas(3);
                    s1.setVolumen("3 volumenes");                    
                } catch (Exception ex) {
                System.out.println(ex.getMessage());
                }
            }
                            System.out.println(s1);
                            System.out.println("USTED SE ENCUENTRA EN LA SECCION DE SEDAN");
                           break;

                        case 2:
                            Deportivo d1 = new Deportivo();
                            d1.setMarca("Porshe");
                            d1.setModelo("xxxx");
                            d1.setTipo("aaa");
            {
                try {
                    d1.setPuertas("2");
                    d1.setDescapotable("Si");
                } catch (Exception ex) {
                System.out.println(ex.getMessage());
                }
            }
                            System.out.println(d1);
                            System.out.println("USTED SE ENCUENTRA EN LA SECCION DE DEPORTIVOS");
                            
                            break;

                        case 3:
                            Motocicleta m1 = new Motocicleta();
            {
                try {
                    m1.setColor("Roja");
                    m1.setMotor("4 tiempos");
                    m1.setVelocidad("");
                } catch (Exception ex) {
                    System.out.println(ex.getMessage());
                }
            }
                            System.out.println(m1);
                            System.out.println("USTED SE ENCUENTRA EN LA SECCION DE MOTOCICLETAS");
                            break;

                        case 4:
                            Camioneta c1 = new Camioneta();
            {
                try {
                    c1.setColor("ROJO");
                    c1.setTamano("XHSXSJ");                    
                } catch (Exception ex) {
                    System.out.println(ex.getMessage());
                }
                            System.out.println(c1);
                            System.out.println("USTED SE ENCUENTRA EN LA SECCION DE DCAMIONETAS");
            }
                            break;

                        case 5:
                            System.out.println("GRACIAS!");
                            break;
                        default:
                            System.out.println("Por favor elija una opcion valida");
     } 
         }while(ver !=5);
         break;
            case "s":
                System.out.println("ESPERAMOS NOS VISITE PRONTO");
     }
    }while(!opcion.equals("S"));
    }
}
