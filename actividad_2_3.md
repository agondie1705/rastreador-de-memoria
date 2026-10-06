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


<img width="685" height="702" alt="image" src="https://github.com/user-attachments/assets/fd4495e4-1b96-4276-8fa8-2296ad277baa" />

comprobaciones

<img width="683" height="533" alt="image" src="https://github.com/user-attachments/assets/1cc7b2b7-c567-488f-a89b-d2448a3053f5" />


Tengo la tabla correcta

Conclusion crítica:
Es mejor usar let o const ya que tienen el ámbito de bloque que te da más control sobre el código y no detecta los errores dejándose muchos atras.
