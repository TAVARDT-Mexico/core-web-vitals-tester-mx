# Auditor de Core Web Vitals y Rendimiento de Pagina

[![Medidor Core Web Vitals](https://img.shields.io/badge/TAVARDT-Core%20Web%20Vitals-5b3cf5.svg)](https://tools.tavardt.com/mx/medidor-core-web-vitals/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de latencia TTFB, compresion HTTP, recursos bloqueadores de renderizado y estabilidad visual CLS.

Desarrollado y mantenido por la division de ingenieria de rendimiento web e infraestructura digital de **TAVARDT**.

***

## Vectores de Riesgo e Impacto Operativo en Rendimiento Web

La latencia prolongada del servidor y los recursos bloqueadores en el frontend debilitan la conversion y la calificacion en Google. Cuando las plataformas web ofrecen cargas sin comprimir y un TTFB elevado, se disparan los abandonos en dispositivos moviles.

El desplazamiento imprevisto de contenido por imagenes sin dimensiones declaradas afecta negativamente el indice Cumulative Layout Shift. La verificacion automatica asegura una experiencia visual estable y un aprovechamiento maximo del trafico web.

***

## Capacidades Centrales de Auditoria Tecnica

* **Medicion Precisa de TTFB y Latencia**: Evaluacion de la respuesta inicial del servidor mediante cronometros de alta resolucion, alertando ante retrasos superiores a 600 ms o criticos sobre 1200 ms.
* **Inspeccion de Compresion HTTP**: Verificacion del uso de algoritmos modernos Brotli o Gzip, penalizando con 15 puntos la entrega de datos sin comprimir.
* **Deteccion de Bloqueo de Renderizado**: Identificacion de estilos CSS y scripts JS sincronos en `<head>` que no incorporan atributos async, defer o module.
* **Auditoria de Estabilidad Visual (CLS)**: Rastreo de elementos `<img>` sin atributos explicitos de ancho y alto, verificando la aplicacion de carga diferida lazy.
* **Identificacion de Resource Hints**: Deteccion de directivas preconnect y preload implementadas para acelerar peticiones a recursos criticos.
* **Puntuacion de Rendimiento W3C**: Metrica cuantitativa de 0 a 100 clasificando la pagina en GOOD (FAST), NEEDS IMPROVEMENT o POOR (SLOW).

***

## Instalacion y Ejecucion

Requiere Python 3.8 o superior sin librerias adicionales.

```bash
git clone https://github.com/TAVARDT-Mexico/core-web-vitals-tester-mx.git
cd core-web-vitals-tester-mx
python cwv_tester.py https://empresa.com.mx
```

Para generar la salida en formato JSON estructurado en flujos de integracion continua:

```bash
python cwv_tester.py https://empresa.com.mx -j
```

***

## Preguntas Frecuentes (FAQ Tecnico)

### 1. Como afecta un Time to First Byte (TTFB) elevado al rendimiento de Core Web Vitals?
Un TTFB deficiente pospone la descarga del HTML inicial, retrasando la ejecucion del resto de recursos y empeorando la metrica LCP. Cuando el servidor supera los 600 milisegundos, el auditor aplica deducciones de puntaje y advierte sobre problemas de cache.

### 2. Por que los scripts y estilos sincronos en el head detienen la renderizacion?
Las etiquetas sin atributos asincronos obligan al navegador a detener la construccion del DOM mientras se descarga y ejecuta el recurso. El auditor identifica archivos sin async, defer o module para destacar oportunidades de optimizacion critica.

### 3. Que provoca los problemas de Cumulative Layout Shift (CLS) cuando faltan dimensiones en imagenes?
Si no se declaran los atributos de ancho y alto en el HTML, el navegador no puede reservar el espacio necesario antes de descargar la imagen. Esto ocasiona saltos bruscos en el contenido visible que perjudican la estabilidad visual y la experiencia.

### 4. Cual es la relevancia de la compresion HTTP mediante Brotli o Gzip?
La compresion de texto reduce el tamano del payload transferido a traves de la red hasta en un setenta por ciento. La falta de compresion activa consume ancho de banda innecesario e incurre en penalizaciones inmediatas de rendimiento.

### 5. De que forma aceleran la carga directivas como preconnect y preload?
Las directivas preconnect y preload anticipan conexiones DNS y negociaciones TLS hacia origenes clave y tipografias criticas. La herramienta confirma su presencia para asegurar que el navegador ordene las prioridades de descarga eficientemente.

***

## Consultoria en Rendimiento Web y Optimizacion de Velocidad

Para planificacion de infraestructuras veloces y cumplimiento de estandares W3C, consulte al equipo de **TAVARDT**.

***

## Enlaces Utiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnosticos:** https://tools.tavardt.com/mx/
* **Contacto Tecnico:** https://ag.tavardt.com/mx/contacto/

***

### Licencia
Distribuido bajo la Licencia MIT. Consulte el archivo LICENSE para conocer los terminos completos.

***

© 2026 TAVARDT. Todos los derechos reservados.
