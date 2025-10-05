# 🚀 Proyecto de Pruebas de Performance con Apache JMeter

Este proyecto tiene como objetivo evaluar el rendimiento de una aplicación web mediante pruebas de carga automatizadas. Se simulan múltiples usuarios concurrentes para medir tiempos de respuesta, estabilidad, transferencia de datos y escalabilidad del sistema bajo diferentes escenarios.

---

## 🎯 Objetivo del Proyecto

- Validar la capacidad del sistema para manejar múltiples usuarios simultáneos.
- Identificar posibles cuellos de botella en tiempos de respuesta, transferencia de datos o saturación de recursos.
- Obtener métricas confiables para tomar decisiones de optimización y escalabilidad.

---

## 🧪 Estructura del Plan de Pruebas

El plan de pruebas está diseñado en Apache JMeter y contiene los siguientes componentes:

- **Plan de Pruebas**
  - `CSV Data Set Config`: configuración de datos de entrada para escenarios dinámicos.
  - `Grupo de Hilos`: define el número de usuarios virtuales y duración de la prueba.
    - `Petición HTTP`: solicitud al endpoint bajo prueba.
      - `Gestor de Cabecera HTTP`: define headers como Content-Type, Authorization, etc.
      - `Aserción de Respuesta`: valida códigos de estado y contenido esperado.
      - `Ver Árbol de Resultados`: muestra respuestas individuales.
      - `Informe Agregado`: consolida métricas como TPS, latencia, errores, percentiles.

---

## 🛠️ Herramientas Utilizadas

- **Apache JMeter 5.5+**: herramienta principal para pruebas de carga.
- **Java 8+**: entorno de ejecución requerido por JMeter.
- **CSV Data Set**: archivo externo para parametrizar escenarios.
- **Postman / Swagger**: para validar endpoints antes de automatizar.
- **Git**: control de versiones del pvroyecto.

---

## 🔧 Configuración en JMeter

El componente `CSV Data Set Config` permite parametrizar los datos de entrada para los escenarios de prueba. A continuación se detalla su configuración recomendada:

- **Filename**: `usuarios.csv`
- **Variable Names**: `usuario,password,token`
- **Delimiter**: `,`
- **Recycle on EOF**: `True`
- **Stop thread on EOF**: `False`
- **Sharing Mode**: `All threads`

Esto asegura que cada hilo (usuario virtual) utilice datos únicos por iteración, permitiendo simular múltiples usuarios con credenciales distintas.

---

##▶️ Cómo Ejecutar el Proyecto

1. Abrir Apache JMeter y cargar el archivo `.jmx` correspondiente al plan de pruebas.
2. Verificar que el archivo CSV esté ubicado correctamente y que las variables estén bien definidas.
3. Configurar el número de hilos (usuarios virtuales), ramp-up y duración en el componente `Thread Group`.
4. Iniciar la ejecución con el botón **Start** o presionando `Ctrl + R`.
5. Observar los resultados en tiempo real a través de los listeners:
   - `Ver Árbol de Resultados`
   - `Informe Agregado`
   - `Tabla de Resultados`
   - `Gráficos de rendimiento`

---

## 📊 Cómo Revisar los Resultados

- **Ver Árbol de Resultados**: muestra cada solicitud HTTP con su respuesta, código de estado, cuerpo y encabezados.
- **Informe Agregado**: presenta métricas clave como:
  - Tiempo promedio de respuesta
  - Percentiles (90%, 95%, 99%)
  - Transacciones por segundo (TPS)
  - Porcentaje de errores
- **Tabla de Resultados**: permite exportar los datos en formato `.csv` para análisis externo.
- **Gráficos de rendimiento**: visualizan la relación entre usuarios virtuales y peticiones por segundo, útil para evaluar escalabilidad.

Se recomienda guardar los resultados para comparativas futuras y validación de mejoras en el sistema.

## 👤 Autor

**Christian Villegas Suarez**  
📧 cristvs95@gmail.com  
📱 +57 302 453 5724  
💼 Senior Software Engineer especializado en automatización de pruebas, análisis de rendimiento y documentación técnica.
