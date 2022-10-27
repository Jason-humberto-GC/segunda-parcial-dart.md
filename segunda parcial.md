<img src="https://siceuc2.ucol.mx/becatitulaciongobiernodelestado/Assets/images/03UdeC_publi_80.png">

# Universidad de Colima 
## Facultad de Ingeniería Mecánica y Eléctrica 
### "Ingenieria en Computacion Inteligente"
### Alumno:
  * Jason Humberto Garcia Camacho 
### Maestro:
  *  Walter Alexander Mata Lopez
--------------------------------------------------
# Portafolio De Programas Relalizados En La Segunda Parcial En Lenguage Dart
-----------------------------------------------------
## Impresión de un "hola mundo"

     void main() {
      print("hola mundo");
     } 
--------------------------------------------------------
## Declaracion de Variables 

 Maneja un tipado  explicito 
 
 Tipo Entero
 Sirve para datos de tipo entero sin decimales  
 
    void main() {
     int miEntero = 10;
     print(miEntero);
    }
 
 Tipo Flotante 
 Sirve para datos con decimales 
 
    void main() {
     double miDouble = 3.1416;
     print(miDouble);
    }
 
 Tipo Numerico
 Este sirve para cuando no se sabe que tipo de dato es el que se va a emplear: int y double;
 tambien conocida como una super clase, por el hecho de que facilita al programador la
 captura de un dato ya sea entero o decimal.
 
     void main() {
      num miNumero1 = 10;
      num miNumero2 = 3.1416;
     
      print(miNumero1);
      print(miNumero2);
     } 

Tipo String

     void main() {
      String miString = "hola";
      print(miString);
     } 
  
Tipo Dynamic
 Es conocido como tipo de dato dinamico; Este se utiliza cunado no sabes que tipo de dato es el que vas utilizar,
 puede contener datos del tipo entero, decimal y texto.

     void main() {
      dynamic miDinamico = "hola";
      print(miDinamico);
      dynamic miDinamico1 = 3.1416;
      print(miDinamico1);
     }
     
 Tipo final 
 se utliza para que eldato no se pueda cambiar ("tiempo de ejecucion".
       
      void main() { 
      final double miPI = 3.1416;  
      print(miPI);
      }
      
      
 ------------------------------------------------------------------------------------------------------------------
 
 ## Verificar un tipo de dato 
Esto se utliza para verificar si un tipo de dato  esta correctamente declarado ya sea entero,double,num o String,
al momento de imprimir te arroja si el dato es falso o verdadero

Ejemplo: 
" print("nombre de la variable" is "tipo de dato"); "

     void main() {
      int miEntero = 10;
      print(miEntero is int);                         //verdadero
  
      double miDouble = 3.1416;
      print(miDouble is double);                     //verdadero
      print(miEntero is double);                     //verdadero

      num miNumero1 = 10;
      num miNumero2 = 3.1416;

      print(miNumero1 is num);                      //verdadero
      print(miNumero2 is num);                      //verdadero

      String miString = "hola";
      print(miString is String);                     //verdadero
      
      bool miBool = true;                           
      print(!miBool);                                //false
      
      bool miBool = true;                           
      print(miBool);                                 //verdadero
     }
     
!! Nota: el dinamico ("dynamic") no se puede verificar que tipo de dato es porque  puede ser utlizado en varios
tipos de datos.!!

!! Nota: el tipop bool es para representar valores booleanos: true y false. !!

---------------------------------------------------------------------------------------------------------------------

## Declaracion de contantes 
Se declara el valor deesde el inicio para que funcione bien  ("tiempo de compilacion")

    void main() {
    const double miPI = 3.1416;   ///declarion de constante de manera explicita 
    print(miPI);
    }
    
 -------------------------------------------------------------------------------------------------------
 
 ## RuntimeType
 verifica el dato en timpo de ejecucioón y muestra el tipo de dato que esta utilizando al moento de ejecutar el programa 
 
    void main() {
    num miNumero;
    miNumero = 3.1416;
    print(miNumero
      .runtimeType); //timpo de ejecucion  y muestra que tipo de dato es double

    dynamic midinamico;
    midinamico = 5;
    print(midinamico
      .runtimeType); //timpo de ejecucion  y muestra que tipo de dato es   int.

    dynamic miDinamico;
    miDinamico = "5";
    print(miDinamico
      .runtimeType); //timpo de ejecucion  y muestra que tipo de dato es  string.
    }
 
 ----------------------------------------------------------------------------------------------------------------
 
 ## Declaracion con var  (inferencia de tipo)
 verifacr tipo de variables: 
 
    void main(List<String> args) {
    var numero1 = 100;      //int
    var numero2 = 9.81;      //double
    var nombre = "jason";   //string
    
    print(numero1.runtimeType);
    print(numero2.runtimeType);
    print(nombre.runtimeType);
    }
 -------------------------------------------------------------------------------------------------------------------
 
 ## casting o convercion de tipos 
 
 
    void main(List<String> args) {
     var numero1 = 100; //tipo int
     var numero2 = 9.81; //tipo double
     
     var resultado;   //dinamic

     resultado = numero1 + numero2;
     print(resultado.runtimeType);  //double
    }
 -----------------------------------------------------------------------------------------------------------------
 
 
