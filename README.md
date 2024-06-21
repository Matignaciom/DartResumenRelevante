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
    'Maria': 30,
    'Pedro': 20
  };
  edad['Luis'] = 35;
  edad.forEach((key, value) {
    print('Clave: $key, Valor: $value');
  });
}
```

Con esto, tienes una buena base para trabajar con listas y mapas en Dart.

### Declaración de Funciones
En Dart, las funciones se declaran utilizando la palabra clave `void` si no devuelven un valor, o el tipo de valor que devuelven.

#### Función Simple
```dart
void saludar() {
  print('¡Hola, mundo!');
}
```

Para llamar a la función:
```dart
saludar();
```

### Funciones con Argumentos
Las funciones pueden tomar argumentos que se pasan al llamarlas.

#### Argumentos Posicionales
Estos argumentos se pasan en un orden específico.

```dart
void saludar(String nombre) {
  print('¡Hola, $nombre!');
}

saludar('Juan'); // ¡Hola, Juan!
```

#### Argumentos con Valores Predeterminados
Puedes proporcionar valores predeterminados a los argumentos.

```dart
void saludar([String nombre = 'amigo']) {
  print('¡Hola, $nombre!');
}

saludar(); // ¡Hola, amigo!
saludar('María'); // ¡Hola, María!
```

### Tipos de Parámetros

#### Parámetros Nombrados
Los parámetros nombrados se especifican por su nombre al llamar a la función. Son opcionales por defecto, pero puedes hacerlos obligatorios utilizando `required`.

```dart
void saludar({String? nombre, int? edad}) {
  print('¡Hola, $nombre! Tienes $edad años.');
}

saludar(nombre: 'Juan', edad: 25); // ¡Hola, Juan! Tienes 25 años.
```

#### Parámetros Nombrados Requeridos
Para hacer que los parámetros nombrados sean obligatorios, usa `required`.

```dart
void saludar({required String nombre, required int edad}) {
  print('¡Hola, $nombre! Tienes $edad años.');
}

saludar(nombre: 'Juan', edad: 25); // ¡Hola, Juan! Tienes 25 años.
```

### Devolver un Valor
Para devolver un valor desde una función, especifica el tipo de valor de retorno y usa la palabra clave `return`.

#### Función que Devuelve un Valor
```dart
int sumar(int a, int b) {
  return a + b;
}

int resultado = sumar(3, 4); // resultado ahora es 7
print(resultado); // 7
```

### Ejemplo Completo

Aquí tienes un ejemplo que combina diferentes tipos de parámetros y una función que devuelve un valor:

```dart
// Función con parámetros posicionales y valores predeterminados
void saludar([String nombre = 'amigo']) {
  print('¡Hola, $nombre!');
}

// Función con parámetros nombrados y devolución de valor
double calcularArea({required double base, required double altura}) {
  return base * altura / 2;
}

// Función que no devuelve valor
void mostrarArea(double area) {
  print('El área es $area');
}

void main() {
  saludar(); // ¡Hola, amigo!
  saludar('María'); // ¡Hola, María!

  double area = calcularArea(base: 5, altura: 10);
  mostrarArea(area); // El área es 25.0
}
```

Con este conocimiento, puedes trabajar con funciones en Dart, pasando argumentos y devolviendo valores según sea necesario.

### Clases y Atributos
En Dart, una clase es una plantilla para crear objetos. Puedes definir atributos dentro de la clase.

#### Definición de una Clase con Atributos
```dart
class Persona {
  String nombre;
  int edad;

  Persona(this.nombre, this.edad); // Constructor
}
```

### Constructor
El constructor es una función especial que se llama cuando se crea una instancia de la clase. En el ejemplo anterior, el constructor toma dos argumentos, `nombre` y `edad`.

#### Instancia de la Clase
```dart
void main() {
  Persona persona1 = Persona('Juan', 25);
  print(persona1.nombre); // Juan
  print(persona1.edad); // 25
}
```

### Modificadores de Acceso
En Dart, los atributos y métodos son públicos por defecto. Para hacerlos privados, usa el guion bajo `_` antes del nombre del atributo o método.

#### Atributos Privados
```dart
class Persona {
  String _nombre;
  int _edad;

  Persona(this._nombre, this._edad);
}
```

### Getters y Setters
Los getters y setters te permiten controlar el acceso a los atributos de una clase.

#### Definición de Getters y Setters
```dart
class Persona {
  String _nombre;
  int _edad;

  Persona(this._nombre, this._edad);

  String get nombre => _nombre;

  set nombre(String nombre) {
    _nombre = nombre;
  }

  int get edad => _edad;

  set edad(int edad) {
    _edad = edad;
  }
}
```

### Herencia
La herencia permite que una clase derive de otra, heredando sus atributos y métodos.

#### Ejemplo de Herencia
```dart
class Persona {
  String nombre;
  int edad;

  Persona(this.nombre, this.edad);

  void mostrarInfo() {
    print('Nombre: $nombre, Edad: $edad');
  }
}

class Empleado extends Persona {
  double salario;

  Empleado(String nombre, int edad, this.salario) : super(nombre, edad);

  void mostrarSalario() {
    print('Salario: $salario');
  }
}

void main() {
  Empleado empleado1 = Empleado('Maria', 30, 50000);
  empleado1.mostrarInfo(); // Nombre: Maria, Edad: 30
  empleado1.mostrarSalario(); // Salario: 50000.0
}
```

### Clases Abstractas
Una clase abstracta no puede ser instanciada y puede contener métodos abstractos (sin implementación).

#### Definición de una Clase Abstracta
```dart
abstract class Figura {
  void dibujar(); // Método abstracto
}

class Circulo extends Figura {
  @override
  void dibujar() {
    print('Dibujar un círculo');
  }
}

void main() {
  Circulo circulo = Circulo();
  circulo.dibujar(); // Dibujar un círculo
}
```

### Interfaces
En Dart, cualquier clase puede actuar como una interfaz. Simplemente implementa la clase y define los métodos.

#### Definición de una Interfaz
```dart
class Vehiculo {
  void encender() => print('Vehículo encendido');
  void apagar() => print('Vehículo apagado');
}

class Coche implements Vehiculo {
  @override
  void encender() => print('Coche encendido');

  @override
  void apagar() => print('Coche apagado');
}

void main() {
  Coche coche = Coche();
  coche.encender(); // Coche encendido
  coche.apagar(); // Coche apagado
}
```

### Mixins
Un mixin es una forma de reutilizar código en múltiples clases. Usas la palabra clave `with`.

#### Definición de un Mixin
```dart
mixin Volador {
  void volar() => print('Estoy volando');
}

class Animal {
  void caminar() => print('Estoy caminando');
}

class Pájaro extends Animal with Volador {}

void main() {
  Pájaro pajaro = Pájaro();
  pajaro.caminar(); // Estoy caminando
  pajaro.volar(); // Estoy volando
}
```

### Ejemplo Completo
A continuación, se muestra un ejemplo completo que incluye clases, herencia, getters y setters, y mixins:

```dart
// Clase base
class Persona {
  String _nombre;
  int _edad;

  Persona(this._nombre, this._edad);

  // Getter y setter para nombre
  String get nombre => _nombre;

  set nombre(String nombre) {
    _nombre = nombre;
  }

  // Getter y setter para edad
  int get edad => _edad;

  set edad(int edad) {
    _edad = edad;
  }

  void mostrarInfo() {
    print('Nombre: $_nombre, Edad: $_edad');
  }
}

// Mixin
mixin Trabajador {
  void trabajar() => print('Estoy trabajando');
}

// Clase derivada con mixin
class Empleado extends Persona with Trabajador {
  double salario;

  Empleado(String nombre, int edad, this.salario) : super(nombre, edad);

  void mostrarSalario() {
    print('Salario: $salario');
  }
}

void main() {
  Empleado empleado1 = Empleado('Juan', 25, 50000);
  empleado1.mostrarInfo(); // Nombre: Juan, Edad: 25
  empleado1.trabajar(); // Estoy trabajando
  empleado1.mostrarSalario(); // Salario: 50000.0
}
```

Con esto, tienes una comprensión básica y completa de cómo trabajar con clases, atributos, constructores, instancias, modificadores de acceso, getters y setters, herencia, clases abstractas, interfaces y mixins en Dart.

### Future
Un `Future` representa un valor o error que estará disponible en algún momento en el futuro. Los `Future` son comunes en Dart para operaciones asíncronas.

#### Ejemplo de Future
```dart
Future<String> obtenerNombre() async {
  return 'Juan';
}
```

### then, catchError y whenComplete
Puedes manejar los resultados y errores de un `Future` utilizando los métodos `then`, `catchError` y `whenComplete`.

#### then
`then` se usa para manejar el resultado exitoso de un `Future`.

```dart
void main() {
  obtenerNombre().then((nombre) {
    print(nombre); // Juan
  });
}

Future<String> obtenerNombre() async {
  return 'Juan';
}
```

#### catchError
`catchError` se usa para manejar errores que ocurren durante la ejecución de un `Future`.

```dart
void main() {
  obtenerNombre().then((nombre) {
    print(nombre);
  }).catchError((error) {
    print('Ocurrió un error: $error');
  });
}

Future<String> obtenerNombre() async {
  throw 'No se pudo obtener el nombre';
}
```

#### whenComplete
`whenComplete` se usa para ejecutar algún código cuando el `Future` completa, independientemente de si fue exitoso o fallido.

```dart
void main() {
  obtenerNombre().then((nombre) {
    print(nombre);
  }).catchError((error) {
    print('Ocurrió un error: $error');
  }).whenComplete(() {
    print('Operación completada');
  });
}

Future<String> obtenerNombre() async {
  throw 'No se pudo obtener el nombre';
}
```

### async y await
El uso de `async` y `await` hace que el código asíncrono se vea y se comporte más como código síncrono.

#### await
`await` se usa para esperar el resultado de un `Future`.

```dart
void main() async {
  try {
    String nombre = await obtenerNombre();
    print(nombre);
  } catch (error) {
    print('Ocurrió un error: $error');
  }
}

Future<String> obtenerNombre() async {
  return 'Juan';
}
```

#### Manejo de Errores con async y await
Puedes manejar errores en una función `async` usando `try-catch`.

```dart
void main() async {
  try {
    String nombre = await obtenerNombre();
    print(nombre);
  } catch (error) {
    print('Ocurrió un error: $error');
  } finally {
    print('Operación completada');
  }
}

Future<String> obtenerNombre() async {
  throw 'No se pudo obtener el nombre';
}
```

### Ejemplo Completo
Aquí tienes un ejemplo completo que muestra cómo usar `Future`, `then`, `catchError`, `whenComplete`, `async`, `await`, y el manejo de errores:

```dart
void main() async {
  // Usando then, catchError y whenComplete
  obtenerNombre()
      .then((nombre) {
        print('Nombre: $nombre');
      })
      .catchError((error) {
        print('Ocurrió un error: $error');
      })
      .whenComplete(() {
        print('Operación completada con then');
      });

  // Usando async y await
  try {
    String nombre = await obtenerNombre();
    print('Nombre: $nombre');
  } catch (error) {
    print('Ocurrió un error: $error');
  } finally {
    print('Operación completada con async/await');
  }
}

Future<String> obtenerNombre() async {
  await Future.delayed(Duration(seconds: 2)); // Simulando una operación asíncrona
  return 'Juan';
}
```

### Resumen
- **Future**: Representa un valor que estará disponible en el futuro.
- **then**: Maneja el resultado exitoso de un `Future`.
- **catchError**: Maneja errores de un `Future`.
- **whenComplete**: Ejecuta código cuando el `Future` completa, independientemente del resultado.
- **async y await**: Permiten escribir código asíncrono de manera más legible y manejan resultados y errores de `Future`.

Con estos conceptos, puedes manejar la programación asíncrona en Dart de manera efectiva.
