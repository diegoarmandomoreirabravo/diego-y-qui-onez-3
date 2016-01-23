# diego-y-qui-onez-3
repositorio de leer texto en java

import java.io.*;
 
class LeeFichero {
   public static void main(String [] arg) {
      File archivo = null;
      FileReader fr = null;
      BufferedReader br = null;
 
      try {
         // Apertura del fichero y creacion de BufferedReader para poder
         // hacer una lectura comoda (disponer del metodo readLine()).
         archivo = new File ("C:\\archivo.txt");
         fr = new FileReader (archivo);
         br = new BufferedReader(fr);
 
         // Lectura del fichero
         String linea;
         while((linea=br.readLine())!=null)
            System.out.println(linea);
      }
      catch(Exception e){
         e.printStackTrace();
      }finally{
         // En el finally cerramos el fichero, para asegurarnos
         // que se cierra tanto si todo va bien como si salta 
         // una excepcion.
         try{                    
            if( null != fr ){   
               fr.close();     
            }                  
         }catch (Exception e2){ 
            e2.printStackTrace();
         }
      }
   }
}





package com.mycompany.login;

import java.io.FileReader;
import java.io.BufferedReader;
public class leertxt {
    public static void main (String arg[]){
    String txt="";
    try {
    FileReader lectura = new FileReader ("txt.txt");
    BufferedReader almacenado = new BufferedReader (lectura);
    
    while((txt = almacenado.readLine())!=null){
    System.out.println(txt);
    }
   
    }
    catch (Exception e){
    System.out.println("usuario o contraseña incorrecto");
    }
    }   
    
}


