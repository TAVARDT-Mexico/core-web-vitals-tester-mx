# Medidor de Core Web Vitals y Rendimiento Web

[![Medidor Core Web Vitals](https://img.shields.io/badge/TAVARDT-Core%20Web%20Vitals-5b3cf5.svg)](https://tools.tavardt.com/mx/medidor-core-web-vitals/)
[![Jurisdiccion](https://img.shields.io/badge/Jurisdiccion-Mexico-00C853.svg)](https://ag.tavardt.com/mx/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Evaluacion de latencia TTFB, bloqueo de renderizado y estabilidad de diseno en infraestructuras de Mexico.

Desarrollado y mantenido por la division de ingenieria de velocidad y rendimiento de **[TAVARDT Mexico](https://ag.tavardt.com/mx/)**.

---

## Capacidades de Auditoria de Core Web Vitals

* **Medicion de Latencia y TTFB**: Evaluacion de tiempo de respuesta de servidor (Time to First Byte) en infraestructuras digitales.
* **Deteccion de Recursos Bloqueantes**: Localizacion de hojas de estilo y scripts sincronos en cabecera que retrasan el renderizado.
* **Control de Desplazamiento de Diseno (CLS)**: Revision de dimensiones fijas y carga diferida en imagenes.
* **Auditoria de Compresion**: Verificacion de codificacion Brotli o Gzip en transferencias HTTP.
* **Puntuacion de Rendimiento W3C**: Calificacion de 0 a 100 con recomendaciones tecnicas priorizadas.

---

## Instalacion y Ejecucion

Requiere Python 3.8 o superior sin dependencias externas.

```bash
git clone https://github.com/TAVARDT-Mexico/core-web-vitals-tester-mx.git
cd core-web-vitals-tester-mx
python cwv_tester.py https://empresa.com.mx
```

Para salida en formato JSON:

```bash
python cwv_tester.py https://empresa.com.mx --json
```

---

## Diagnostico Completo en la Web

Para auditorias avanzadas de velocidad y respuesta:

* **[Medidor de Core Web Vitals Oficial](https://tools.tavardt.com/mx/medidor-core-web-vitals/)**
* **[Portal Corporativo TAVARDT Mexico](https://ag.tavardt.com/mx/)**

---

## Consultoria en Optimizacion y Rendimiento Web

Para arquitectura de carga ultrarrapida bajo directrices de Estandares W3C y Mejores Practicas de Velocidad Web, contacte a **[TAVARDT Mexico](https://ag.tavardt.com/mx/contacto/)**.
