function ejercicio1() {
    // Algoritmo que transforma de grados Celsius a Fahrenheit
    console.clear();
    
    // Solicitar al usuario la temperatura en grados Celsius
    // parseFloat se usa para convertir la entrada del usuario (un string) a un número de punto flotante
    let celsius = parseFloat(prompt("Ingrese la temperatura en grados Celsius:"));
    
    // Convertir la temperatura de Celsius a Fahrenheit usando la fórmula: F = (C * 9/5) + 32
    let fahrenheit = (celsius * 9/5) + 32;
    
    // Mostrar la temperatura ingresada en Celsius
    console.log(`Temperatura ingresada: ${celsius}°C`);
    
    // Mostrar la temperatura convertida en Fahrenheit
    console.log(`La temperatura en grados Fahrenheit es: ${fahrenheit}°F`);
}

function ejercicio2() {
    // Algoritmo que lee un número entero, obtiene y presenta el doble y el triple del número
    console.clear();
    
    // Solicitar al usuario un número entero
    // parseInt se usa para convertir la entrada del usuario (un string) a un número entero
    let numero = parseInt(prompt("Ingrese un número entero:"));
    
    // Calcular el doble del número ingresado
    let doble = numero * 2;
    
    // Calcular el triple del número ingresado
    let triple = numero * 3;
    
    // Mostrar el número ingresado
    console.log(`Número ingresado: ${numero}`);
    
    // Mostrar el doble del número ingresado
    console.log(`El doble del número es: ${doble}`);
    
    // Mostrar el triple del número ingresado
    console.log(`El triple del número es: ${triple}`);
}

function ejercicio3() {
    // Algoritmo que lee 4 variables y calcula e imprime su producto, su suma y su media aritmética
    console.clear();
    
    // Solicitar al usuario cuatro números, uno por uno, y convertirlos a números de punto flotante
    let vari1 = parseFloat(prompt("Ingrese la primera variable:"));
    let vari2 = parseFloat(prompt("Ingrese la segunda variable:"));
    let vari3 = parseFloat(prompt("Ingrese la tercera variable:"));
    let vari4 = parseFloat(prompt("Ingrese la cuarta variable:"));
    
    // Calcular el producto de las cuatro variables
    let producto = vari1 * vari2 * vari3 * vari4;
    
    // Calcular la suma de las cuatro variables
    let suma = vari1 + vari2 + vari3 + vari4;
    
    // Calcular la media aritmética de las cuatro variables
    let mediaAritmetica = suma / 4;
    
    // Mostrar las variables ingresadas
    console.log(`Variables ingresadas: ${vari1}, ${vari2}, ${vari3}, ${vari4}`);
    
    // Mostrar el producto de las variables
    console.log(`El producto de las variables es: ${producto}`);
    
    // Mostrar la suma de las variables
    console.log(`La suma de las variables es: ${suma}`);
    
    // Mostrar la media aritmética de las variables
    console.log(`La media aritmética de las variables es: ${mediaAritmetica}`);
}

function ejercicio4() {
    // Algoritmo que lee el peso de un hombre en libras y devuelve su peso en kilogramos y gramos
    console.clear();
    
    // Solicitar al usuario el peso en libras y convertirlo a número de punto flotante
    let pesoLibras = parseFloat(prompt("Ingrese el peso en libras:"));
    
    // Convertir el peso de libras a kilogramos usando la conversión: 1 libra = 0.453593 kilogramos
    let pesoKilogramos = pesoLibras * 0.453593;
    
    // Obtener los gramos de la parte decimal de los kilogramos
    let pesoGramos = (pesoKilogramos - Math.floor(pesoKilogramos)) * 1000; 
    
    // Mostrar el peso ingresado en libras
    console.log(`Peso ingresado en libras: ${pesoLibras} lb`);
    
    // Mostrar el peso convertido en kilogramos y gramos
    console.log(`El peso en kilogramos y gramos es: ${Math.floor(pesoKilogramos)} kg ${pesoGramos.toFixed(2)} g`);
}

function ejercicio5() {
    // Algoritmo que resuelve la expresión matemática dada
    console.clear();
    console.log("Expresión: x=((sen(a)+cos(b))*(trunc(a) mod 2))+(raiz(a^3)/(a*b+c))");
    
    // Solicitar al usuario los valores de 'a', 'b', y 'c', y convertirlos a números de punto flotante
    let a = parseFloat(prompt("Ingrese el valor de 'a':"));
    let b = parseFloat(prompt("Ingrese el valor de 'b':"));
    let c = parseFloat(prompt("Ingrese el valor de 'c':"));
    
    // Calcular la expresión matemática paso a paso
    let parte1 = Math.sin(a) + Math.cos(b); // Calcular (sen(a) + cos(b))
    let parte2 = Math.trunc(a) % 2; // Calcular (trunc(a) mod 2)
    let parte3 = Math.sqrt(Math.pow(a, 3)); // Calcular raiz(a^3)
    let parte4 = a * b + c; // Calcular (a*b + c)
    let x = (parte1 * parte2) + (parte3 / parte4); // Calcular la expresión completa
    
    // Mostrar los valores ingresados
    console.log(`Valores ingresados: a=${a}, b=${b}, c=${c}`);
    
    // Mostrar el resultado de la expresión matemática
    console.log(`El resultado de la expresión matemática es: ${x}`);
}

function ejercicio6() {
    // Algoritmo que calcula el sueldo, sobretiempo, ingreso total, seguro social y neto a recibir de un empleado
    console.clear();
    
    // Definir constantes
    const horasNormales = 40;
    const valorHoraNormal = 5;
    const valorHoraSobretiempo = valorHoraNormal * 2;
    const porcentajeSeguroSocial = 0.1;
    
    // Solicitar al usuario las horas trabajadas en la semana y convertirlas a número entero
    let horasTrabajadas = parseInt(prompt("Ingrese las horas trabajadas en la semana:"));
    
    // Inicializar variables para el sueldo, sobretiempo y seguro social
    let sueldo = 0;
    let sobretiempo = 0;
    let seguroSocial = 0;
    
    // Calcular el sueldo y sobretiempo dependiendo de las horas trabajadas
    if (horasTrabajadas <= horasNormales) {
        sueldo = horasTrabajadas * valorHoraNormal; // Calcular sueldo normal
    } else {
        sueldo = horasNormales * valorHoraNormal; // Calcular sueldo normal
        sobretiempo = (horasTrabajadas - horasNormales) * valorHoraSobretiempo; // Calcular sobretiempo
    }
    
    // Calcular el ingreso total sumando el sueldo y el sobretiempo
    let ingresoTotal = sueldo + sobretiempo;
    
    // Calcular el seguro social (10% del ingreso total)
    seguroSocial = ingresoTotal * porcentajeSeguroSocial;
    
    // Calcular el neto a recibir restando el seguro social del ingreso total
    let netoRecibir = ingresoTotal - seguroSocial;
    
    // Mostrar las horas trabajadas
    console.log(`Horas trabajadas: ${horasTrabajadas}`);
    
    // Mostrar el sueldo
    console.log(`El sueldo del empleado es: ${sueldo}`);
    
    // Mostrar el sobretiempo
    console.log(`El sobretiempo del empleado es: ${sobretetime}`);
    
    // Mostrar el ingreso total
    console.log(`El ingreso total del empleado es: ${ingresoTotal}`);
    
    // Mostrar el seguro social
    console.log(`El seguro social del empleado es: ${seguroSocial}`);
    
    // Mostrar el neto a recibir
    console.log(`El neto a recibir del empleado es: ${netoRecibir}`);
}

function ejercicio7() {
    // Algoritmo que pide dos números y presenta el mayor de los dos si el primero es par y el segundo impar
    console.clear();
    
    // Solicitar al usuario el primer número y convertirlo a número entero
    let num1 = parseInt(prompt("Ingrese el primer número:"));
    
    // Solicitar al usuario el segundo número y convertirlo a número entero
    let num2 = parseInt(prompt("Ingrese el segundo número:"));
    
    // Mostrar los números ingresados
    console.log(`Números ingresados: ${num1} y ${num2}`);
    
    // Verificar si el primer número es par y el segundo es impar
    if (num1 % 2 === 0 && num2 % 2 !== 0) {
        // Si es así, mostrar el número mayor de los dos
        console.log(`El número mayor es: ${Math.max(num1, num2)}`);
    } else {
        // Si no cumplen las condiciones, mostrar un mensaje indicando esto
        console.log("Los números no cumplen con las condiciones requeridas.");
    }
}

function ejercicio8() {
    // Algoritmo que lee un carácter y determina si está entre las letras a y z o es un signo de puntuación
    console.clear();
    
    // Solicitar al usuario un carácter
    let caracter = prompt("Ingrese un carácter:");
    
    // Mostrar el carácter ingresado
    console.log(`Carácter ingresado: ${caracter}`);
    
    // Verificar si el carácter es una letra (entre 'a' y 'z' o entre 'A' y 'Z')
    if ((caracter >= 'a' && caracter <= 'z') || (caracter >= 'A' && caracter <= 'Z')) {
        console.log("El carácter ingresado es una letra.");
    } 
    // Verificar si el carácter es un signo de puntuación
    else if (caracter === "," || caracter === "." || caracter === ";" || caracter === ":") {
        console.log("El carácter ingresado es un signo de puntuación.");
    } 
    // Si no es ni letra ni signo de puntuación, mostrar que es otro tipo de carácter
    else {
        console.log("El carácter ingresado no es una letra ni un signo de puntuación.");
    }
}

function ejercicio9() {
    // Algoritmo que determina el costo total por cierta cantidad de colas
    console.clear();
    
    // Solicitar al usuario la cantidad de colas y convertirla a número entero
    let cantidadColas = parseInt(prompt("Ingrese la cantidad de colas:"));
    
    // Definir el costo unitario, aplicando descuento si la cantidad es 12 o más
    let costoUnitario = cantidadColas < 12 ? 0.25 : 0.25 * 0.9; // Descuento del 10% si son 12 o más colas
    
    // Calcular el costo total multiplicando la cantidad de colas por el costo unitario
    let costoTotal = cantidadColas * costoUnitario;
    
    // Mostrar la cantidad de colas ingresadas
    console.log(`Cantidad de colas ingresadas: ${cantidadColas}`);
    
    // Mostrar el costo total
    console.log(`El costo total por ${cantidadColas} colas es: ${costoTotal}`);
}

function ejercicio10() {
    // Algoritmo que aplica descuentos a trajes dependiendo de su precio y calcula el pago con IVA
    console.clear();
    
    // Solicitar al usuario el precio del traje y convertirlo a número de punto flotante
    let precio = parseFloat(prompt("Ingrese el precio del traje:"));
    
    // Calcular el descuento: 10% del precio si es mayor a 200, de lo contrario 10 unidades monetarias
    let descuento = precio > 200 ? precio * 0.1 : 10;
    
    // Calcular el precio con descuento
    let precioConDescuento = precio - descuento;
    
    // Calcular el IVA del 15% sobre el precio con descuento
    let iva = precioConDescuento * 0.15;
    
    // Calcular el total a pagar sumando el precio con descuento y el IVA
    let totalAPagar = precioConDescuento + iva;
    
    // Mostrar el precio del traje ingresado
    console.log(`Precio del traje ingresado: ${precio}`);
    
    // Mostrar el precio del traje con descuento aplicado
    console.log(`El precio del traje con descuento es: ${precioConDescuento}`);
    
    // Mostrar el valor del IVA calculado
    console.log(`El valor del IVA es: ${iva}`);
    
    // Mostrar el total a pagar (precio con descuento + IVA)
    console.log(`El total a pagar es: ${totalAPagar}`);
}

function ejercicio11() {
    // Algoritmo que presenta el nombre de un día de la semana dado su número
    console.clear();
    
    // Definir un arreglo con los nombres de los días de la semana
    const diasSemana = ["Domingo", "Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado"];
    
    // Solicitar al usuario un número del 1 al 7 para representar un día de la semana
    let numeroDia = parseInt(prompt("Ingrese un número del 1 al 7 para representar un día de la semana:"));
    
    // Verificar si el número ingresado es válido (entre 1 y 7)
    if (numeroDia >= 1 && numeroDia <= 7) {
        // Mostrar el nombre del día correspondiente al número ingresado
        console.log(`El día correspondiente al número ${numeroDia} es: ${diasSemana[numeroDia - 1]}`);
    } else {
        // Mostrar un mensaje de error si el número no es válido
        console.log("Número de día no válido.");
    }
}

function ejercicio12() {
    // Algoritmo que presenta el nombre de un mes del año dado su número
    console.clear();
    
    // Definir un arreglo con los nombres de los meses del año
    const nombresMeses = ["Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio", "Julio", "Agosto", "Septiembre", "Octubre", "Noviembre", "Diciembre"];
    
    // Solicitar al usuario un número del 1 al 12 para representar un mes del año
    let numeroMes = parseInt(prompt("Ingrese un número del 1 al 12 para representar un mes:"));
    
    // Verificar si el número ingresado es válido (entre 1 y 12)
    if (numeroMes >= 1 && numeroMes <= 12) {
        // Mostrar el nombre del mes correspondiente al número ingresado
        console.log(`El mes correspondiente al número ${numeroMes} es: ${nombresMeses[numeroMes - 1]}`);
    } else {
        // Mostrar un mensaje de error si el número no es válido
        console.log("Número de mes no válido.");
    }
}


function ejercicio13() {
    // Dado 5 nombres almacenarlos en un arreglo y luego presentar cada nombre del arreglo desde el último al primero sin usar ciclos.
    console.clear();
    let nombres = [];
    
    // Solicitar al usuario cinco nombres y almacenarlos en un arreglo
    for (let i = 0; i < 5; i++) {
        let nombre = prompt(`Ingrese el nombre ${i + 1}:`);
        nombres.push(nombre);
    }
    
    // Mostrar los nombres en orden inverso usando reverse() y join() para formatear la salida
    console.log("Nombres ingresados de forma inversa:");
    console.log(nombres.reverse().join("\n"));
}

function ejercicio14() {
    // Dada una dirección cualquiera presentar el primer carácter, el del medio y el último de dicha dirección.
    console.clear();
    
    // Solicitar al usuario una dirección
    let direccion = prompt("Ingrese una dirección:");
    
    // Obtener el primer carácter
    let primerCaracter = direccion.charAt(0);
    
    // Obtener el último carácter
    let ultimoCaracter = direccion.charAt(direccion.length - 1);
    
    // Obtener el carácter del medio
    let caracterMedio = direccion.charAt(Math.floor(direccion.length / 2));
    
    // Mostrar los caracteres obtenidos
    console.log(`Primer carácter de la dirección: ${primerCaracter}`);
    console.log(`Carácter del medio de la dirección: ${caracterMedio}`);
    console.log(`Último carácter de la dirección: ${ultimoCaracter}`);
}

function ejercicio15() {
    // Almacenar 5 valores aleatorios en un arreglo e imprimir el primer valor si es par positivo y el último si es impar negativo.
    console.clear();
    let numeros = [];
    
    // Generar y almacenar cinco valores aleatorios en el arreglo
    for (let i = 0; i < 5; i++) {
        numeros.push(Math.floor(Math.random() * 100)); // Genera números aleatorios entre 0 y 99
    }
    
    // Mostrar los valores generados
    console.log("Valores aleatorios generados:");
    console.log(numeros);

    // Verificar y mostrar el primer número si es par y positivo
    if (numeros[0] % 2 === 0 && numeros[0] > 0) {
        console.log(`El primer número (${numeros[0]}) es par y positivo.`);
    } else {
        // Mostrar el último número si el primero no es par y positivo
        console.log(`El último número (${numeros[numeros.length - 1]}) es impar y negativo.`);
    }
}

function ejercicio16() {
    // Dado un arreglo vacío, añadir 3 nombres y presentar el primer y el último carácter de cada nombre desde el arreglo.
    console.clear();
    let nombres = [];
    
    // Solicitar al usuario tres nombres y almacenarlos en el arreglo
    for (let i = 0; i < 3; i++) {
        let nombre = prompt(`Ingrese el nombre ${i + 1}:`);
        nombres.push(nombre);
    }
    
    // Mostrar el primer y el último carácter de cada nombre
    console.log("Primer y último carácter de cada nombre:");
    nombres.forEach(nombre => console.log(nombre.charAt(0), nombre.charAt(nombre.length - 1)));
}

function ejercicio17() {
    // Dada una cadena presentar el primer carácter siempre y cuando sea un dígito
    console.clear();
    
    // Solicitar al usuario una cadena
    let cadena = prompt("Ingrese una cadena:");
    
    // Obtener el primer carácter de la cadena
    let primerCaracter = cadena.charAt(0);
    
    // Verificar si el primer carácter es un dígito y mostrarlo
    if (!isNaN(primerCaracter)) {
        console.log(`El primer carácter es un dígito y es: ${primerCaracter}`);
    } else {
        console.log("El primer carácter no es un dígito.");
    }
}

function ejercicio18() {
    // Dada una cadena presentar el último carácter siempre y cuando sea una letra
    console.clear();
    
    // Solicitar al usuario una cadena
    let cadena = prompt("Ingrese una cadena:");
    
    // Obtener el último carácter de la cadena
    let ultimoCaracter = cadena.charAt(cadena.length - 1);
    
    // Verificar si el último carácter es una letra y mostrarlo
    if (ultimoCaracter.match(/[a-zA-Z]/)) {
        console.log(`El último carácter es una letra y es: ${ultimoCaracter}`);
    } else {
        console.log("El último carácter no es una letra.");
    }
}

function ejercicio19() {
    // Dada una cadena presentar el primer carácter siempre y cuando sea una vocal
    console.clear();
    
    // Solicitar al usuario una cadena
    let cadena = prompt("Ingrese una cadena:");
    
    // Obtener el primer carácter de la cadena
    let primerCaracter = cadena.charAt(0);
    
    // Verificar si el primer carácter es una vocal y mostrarlo
    if (primerCaracter.match(/[aeiouAEIOU]/)) {
        console.log(`El primer carácter es una vocal y es: ${primerCaracter}`);
    } else {
        console.log("El primer carácter no es una vocal.");
    }
}

function ejercicio20() {
    // Dada una cadena presentar el carácter de en medio, siempre y cuando sea un carácter de puntuación
    console.clear();
    
    // Solicitar al usuario una cadena
    let cadena = prompt("Ingrese una cadena:");
    
    // Obtener la longitud de la cadena
    let longitud = cadena.length;
    
    // Obtener el carácter del medio
    let caracterMedio = cadena.charAt(Math.floor(longitud / 2));
    
    // Verificar si el carácter del medio es un carácter de puntuación y mostrarlo
    if (caracterMedio.match(/[;:.,]/)) {
        console.log(`El carácter del medio es un carácter de puntuación y es: ${caracterMedio}`);
    } else {
        console.log("El carácter del medio no es un carácter de puntuación.");
    }
}

function ejercicio21() {
    // Dado dos caracteres, indicar si son iguales o si el primero es menor que el segundo o mayor que el segundo
    console.clear();
    
    // Solicitar al usuario dos caracteres
    let caracter1 = prompt("Ingrese el primer carácter:");
    let caracter2 = prompt("Ingrese el segundo carácter:");
    
    // Comparar los caracteres y mostrar el resultado
    if (caracter1 === caracter2) {
        console.log("Los caracteres son iguales.");
    } else if (caracter1 < caracter2) {
        console.log(`El primer carácter (${caracter1}) es menor que el segundo carácter (${caracter2}).`);
    } else {
        console.log(`El primer carácter (${caracter1}) es mayor que el segundo carácter (${caracter2}).`);
    }
}

function ejercicio22() {
    // Dado dos nombres, indicar si son iguales o si el primero es menor que el segundo o mayor que el segundo
    console.clear();
    
    // Solicitar al usuario dos nombres
    let nombre1 = prompt("Ingrese el primer nombre:");
    let nombre2 = prompt("Ingrese el segundo nombre:");
    
    // Comparar los nombres y mostrar el resultado
    if (nombre1 === nombre2) {
        console.log("Los nombres son iguales.");
    } else if (nombre1 < nombre2) {
        console.log(`El primer nombre (${nombre1}) es menor que el segundo nombre (${nombre2}).`);
    } else {
        console.log(`El primer nombre (${nombre1}) es mayor que el segundo nombre (${nombre2}).`);
    }
}

function ejercicio23() {
    // Dada una cadena, indicar cuántos elementos tiene, sin usar ciclos
    console.clear();
    
    // Solicitar al usuario una cadena
    let cadena = prompt("Ingrese una cadena:");
    
    // Obtener y mostrar la cantidad de elementos de la cadena
    let cantidadElementos = cadena.length;
    console.log(`La cadena tiene ${cantidadElementos} elementos.`);
}

function ejercicio24() {
    // Dado un arreglo, indicar cuántos elementos tiene, sin usar ciclos
    console.clear();
    
    // Solicitar al usuario los elementos del arreglo separados por comas
    let arreglo = prompt("Ingrese los elementos del arreglo separados por comas:");
    
    // Dividir la cadena ingresada en un arreglo de elementos
    let elementos = arreglo.split(",");
    
    // Obtener y mostrar la cantidad de elementos del arreglo
    let cantidadElementos = elementos.length;
    console.log(`El arreglo tiene ${cantidadElementos} elementos.`);
}


// Menú principal
function menu() {  //Esta funcion una vez llamda para iniciar mostrara el menu del programa 
    console.clear();

        console.log("xXx-·=»‡«=·- Menu Ejercicios -·=»‡«=·-xXx");
        console.log("1) Transformar de grados Celsius a Fahrenheit");
        console.log("2) Obtener el doble y el triple de un número entero");
        console.log("3) Calcular producto, suma y media aritmética de 4 variables");
        console.log("4) Convertir peso de libras a kilogramos y gramos");
        console.log("5) Resolver expresión matemática");
        console.log("6) Calcular sueldo de empleado");
        console.log("7) Presentar el mayor de dos números (si el primero es par y el segundo impar)");
        console.log("8) Verificar carácter (letra, signo de puntuación, otro)");
        console.log("9) Determinar costo total por cantidad de colas");
        console.log("10) Aplicar descuento a trajes y calcular pago con IVA");
        console.log("11) Presentar el nombre de un día de la semana");
        console.log("12) Presentar el nombre de un mes del año");
        console.log("13) Presentar nombres ingresados de forma inversa");
        console.log("14) Presentar primer, medio y último carácter de una dirección");
        console.log("15) Presentar primer valor si es par positivo y último si es impar negativo");
        console.log("16) Añadir nombres y presentar primer y último carácter de cada nombre");
        console.log("17) Presentar primer carácter si es un dígito");
        console.log("18) Presentar último carácter si es una letra");
        console.log("19) Presentar primer carácter si es una vocal");
        console.log("20) Presentar carácter del medio si es un carácter de puntuación");
        console.log("21) Indicar si dos caracteres son iguales o si el primero es menor que el segundo o mayor que el segundo");
        console.log("22) Indicar si dos nombres son iguales o si el primero es menor que el segundo o mayor que el segundo");
        console.log("23) Indicar cuántos elementos tiene una cadena, sin usar ciclos");
        console.log("24) Indicar cuántos elementos tiene un arreglo, sin usar ciclos");
    

        let opcion = parseInt(prompt("Elija opción [1...24]:"));
// Esto funcionara segun el numero ingresado y llamara a las funcion del ejercicio maracdo del 1 al 24 
//Por ejemplo si el usuario marca 5 , se activara el "case 5" lo cual llamara a ña funcion ejercicio5()
//asi con todo los 24 ejercicios
        switch (opcion) {
            case 1:
                ejercicio1();
                break;
            case 2:
                ejercicio2();
                break;
            case 3:
                ejercicio3();
                break;
            case 4:
                ejercicio4();
                break;
            case 5:
                ejercicio5();
                break;
            case 6:
                ejercicio6();
                break;
            case 7:
                ejercicio7();
                break;
            case 8:
                ejercicio8();
                break;
            case 9:
                ejercicio9();
                break;
            case 10:
                ejercicio10();
                break;
            case 11:
                ejercicio11();
                break;
            case 12:
                ejercicio12();
                break;
            case 13:
                ejercicio13();
                break;
            case 14:
                ejercicio14();
                break;
            case 15:
                ejercicio15();
                break;
            case 16:
                ejercicio16();
                break;
            case 17:
                ejercicio17();
                break;
            case 18:
                ejercicio18();
                break;
            case 19:
                ejercicio19();
                break;
            case 20:
                ejercicio20();
                break;
            case 21:
                ejercicio21();
                break;
            case 22:
                ejercicio22();
                break;
            case 23:
                ejercicio23();
                break;
            case 24:
                ejercicio24();
                break;
            case "atras":  
              break;
            default:
                console.log("Opción no válida."); //por el el usuario ingrega algo fuera de la lista 
        }
        let volver = prompt("Presione 's' para volver al menú principal:"); //ya que la consola se limpia con esto regresamos 
        if (volver === 's') { //y llamamos a la funcion menu para mostralo otra vez 
            menu();
}
}

// Llamar a la función del menú para iniciar el programa
menu();
