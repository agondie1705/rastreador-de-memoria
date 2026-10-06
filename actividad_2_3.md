Rastreador de memoria
// CONFIGURACIÓN DE DEPURACIÓN
const _DEBUGMODE = true;
 
// === ZONA 1 ===
if (_DEBUGMODE) console.log("Log A:", producto); 
var producto = "Teclado Mecánico";
if (_DEBUGMODE) console.log("Log B:", producto);
 
 
// === ZONA 2 ===
function laboratorioScope() {
    var descuento = 10;
    
    if (true) {
        let descuento = 25;
        const impuesto = 0.21;
        if (_DEBUGMODE) console.log("Log C:", descuento);
    }
    
    if (_DEBUGMODE) console.log("Log D:", descuento);
    
    try {
        if (_DEBUGMODE) console.log("Log E:", impuesto);
    } catch (error) {
        if (_DEBUGMODE) console.log("Log E: ¡ERROR CATÁSTROFICO!");
    }
}
 
laboratorioScope();
 
 
// === ZONA 3 ===
try {
    if (_DEBUGMODE) console.log("Log F:", precio);
    let precio = 49.99;
} catch (error) {
    if (_DEBUGMODE) console.log("Log F: ¡ERROR CATÁSTROFICO!");
}

 Tabla de predicciones

CHATO USADO PARA LAS CORRECCIONES ORTOGRÁFICAS
Identificador 
¿Qué imprimirá la consola? (Predicción) 
Justificación Teórica (Usa términos como: Hoisting, Ámbito de bloque, Ámbito de función, Undefined,...) 
Log A 
Imprimirá undefined 
Ya que la variable tiene hoisting, es decir, se llama a producto antes de que tenga su valor asignado, por eso es undefined.


Log B 
Imprimirá Teclado Mecánico 
Lo imprimirá correctamente al encontrarse ya con la variable producto creada. 
Log C 
Imprimirá 25
Lo imprimirá porque sustituye el descuento 10 por un 25, ya que let tiene un ámbito de bloque.
Log D 
Imprimirá 10
Lo imprimirá debido a que el descuento = 25 es un let y tiene un ámbito de bloque. 
Log E 
Imprimirá Log E: ¡ERROR CATÁSTROFICO
Lo imprimirá así debido al mismo problema de arriba, que como el impuesto es una const tiene ámbito de bloque y no se aplica. 
Log F 
Imprimirá Log F: ¡ERROR CATÁSTROFICO!
Ya que el precio también tiene ámbito de bloque y porque se encuentra en el TDZ al ser un let y llamarse antes de crearla; si fuese un var sería undefined. 


comprobaciones

<img width="683" height="533" alt="image" src="https://github.com/user-attachments/assets/1cc7b2b7-c567-488f-a89b-d2448a3053f5" />


Tengo la tabla correcta

Conclusion crítica:
Es mejor usar let o const ya que tienen el ámbito de bloque que te da más control sobre el código y no detecta los errores dejándose muchos atras.
