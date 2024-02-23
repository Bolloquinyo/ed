/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package com.mycompany.mainrefugiocanino;

/**
 *
 * @author DAM102
 */
public class RefugioCanino {

    private String[] nombresPerros;
    private String[] razasPerros;
    private int cantidadPerros;

    public RefugioCanino() {
        nombresPerros = new String[100];
        razasPerros = new String[100];
        cantidadPerros = 0;
    }

    // Método para agregar un perro al refugio
    public void agregarPerro(String nombre, String raza) {
        nombresPerros[cantidadPerros] = nombre;
        razasPerros[cantidadPerros] = raza;
        cantidadPerros++;
    }

    // Método para mostrar la lista de perros en el refugio
    public void mostrarPerros() {
        for (int i = 0; i < cantidadPerros; i++) {
            System.out.println("Nombre: " + nombresPerros[i] + ", Raza: " + razasPerros[i]);
        }
    }


    /*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */
package com.mycompany.mainrefugiocanino;

/**
 *
 * @author DAM102
 */
public class MainRefugioCanino {

    public static void main(String[] args) {

        System.out.println("Bienvenido a la base de datos del refugio");

        // Crear una instancia del refugio
        RefugioCanino refugio = new RefugioCanino();

        // Agregar algunos perros al refugio
        refugio.agregarPerro("Max", "Labrador");
        refugio.agregarPerro("Bella", "Pastor Alemán");
        refugio.agregarPerro("Toby", "Husky");

        // Mostrar la lista de perros en el refugio
        System.out.println("\nLista de perros en el refugio:");
        refugio.mostrarPerros();

        // Obtener y mostrar el número de perros en el refugio
        int numeroDePerros = refugio.obtenerNumeroDePerros();
        System.out.println("\nNúmero de perros en el refugio: " + numeroDePerros);

    }
}
    

    // Método para obtener el número de perros en el refugio
    public int obtenerNumeroDePerros() {
        return cantidadPerros;
    }
}
