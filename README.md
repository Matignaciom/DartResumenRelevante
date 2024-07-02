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
