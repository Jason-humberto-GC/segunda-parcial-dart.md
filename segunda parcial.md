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
## imprecion de varios renglones 


    void main(List<String> args) {
     print("en lugar de\n"
       "la mancha de cuyo\n"
       "mombre no quiero acordarme");
    }
-------------------------------------------------------------
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
 
 ## casting o convercion de tipos de datos 
 
 
    void main(List<String> args) {
     var numero1 = 100; //tipo int
     var numero2 = 9.81; //tipo double
     
     var resultado;   //dinamic

     resultado = numero1 + numero2;
     print(resultado.runtimeType);  //double
    }
    
    
  convercion de resultado   double a int 
  
    void main(List<String> args) {
    const numero1 = 19.5;
    const numero2 = 10;
    final total = (numero1 * numero2).toInt();
    print(total);  
    }
    
 -----------------------------------------------------------------------------------------------------------------
 
 ## Numeros en distintas bases
 
 Multiplicionde numeros hexadecimales 
 
    void main(List<String> args) {
    int nHexa1 = 0xF;
    int nHexa2 = 0xF;

    print(nHexa1 * nHexa2);
    }
    
    
 Numeros Octales
 
    void main(List<String> args) {
    var nOctal = 125.toRadixString(8);   // este no se puede mutiplicar 
    print(nOctal);
    
    var nH = 125.toRadixString(16);
    print(nH); 
    } 
 -------------------------------------------------------------------------------------------------------------
 
 ## Strings
 
    void main(List<String> args) {
    String nombreCurso = "programacion funcional";

    String carrera = "Ici";

    print(carrera + " " + nombreCurso); 
     }
     
     
     
    void main(List<String> args) {
    String nombreCurso = "programacion funcional";

    String carrera = "Ici";

    print(carrera + " " + nombreCurso);
    var num = 4;
    // interpolación de cadenas
    print("$carrera $nombreCurso");
    print(
      "${carrera} ${nombreCurso}"); //se utliza en operaciones y para llamar funciones
    print("el cuadrado de $num es ${num * num}");
    print("el cuadrado de $num es ${cuadrado(num)}");
    }

    String getCarrera() {
       return "ICI";
    }

    Int cuadrado(int num) {
    return num * num;
    }
    
---------------------------------------------------------------------

## Listas 

    void main(List<String> args) {
     final calificaciones = []; // lista vacia
     print(calificaciones);
     calificaciones.add(2);
    }
    
Agrgar un dato a la lista (.add)

    void main(List<String> args) {
    final calificaciones = [10,6,9, 8,10,8]; 
    print(calificaciones);
    calificaciones.add(2);   // agrgar un dato a la lista 
    print(calificaciones);  
    }
 Nota: solo con "const" marca error el agragar un valor en la lista 
 
 
 Imprimir de un dato por renglon de la lista 
 
     void main(List<String> args) {
      final calificaciones = [10, 6, 9, 8, 10, 8];   
       print(calificaciones);
      calificaciones.add(2);
      for (var i = 0; i < calificaciones.length; i++) {
             print(calificaciones[i]);
          }
     }
     
     
 Genrar listas 
   
    void main(List<String> args) {
      var numeros = List<int>.generate(10, (i) => i + 1);
      print(numeros);
      var sum = 0;
      numeros.forEach((e) => sum += e);
      print("sum1: $sum");
      sum = 0;
      numeros.forEach((e) {
       sum += e;
     });
     print("sum2: $sum");
     }
     
 --------------------------------------------------------------------------------------
 
 ## condicionales 
 
    void main(List<String> args) {
     int n1 = 5, n2 = 5;
     if (n1 > n2) {
       print("$n1 > $n2");
     } else if (n1 == n2) {
        print("$n1=$n2");
     } else {
       print("$n1<$n2");
      }
    }
    
----------------------------------------------------------------

## Operador tenario

    void main(List<String> args) {
      int n1 = 9, n2 = 4;
      int mayor;
      if (n1 > n2) {
         mayor = n1;
      } else {
         mayor = n2;
        }
        print("el mayor es: $mayor");
        
        int menor;
        n1 < n2 ? menor = n1 : menor = n2;
        print("el menor es: $menor");
        menor = n1 < n2 ? n1 : n2; //declarativo (funcional)
      }
      
------------------------------------------------------------------------

## Sentencia  switch case

    void main(List<String> args) {
     var dia;
     dia = 1;

     switch (dia) {
      case 1:
        print("el dia es ${getDay(dia)}");
        break;
       case "martes":
        print("el dia de hoy es maetes ");
        break;
       default:
         print("dia no conocido");
       }
    }

    String getDay(int num) {
      if (num == 1) {
       return "lunes";
     } else {
       return "";
      }
    }

------------------------------------------------------------------------

## Ciclos

     void main(List<String> args) {
      for (var i = 1; i <= 5; i++) {
        print("$i");
     }

      var numeros = ["1", "2", 3.1416, true, 5];      //forma 1
      for (var e in numeros) {
        print("$e");
      }  
    } 
    
    numeros.forEach((e) {                     //forma 2
    print("$e");
    });
   
ciclo con while

    void main(List<String> args) {
     var num = 1;
     while (num <= 5) {
       stdout.write("$num");
       num++;
     }
       print("");         //ciclo con do while
       num = 1;
       do {
          stdout.write("$num");
          num++;
       } while (num <= 5); 
      }
    
---------------------------------------------------------------------------------------------------------

 ## clases
 
    class User {                 //Creacion de la clase User, las claves van con mayuscula
    String? nombre;              //Propiedad nombre de tipo String. Se declaran igual que una variable,
                                  //se llaman propiedad al ir dentro de la clase
    int? edad;                    //Propiedad de edad
    }

    void main(List<String> args) {
     User usuario1 = User();           //Creacion de instancia usuario1 de la clase User
     print(usuario1);                 //Impresion de la instancia usuario1
     print(usuario1.nombre);          //Impresion de la propoiedad nombre de la instanca usuario1
     print(usuario1.edad);            //Impresion de la propiedad edad de la instancia usuario1
    }

------------------------------------------------------------------------------------------------

    class User {
    String nombre = "Alex";
    int edad = 50;
    }

    void main(List<String> args) {
      User usuario1 = User();
      print(usuario1.nombre);
      print(usuario1.edad);
    }

--------------------------------------------------------------------------------------------- 

    class User {
    String nombre = "Alex";
    int edad = 50;
    }

    void main(List<String> args) {
     User usuario1 = User();
     User usuario2 = User();

      print(usuario1.nombre);
      print(usuario1.edad);
      print(usuario2.nombre);
      print(usuario1.edad);
    }

-----------------------------------------------------------------------------------------------

    class User {
    String? nombre;
    int? edad;
    }

    void main(List<String> args) {
     User usuario1 = User();
     var usuario2 = User();

     usuario1.nombre = "Alex";
     usuario1.edad = 50;
     usuario2.nombre = "Jimena";
     usuario2.edad = 11;

     print(usuario1.nombre);
     print(usuario1.edad);
     print(usuario2.nombre);
     print(usuario2.edad);
    }

----------------------------------------------------------------------------------------------

    class User {
    String? nombre;
    int? edad;

    void reporte() {
     //1
    print("Nombre: $nombre"); //2
    print("Edad: $edad años"); //3
     } 
    }

    void main(List<String> args) {
      User usuario1 = User();
      usuario1.nombre = "Alex";
      usuario1.edad = 50;

     usuario1.reporte(); //4 
    }

notas: Al estar dentro de la clase se convierte en metodo

1-Metodo reporte, es parecido a una duncion.

2-Imprime la propiedad nombre

3-Imprime la propiedad edad

4-Se invoca al metodo de la instancia usuario1

-----------------------------------------------------------------------------------------------

Encapsulamiento
- Capacidad de ocultar los atributos de clase
- Hacerlos locales dentro de la clase
- Las propiedades privadas inician con _

Metodos contructores: Getter y Setter
Setter: Son metodos que establecen/inicializan
los atributos de la clase
Getter: Son metodos que retornan los valores de los
atributos de la clase

------------------------------------------------------------------------------------------

    class User {
      String? _nombre;
      int? _edad;

    void set nombre(String nombre) { //1
       _nombre = nombre; //2
      }

     String get nombre{ //3
        _nombre!; //4
      }

    void reporte() {
      print("Nombre: $_nombre");
      print("Edad: $_edad años");
     }
    }

    void main(List<String> args) {
     final usuario1 = User();
     usuario1.nombre = "Alex"; //5
     print(usuario1.nombre); //6
     usuario1.reporte();
    }

1. Metodo Setter
2. Establece el argumento que recibe la propiedad propiedad
privada. Solo puede recibir un argumento
3. Metodo Getter
4. Retorna la propiedad privada. Solo puede retornar una
propiedad
5. Establece el valor de la propiedad haciendo uso del
setter
6. Obtiene el valor de la propiedad haciendo uso del getter

------------------------------------------------------------------------------------------

    class User {
     String? _nombre;
     int? _edad;

     void set nombre(String nombre) {
      _nombre = nombre;
     }

     String get nombre{
      return _nombre!;
     }

     void set edad(int edad) {
       _edad = edad;
     }

      int get edad{
       return _edad!;
      }

     void reporte() {
      print("Nombre: $_nombre");
      print("Edad: $_edad años");
      }
    }

     void main(List<String> args) {
      final usuario1 = User();
      usuario1.nombre = "Alex";
      usuario1.edad = 50;
      print(usuario1.nombre);
      print(usuario1.edad);
     usuario1.reporte();
    }

-------------------------------------------------------------------------------------

## Usando metodos arrow

    class User {
      String? _nombre;
      int? _edad;

      void set nombre(String nombre) => _nombre = nombre;
      void set edad(int edad) => _edad = edad;

      String get nombre => _nombre!;
      int get edad => _edad!;

      void reporte() {
        print("Nombre: $_nombre");
        print("Edad: $_edad años");
      }
    }

       void main(List<String> args) {
        final usuario1 = User();
        usuario1.nombre = "Alex";
        usuario1.edad = 50;
        print(usuario1.nombre);
       print(usuario1.edad);
       usuario1.reporte(); 
    }    

--------------------------------------------------------------------------------------------------

## Constructores

- Metodo de la clase que se encarga de inicializar los atributos
- Es el primer metodo que se llama al crear la instancia
- El metodo lleva el nombre de la clase

--------------------------------------------------------------------------------------------------

    class User {
      User() {
       //1
      print("Constructor User");
     }
    }

     void main(List<String> args) {
      final usuario1 = User(); //2
      print(usuario1);
    }

1. Creacion del contructor User dentro de la clase User
2. Creacion de la instancia usuario1 que invoca al constructor
User al momento de su creacion

---------------------------------------------------------------------------------------------
## Equivalencia a los setters y getters

     class User {
      String? _nombre; //1
      int? _edad;

     User(String nombre, int edad) {
       //2
      this._nombre = nombre;
      this._edad = edad;
     }

     String? get nombre => _nombre; //3
     int? get edad => _edad;
    }

    void main(List<String> args) {
     final usuario1 = User("Alex", 50); //4
     print(usuario1.nombre);
     print(usuario1.edad);
    }

1. Cracion de las propiedades de la clase User
2. Creacion del contructor User de la clase User
3. Creacion de getters
4. Creacion de la instancia usuario1

---------------------------------------------------------------------------------------------------

## Version corta de constructores {short hand}

     class User {
       String _nombre; //1
       int _edad;

       User(this._nombre, this._edad); //2

       String get nombre => _nombre; //3
       int get edad => _edad;
     }

     void main(List<String> args) {
       final usuario1 = User("Alex", 50); //4
       print(usuario1.nombre);
       print(usuario1.edad);
     }

1. Creacion de las propiedades
2. Creacion del contructor
3. Creacion de los getters
4. Creacion de la instancia User con su contruccion

-------------------------------------------------------------------------------------------------------

## Constructores con propiedades nombradas

    class User {
      String? nombre; //1
      int? edad;

      User({this.nombre, this.edad}); //2

      String? get getNombre => nombre; //3
      int? get getEdad => edad;
    }

    void main(List<String> args) {
      final usuario1 = User(nombre: "Alex", edad: 50); //4
      print(usuario1.nombre);
      print(usuario1.edad);
    }

1. Creacion de las propiedades
2. Creacion del contructor
3. Creacion de los getters
4. Creacion de la instancia User con su contruccion

---------------------------------------------------------------------------------------

## Varios constructores para una clase

    class User {
     String? nombre;
     int? edad;

     User.nombre(this.nombre); //1
     User.edad(this.edad); //2

     String? get getNombre => nombre;
     int? get getEdad => edad;
    }

    void main(List<String> args) {
      final usuario1 = User.nombre("Alex"); //3
      final usuario2 = User.edad(50); //4

      print(usuario1.getNombre);
      print(usuario1.getEdad);

      print(usuario2.getEdad);
      print(usuario2.getNombre);
    }

1. Constructor para la propieda nombre
2. Constructor para la propiedad edad
3. Creacion de la instancia usuario1 con el constructor nombre
4. Creacion de la instancia usuario2 con el constructor edad

-------------------------------------------------------------------------------------------

    class User {
      String? _nombre;
      int? _edad;

      User.nombre(String nombre) {
       _nombre = nombre;
       _edad = 0;
     }

      User.edad(int edad) {
       _nombre = "-";
       _edad = edad;
     }

     String? get getNombre => _nombre;
     int? get getEdad => _edad;
    }

    void main(List<String> args) {
      final usuario1 = User.nombre("Alex");
      final usuario2 = User.edad(50);

      print(usuario1.getNombre);
      print(usuario1.getEdad);

      print(usuario2.getEdad);
      print(usuario2.getNombre);
    }

-------------------------------------------------------------------------------------------
## Herencia y polimorfismo

Herencia
-Mecanismo con el que se puede extender la funcionalidad de una clase
-Por ejemplo usuario puede ser:
   -Estudiante
   -Profesor
   -Directivo
   -Etc.

-------------------------------------------------------------------------------------------

    class Estudiante {
     String nombre = "";
     int edad = 0;

     void mostrarDatos() {
       print("Nombre: $nombre");
       print("Edad: $edad");
     }
    }

    class Profesor {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
       print("Nombre: $nombre");
       print("Edad: $edad");
     }
    }

    class Directivo {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
       print("Nombre: $nombre");
       print("Edad: $edad");
     }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

---------------------------------------------------------------------------------------------------------

    class User {
      String nombre = "";
      int edad = 0;

    void mostrarDatos() {
      print("Nombre: $nombre");
      print("Edad: $edad");
     } 
    }

    class Estudiante extends User {}

    class Profesor extends User{}

    class Directivo extends User{}

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

-------------------------------------------------------------------------------------
## Sobreescritura de metodos (Overriding)

    class User {
     String nombre = "";
     int edad = 0;

     void mostrarDatos() {
      print("Nombre: $nombre");
      print("Edad: $edad");
     }
    }

    class Estudiante extends User {
     @override
     void mostrarDatos() {
       print("Estudiante: $nombre");
       print("Edad: $edad");
     } 
    }

    class Profesor extends User{}

    class Directivo extends User{}

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

---------------------------------------------------------------------------------------------

## Uso del constructor super

    class User {
      String nombre = "";
      int edad = 0;
      User(this.nombre, this.edad);

      void mostrarDatos() {
       print("Nombre: $nombre");
       print("Edad: $edad");
     }
    }

    class Estudiante extends User {
      Estudiante(String nombre, int edad) : super(nombre, edad);
    }

    class Profesor extends User {
      Profesor(String nombre, int edad) : super(nombre, edad);
    }

    class Directivo extends User {
      Directivo(String nombre, int edad) : super(nombre, edad);
    }

    void main(List<String> args) {
    final estudiante1 = Estudiante("Hugo", 15);
    estudiante1.mostrarDatos();

    final profesor1 = Profesor("Paco", 25);
    profesor1.mostrarDatos();

    final directivo1 = Directivo("Luis", 30);
    directivo1.mostrarDatos(); 
    }

---------------------------------------------------------------------------------

## Ejecucion de metodos de la superclase

    class User {
     String nombre = "";
     int edad = 0;
     User(this.nombre, this.edad);

     void mostrarDatos() {
       print("Nombre: $nombre");
       print("Edad $edad");
     }
    }

    class Estudiante extends User {
     Estudiante(String nombre, int edad) : super(nombre, edad);

     @override
     void mostraDatos() {
       print("Estudiante");
       super.mostrarDatos();
      }
    }

    class Profesor extends User {
     Profesor(String nombre, int edad) : super(nombre, edad);

     @override
     void mostraDatos() {
       print("Profesor");
       super.mostrarDatos();
     }
    }

    class Directivo extends User {
     Directivo(String nombre, int edad) : super(nombre, edad);

     @override
     void mostraDatos() {
       print("Directivo");
       super.mostrarDatos();
     }
    }

    void main(List<String> args) {
     final estudiante1 = Estudiante("Hugo", 15);
     estudiante1.mostrarDatos();

     final profesor1 = Profesor("Paco", 25);
     profesor1.mostrarDatos();

     final directivo1 = Directivo("Luis", 30);
     directivo1.mostrarDatos();
    }

---------------------------------------------------------------------------------------------

## Clase Abstractas con metodos

- Permites la creacion de metodos y propiedades generales
sin su implementacion
- No son instanciables

---------------------------------------------------------------------------------------------

    abstract class User {
      String? nombre;
      int? edad;

      void mostarDatos();
     }

    class Estudiante extends User {
      void mostrarDatos() {
        print("Estudiante");
        print("Nombre: $nombre");
        print("Edad: $edad");
     } 
    }

     void main(List<String> args) {
       final estudiante1 = Estudiante();
       estudiante1.nombre = "Alex";
       estudiante1.edad = 50;
       estudiante1.mostarDatos();
     }

---------------------------------------------------------------------------

## Clases abstractas con constructores

    abstract class User {
      String? nombre;
      int? edad;

      User(this.nombre, this.edad);
      void mostrarDatos(); 
    }

    class Estudiante extends User {
     Estudiante(String nombre, int edad) : super(nombre, edad);
     void mostrarDatos() {
       print("Estudiante");
       print("Nombre $nombre");
       print("Edad: $edad");
     } 
    }

    void main(List<String> args) {
     final estudiante1 = Estudiante("Alex", 50);
     estudiante1.mostrarDatos();
    }

-------------------------------------------------------------------------------------

## Interfaces

    class User {
     String? nombre;
     int? edad;

     void mostrarDatos() {}
    }

    class Estudiante implements User {
      String? nombre;
      int? edad;

     void mostrarDatos() {
       print("Estudiante");
       print("Nombre $nombre");
       print("Edad $edad");
     }
    }
 
    void main(List<String> args) {
     final estudiante1 = Estudiante();
     estudiante1.nombre = "Alex";
     estudiante1.edad = 52;
     estudiante1.mostrarDatos();
    }

---------------------------------------------------------------------------------------
## Multi-Interfaces

    class User {
     String? nombre;
     int? edad;

     void mostrarDatos() {} 
    }

    class Estudiante implements User, Materia {
     String? nombre;
     int? edad;
     String? materia;

     void mostrarDatos() {
       print("Estudiante");
       print("Nombre: $nombre");
       print("Edad $edad");
     } 
    }

    class Materia {
     String? materia;
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Alex";
      estudiante1.edad = 50;
      estudiante1.mostrarDatos();
      estudiante1.materia = "Matematicas";
      print("Materia: ${estudiante1.materia}");
    }

---------------------------------------------------------------------------------------//
## Propiedaes de instancia

    void main(List<String> args) {
     final usuario1 = User();
     final usuario2 = User();
     print(usuario1.maxUsers);
     print(usuario2.maxUsers); 
    }

    class User {
     int maxUsers = 10; 
    }

-------------------------------------------------------------------------------

## Propiedades de clase

    void main(List<String> args) {
     print(User.maxUsers);
    }

    class User {
     static int maxUsers = 10;
    }

-------------------------------------------------------------------------------------

## Metodos de clase

    void main(List<String> args) {
     print(User.maxUsers);
     print("Maximo de usuarios: ${User.getMAxUsers()}");
    } 

    class User {
      static int maxUsers = 10;

      static int getMAxUsers() {
      return maxUsers;
      }
     }
 
 
