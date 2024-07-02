### Introducción

¡Hola! Soy Matías Ignacio y te doy la bienvenida a este repositorio de aprendizaje gratuito sobre programación en Dart. Aquí encontrarás una guía completa y detallada para entender los conceptos fundamentales de este lenguaje, desde los operadores básicos hasta estructuras más avanzadas como listas, mapas, funciones, clases y más. Mi objetivo es proporcionar recursos accesibles y fáciles de entender para todos aquellos que deseen aprender Dart, ya sea que estés comenzando tu viaje en la programación o busques mejorar tus habilidades. ¡Espero que disfrutes y encuentres útil este material!

### Operadores de Asignación
Los operadores de asignación se utilizan para asignar valores a las variables. Los más comunes son:

- `=`: Asignación simple.
  ```dart
  int a = 5;
  ```

- `+=`: Asignación con suma.
  ```dart
  int a = 5;
  a += 3; // a ahora es 8
  ```

- `-=`: Asignación con resta.
  ```dart
  int a = 5;
  a -= 3; // a ahora es 2
  ```

- `*=`: Asignación con multiplicación.
  ```dart
  int a = 5;
  a *= 3; // a ahora es 15
  ```

- `/=`: Asignación con división.
  ```dart
  double a = 5.0;
  a /= 2; // a ahora es 2.5
  ```

- `~/=`: Asignación con división entera.
  ```dart
  int a = 5;
  a ~/= 2; // a ahora es 2
  ```

- `%=`: Asignación con módulo.
  ```dart
  int a = 5;
  a %= 2; // a ahora es 1
  ```

### Operadores Unarios
Los operadores unarios se aplican a un solo operando y realizan diversas operaciones:

- `++`: Incremento.
  ```dart
  int a = 5;
  a++; // a ahora es 6
  ```

- `--`: Decremento.
  ```dart
  int a = 5;
  a--; // a ahora es 4
  ```

- `-`: Negación.
  ```dart
  int a = 5;
  int b = -a; // b ahora es -5
  ```

- `!`: Negación lógica.
  ```dart
  bool a = true;
  bool b = !a; // b ahora es false
  ```

- `~`: Complemento de bits.
  ```dart
  int a = 5;
  int b = ~a; // b ahora es -6
  ```

### Operadores Condicionales
Los operadores condicionales se utilizan para tomar decisiones basadas en condiciones:

- `?:`: Operador ternario.
  ```dart
  int a = 5;
  int b = (a > 3) ? 10 : 20; // b ahora es 10 porque a es mayor que 3
  ```

- `??`: Operador de fusión nula.
  ```dart
  String? a;
  String b = a ?? 'Valor por defecto'; // b ahora es 'Valor por defecto' porque a es null
  ```

- `??=`: Asignación condicional.
  ```dart
  String? a;
  a ??= 'Valor asignado'; // a ahora es 'Valor asignado' porque era null
  ```

Estos son los operadores básicos en Dart. Cada uno tiene su propia utilidad y se emplea en diferentes escenarios para manejar variables y expresiones.

### Listas en Dart
Una lista es una colección ordenada de objetos, que puede contener duplicados.

#### Crear una Lista
```dart
List<int> numeros = [1, 2, 3, 4, 5];
List<String> frutas = ['manzana', 'banana', 'naranja'];
```

#### Recorrer una Lista
Puedes usar varios métodos para recorrer una lista:

- **For Loop:**
  ```dart
  List<int> numeros = [1, 2, 3, 4, 5];
  for (int i = 0; i < numeros.length; i++) {
    print(numeros[i]);
  }
  ```

- **For-in Loop:**
  ```dart
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  for (String fruta in frutas) {
    print(fruta);
  }
  ```

- **forEach:**
  ```dart
  List<int> numeros = [1, 2, 3, 4, 5];
  numeros.forEach((numero) {
    print(numero);
  });
  ```

#### Métodos Útiles de una Lista
Dart proporciona varios métodos útiles para trabajar con listas:

- **add**: Añadir un solo elemento.
  ```dart
  List<int> numeros = [1, 2, 3];
  numeros.add(4); // [1, 2, 3, 4]
  ```

- **addAll**: Añadir múltiples elementos.
  ```dart
  List<int> numeros = [1, 2, 3];
  numeros.addAll([4, 5, 6]); // [1, 2, 3, 4, 5, 6]
  ```

- **remove**: Eliminar un elemento.
  ```dart
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  frutas.remove('banana'); // ['manzana', 'naranja']
  ```

- **removeAt**: Eliminar un elemento en un índice específico.
  ```dart
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  frutas.removeAt(1); // ['manzana', 'naranja']
  ```

- **indexOf**: Encontrar el índice de un elemento.
  ```dart
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  int index = frutas.indexOf('banana'); // 1
  ```

- **contains**: Verificar si un elemento está en la lista.
  ```dart
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  bool existe = frutas.contains('banana'); // true
  ```

### Map en Dart
Un mapa es una colección de pares clave-valor. Cada clave única está asociada a un valor.

#### Crear un Map
```dart
Map<String, int> edad = {
  'Juan': 25,
  'Maria': 30,
  'Pedro': 20
};
```

#### Recorrer un Map
Puedes recorrer un mapa de varias maneras:

- **forEach:**
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30,
    'Pedro': 20
  };
  edad.forEach((key, value) {
    print('Clave: $key, Valor: $value');
  });
  ```

- **for-in Loop con keys:**
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30,
    'Pedro': 20
  };
  for (String key in edad.keys) {
    print('Clave: $key, Valor: ${edad[key]}');
  }
  ```

- **for-in Loop con entries:**
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30,
    'Pedro': 20
  };
  for (var entry in edad.entries) {
    print('Clave: ${entry.key}, Valor: ${entry.value}');
  }
  ```

#### Métodos Útiles de un Map
Dart proporciona varios métodos útiles para trabajar con mapas:

- **addAll**: Añadir múltiples pares clave-valor.
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
  };
  edad.addAll({
    'Maria': 30,
    'Pedro': 20
  }); // {'Juan': 25, 'Maria': 30, 'Pedro': 20}
  ```

- **remove**: Eliminar un par clave-valor por clave.
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30
  };
  edad.remove('Maria'); // {'Juan': 25}
  ```

- **containsKey**: Verificar si una clave está en el mapa.
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30
  };
  bool existe = edad.containsKey('Maria'); // true
  ```

- **containsValue**: Verificar si un valor está en el mapa.
  ```dart
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30
  };
  bool existe = edad.containsValue(30); // true
  ```

### Ejemplo Completo

Aquí tienes un ejemplo completo que utiliza listas y mapas:

```dart
void main() {
  // Listas
  List<String> frutas = ['manzana', 'banana', 'naranja'];
  frutas.add('pera');
  frutas.forEach((fruta) {
    print(fruta);
  });

  // Mapas
  Map<String, int> edad = {
    'Juan': 25,
    'Maria': 30

,
    'Pedro': 20
  };
  edad['Ana'] = 22;
  edad.forEach((key, value) {
    print('Clave: $key, Valor: $value');
  });
}
```

### Funciones en Dart

Las funciones en Dart son bloques de código reutilizables que realizan una tarea específica. Se pueden definir utilizando la palabra clave `void` si no retornan un valor, o especificando el tipo de valor que retornan.

#### Definir una Función
```dart
void saludar() {
  print('Hola!');
}

int sumar(int a, int b) {
  return a + b;
}
```

#### Llamar a una Función
```dart
void main() {
  saludar(); // Llama a la función saludar
  int resultado = sumar(3, 4); // Llama a la función sumar
  print(resultado); // Imprime 7
}
```

#### Funciones Flecha
Las funciones flecha son una forma corta de definir funciones que contienen una sola expresión.

```dart
int multiplicar(int a, int b) => a * b;

void main() {
  int resultado = multiplicar(3, 4); // Llama a la función multiplicar
  print(resultado); // Imprime 12
}
```

### Clases en Dart

Las clases son una forma de encapsular datos y comportamientos relacionados. Puedes crear instancias de una clase para trabajar con sus datos y métodos.

#### Definir una Clase
```dart
class Persona {
  String nombre;
  int edad;

  Persona(this.nombre, this.edad);

  void saludar() {
    print('Hola, me llamo $nombre y tengo $edad años.');
  }
}
```

#### Crear una Instancia de una Clase
```dart
void main() {
  Persona persona = Persona('Juan', 25);
  persona.saludar(); // Llama al método saludar
}
```

#### Herencia
La herencia permite que una clase herede propiedades y métodos de otra clase.

```dart
class Empleado extends Persona {
  String puesto;

  Empleado(String nombre, int edad, this.puesto) : super(nombre, edad);

  @override
  void saludar() {
    super.saludar();
    print('Soy un $puesto.');
  }
}

void main() {
  Empleado empleado = Empleado('Maria', 30, 'Ingeniera');
  empleado.saludar(); // Llama al método saludar
}
```

### Interfaces
En Dart, las interfaces se implementan utilizando la palabra clave `implements`. Al implementar una interfaz, una clase debe proporcionar implementaciones para todos los métodos de la interfaz.

#### Ejemplo de Interface
```dart
abstract class Vehiculo {
  void encender();
  void apagar();
}

class Coche implements Vehiculo {
  @override
  void encender() {
    print('El coche está encendido');
  }

  @override
  void apagar() {
    print('El coche está apagado');
  }
}

void main() {
  Coche miCoche = Coche();
  miCoche.encender(); // El coche está encendido
  miCoche.apagar(); // El coche está apagado
}
```

### Mixins
Los mixins permiten compartir métodos entre múltiples clases sin usar herencia. Los mixins se definen utilizando la palabra clave `mixin`.

#### Ejemplo de Mixin
```dart
mixin Volador {
  void volar() {
    print('Estoy volando');
  }
}

class Ave with Volador {}

void main() {
  Ave miAve = Ave();
  miAve.volar(); // Estoy volando
}
```

### Manejo de Excepciones
El manejo de excepciones en Dart se realiza utilizando bloques `try`, `catch` y `finally`.

#### Ejemplo de Manejo de Excepciones
```dart
void main() {
  try {
    int resultado = 10 ~/ 0;
    print(resultado);
  } catch (e) {
    print('Error: $e');
  } finally {
    print('Esto siempre se ejecuta');
  }
}
```

### Futures y Async/Await
Dart es un lenguaje asincrónico que permite realizar operaciones no bloqueantes utilizando `Future`, `async` y `await`.

#### Ejemplo de Future
```dart
Future<String> fetchUserOrder() {
  // Simula una demora en la red
  return Future.delayed(Duration(seconds: 2), () => 'Café con leche');
}

void main() {
  fetchUserOrder().then((order) {
    print('Orden recibida: $order');
  });
  print('Esperando la orden...');
}
```

#### Ejemplo de Async/Await
```dart
Future<String> fetchUserOrder() async {
  // Simula una demora en la red
  return await Future.delayed(Duration(seconds: 2), () => 'Café con leche');
}

void main() async {
  print('Esperando la orden...');
  String order = await fetchUserOrder();
  print('Orden recibida: $order');
}
```

### Streams
Los streams proporcionan una secuencia de datos asincrónicos. Puedes usar streams para manejar eventos que ocurren en el tiempo.

#### Ejemplo de Stream
```dart
Stream<int> contador(int max) async* {
  for (int i = 0; i <= max; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}

void main() {
  Stream<int> stream = contador(5);
  stream.listen((data) {
    print('Contador: $data');
  });
}
```

### Programación Orientada a Objetos (POO)
Dart es un lenguaje orientado a objetos y soporta características como encapsulación, herencia y polimorfismo.

#### Ejemplo Completo de POO
```dart
class Animal {
  void sonido() {
    print('El animal hace un sonido');
  }
}

class Perro extends Animal {
  @override
  void sonido() {
    print('El perro ladra');
  }
}

class Gato extends Animal {
  @override
  void sonido() {
    print('El gato maúlla');
  }
}

void main() {
  Animal miAnimal = Animal();
  miAnimal.sonido(); // El animal hace un sonido

  Perro miPerro = Perro();
  miPerro.sonido(); // El perro ladra

  Gato miGato = Gato();
  miGato.sonido(); // El gato maúlla
}
```

### Conclusión
Con esta guía, ahora tienes una comprensión sólida de los conceptos fundamentales de Dart, incluyendo operadores, listas, mapas, funciones, clases, herencia, interfaces, mixins, manejo de excepciones, programación asincrónica y más. ¡Espero que este material te haya sido útil y te animo a seguir practicando y explorando más sobre Dart y Flutter!

---

### Guía Avanzada de Dart para Flutter

---

## Instalación y Configuración

### Cómo instalar Dart

#### Windows
1. Descarga el SDK de Dart desde [dart.dev](https://dart.dev/get-dart).
2. Extrae el archivo en una ubicación de tu elección.
3. Agrega la ruta del SDK de Dart a tu variable de entorno `PATH`.

#### macOS
1. Usa Homebrew para instalar Dart:
   ```sh
   brew tap dart-lang/dart
   brew install dart
   ```

#### Linux
1. Añade el repositorio de Dart:
   ```sh
   sudo apt update
   sudo apt install apt-transport-https
   sudo sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
   sudo sh -c 'wget -qO- https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
   ```
2. Instala Dart:
   ```sh
   sudo apt update
   sudo apt install dart
   ```

### Configuración del Entorno de Desarrollo
#### Visual Studio Code
1. Instala el [Dart SDK](https://dart.dev/get-dart).
2. Instala la extensión de Dart desde el Marketplace de VS Code.

#### IntelliJ IDEA
1. Instala el [Dart SDK](https://dart.dev/get-dart).
2. Instala el plugin de Dart desde el repositorio de plugins de IntelliJ.

## Tipos de Datos

### Tipos Numéricos
```dart
int entero = 42;
double decimal = 3.14;
```

### Cadenas de Caracteres
```dart
String simple = 'Hola';
String interpolada = 'El valor es ${entero + decimal}';
String multilinea = '''
Línea 1
Línea 2
''';
```

### Listas, Conjuntos y Mapas
#### Listas
```dart
List<int> numeros = [1, 2, 3];
```

#### Conjuntos
```dart
Set<String> nombres = {'Alice', 'Bob'};
```

#### Mapas
```dart
Map<String, int> telefonos = {
  'Alice': 1234,
  'Bob': 5678
};
```

### Nulos y Nullable Types
```dart
String? nombre;
nombre = 'Alice'; // Correcto
nombre = null; // También correcto
```

## Control de Flujo

### Condicionales
```dart
if (entero > 0) {
  print('El número es positivo.');
} else if (entero < 0) {
  print('El número es negativo.');
} else {
  print('El número es cero.');
}
```

### Operadores Ternarios
```dart
String resultado = entero > 0 ? 'Positivo' : 'No positivo';
```

### Bucles
```dart
for (int i = 0; i < 5; i++) {
  print('i: $i');
}

while (entero > 0) {
  entero--;
}

do {
  entero++;
} while (entero < 5);
```

## Funciones Avanzadas

### Funciones Anónimas y Lambdas
```dart
var sumar = (int a, int b) => a + b;
print(sumar(2, 3)); // 5
```

### Closures
```dart
Function makeAdder(int addBy) {
  return (int i) => addBy + i;
}

var add2 = makeAdder(2);
print(add2(3)); // 5
```

### Parámetros Nombrados y Opcionales
```dart
void saludar(String nombre, {String? mensaje}) {
  print('Hola $nombre, ${mensaje ?? 'bienvenido'}');
}
saludar('Alice', mensaje: '¿cómo estás?');
```

## Programación Orientada a Objetos Avanzada

### Constructores
```dart
class Persona {
  String nombre;
  int edad;

  Persona(this.nombre, this.edad);
  Persona.named(this.nombre, this.edad);

  // Constructor constante
  const Persona.constant(this.nombre, this.edad);

  // Constructor fábrica
  factory Persona.fromJson(Map<String, dynamic> json) {
    return Persona(json['nombre'], json['edad']);
  }
}
```

### Sobrecarga de Operadores
```dart
class Vector {
  final int x, y;

  Vector(this.x, this.y);

  Vector operator +(Vector v) => Vector(x + v.x, y + v.y);
}

void main() {
  final v1 = Vector(2, 3);
  final v2 = Vector(4, 5);
  final v3 = v1 + v2;
  print('(${v3.x}, ${v3.y})'); // (6, 8)
}
```

### Enumeraciones (Enums)
```dart
enum Estado { INICIADO, EN_PROGRESO, TERMINADO }

void main() {
  Estado estado = Estado.EN_PROGRESO;

  switch (estado) {
    case Estado.INICIADO:
      print('Iniciado');
      break;
    case Estado.EN_PROGRESO:
      print('En progreso');
      break;
    case Estado.TERMINADO:
      print('Terminado');
      break;
  }
}
```

## Asincronía Avanzada

### Future y Completer
```dart
Future<int> obtenerValor() async {
  return 42;
}

Completer<int> completer = Completer<int>();

void main() {
  completer.complete(42);
  completer.future.then((value) => print(value));
}
```

### Streams Avanzados
```dart
Stream<int> contar(int max) async* {
  for (int i = 0; i <= max; i++) {
    yield i;
  }
}

void main() {
  contar(5).listen((numero) {
    print(numero);
  });
}
```

## Gestión de Paquetes

### pub.dev
Para encontrar y usar paquetes en Dart, visita [pub.dev](https://pub.dev).

### Archivo `pubspec.yaml`
```yaml
name: mi_paquete
version: 1.0.0
description: Descripción de mi paquete

environment:
  sdk: '>=2.12.0 <3.0.0'

dependencies:
  http: ^0.13.3
```

### Crear y Publicar Paquetes
1. Crea el archivo `pubspec.yaml` con la configuración adecuada.
2. Añade tu código en el directorio `lib`.
3. Publica tu paquete usando:
   ```sh
   dart pub publish
   ```

## Testing

### Pruebas Unitarias
```dart
import 'package:test/test.dart';

void main() {
  test('sumar dos números', () {
    expect(2 + 3, 5);
  });
}
```

### Mocks y Stubs
```dart
import 'package:mockito/mockito.dart';

class Servicio {
  String obtenerDato() => 'dato';
}

class MockServicio extends Mock implements Servicio {}

void main() {
  var servicio = MockServicio();
  when(servicio.obtenerDato()).thenReturn('dato falso');

  print(servicio.obtenerDato()); // 'dato falso'
}
```

### Integración Continua
Configura CI con GitHub Actions:
```yaml
name: Dart CI

on: [push, pull_request]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    -

 name: Install Dart
      uses: dart-lang/setup-dart@v1
    - name: Install dependencies
      run: dart pub get
    - name: Run tests
      run: dart test
```

## Interoperabilidad y Plugins

### Crear Plugins en Flutter
1. Crea un nuevo plugin:
   ```sh
   flutter create --template=plugin nombre_del_plugin
   ```
2. Añade el código de la plataforma nativa en los directorios `android` y `ios`.
3. Usa el plugin en tu proyecto Flutter añadiéndolo a `pubspec.yaml`.

### Integración con APIs de Plataforma
Para invocar código nativo desde Flutter, usa los canales de plataforma (Platform Channels).

### Integración con Flutter Web y Desktop
1. Agrega soporte web o desktop:
   ```sh
   flutter create .
   flutter build web
   flutter build windows
   ```

### Ejemplos de Casos de Uso del Mundo Real

#### Integración con APIs REST
```dart
import 'package:http/http.dart' as http;
import 'dart:convert';

Future<void> fetchPost() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/posts/1'));

  if (response.statusCode == 200) {
    var data = jsonDecode(response.body);
    print(data);
  } else {
    throw Exception('Failed to load post');
  }
}
```

#### Autenticación con Firebase Auth
```dart
import 'package:firebase_auth/firebase_auth.dart';

Future<User?> signInWithEmail(String email, String password) async {
  try {
    UserCredential userCredential = await FirebaseAuth.instance.signInWithEmailAndPassword(email: email, password: password);
    return userCredential.user;
  } catch (e) {
    print(e);
    return null;
  }
}
```

## Pruebas y Mejora del Rendimiento

### Técnicas de Optimización
- Usa el widget `RepaintBoundary` para evitar redibujar innecesariamente.
- Implementa Lazy Loading en listas largas.
- Minimiza el uso de operaciones costosas en `build()`.

### Herramientas de Profiling
- Flutter DevTools: Herramienta poderosa para debugging y profiling.
- Dart Observatory: Permite inspeccionar el rendimiento de aplicaciones Dart.

## Conclusión

Esta guía avanzada de Dart para Flutter abarca una amplia gama de temas que van desde la instalación y configuración básica hasta técnicas avanzadas de programación, gestión de estado, pruebas y optimización. Esperamos que esta guía te ayude a profundizar tus conocimientos y habilidades en Dart y Flutter, permitiéndote construir aplicaciones móviles robustas y de alto rendimiento.
