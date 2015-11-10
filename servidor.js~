#!/usr/bin/env node

/**
 * 
 * @author Antonio Espinosa Jiménez
 */

//incluyo el módulo necesario http
var http = require('http');

//inicializo las visitas iniciales a 0
var contador = 0;

/**
 * 
 * En cada conexión devuelve un código HTML con el número actual de visitas,
 * incrementado el valor de contador en uno cada vez que recibe una petición.
 * Escucha en el puerto 8081.
 */
http.createServer(function (req, res) {
    contador++;
    console.log('Nueva conexion --> ' + 'contador: ' + contador);
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">');
    res.write('<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">');
    res.write('<title>Ejercicio de Node.js (Contador de visitas)</title></head>');
    res.write('<body style="background-color:#A9A9F5"><h1 style="text-align:center">Bienvenid@ a mi web</h1>');
    res.write('<p style="text-align:center">El número actual de visitas es: ' + contador + '</p>');
    res.write('</body></html>');
    res.end();
}).listen(8081);

//muestro en la terminal que se está ejecutando
console.log("Servidor ejecutándose en http://127.0.0.1:8081/");