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
