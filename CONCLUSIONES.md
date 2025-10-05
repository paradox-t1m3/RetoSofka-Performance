\## 🧾 Conclusiones



\### 🔍 Hallazgos Relevantes



\- El sistema alcanzó una tasa de éxito superior al \*\*97%\*\* en las transacciones evaluadas, lo que refleja una alta confiabilidad bajo carga.

\- El \*\*percentil 99\*\* se mantuvo en \*\*297 milisegundos\*\*, indicando que incluso en los escenarios más exigentes, los tiempos de respuesta fueron aceptables.

\- No se registraron errores durante la ejecución de las pruebas, lo que confirma la \*\*estabilidad funcional\*\* del sistema.

\- La \*\*latencia de bloqueo\*\* fue mínima, lo que sugiere una arquitectura eficiente y bien optimizada.

\- Se observó una \*\*correlación directa entre usuarios virtuales y peticiones por segundo\*\*, lo que evidencia un comportamiento \*\*escalable\*\* sin degradación significativa.

\- Las métricas de red mostraron un manejo adecuado de volúmenes de datos, con tasas de transferencia estables y sin saturación.



\### 🛠️ Recomendaciones



\- Realizar pruebas de carga progresiva para identificar el umbral máximo de usuarios concurrentes antes de que se degrade el rendimiento.

\- Documentar la configuración actual del entorno (hardware, red, parámetros de JMeter) para asegurar reproducibilidad en futuras ejecuciones.

\- Implementar monitoreo en tiempo real durante las pruebas para correlacionar métricas de aplicación con métricas de infraestructura.

\- Verificar la disponibilidad y correcta respuesta de los endpoints antes de ejecutar cualquier escenario de prueba.

\- Revisar la arquitectura para identificar oportunidades de optimización en componentes que gestionan concurrencia o acceso a recursos compartidos.



\### 📌 Conclusión General



El sistema demostró un rendimiento sólido y consistente bajo condiciones de carga controlada. La arquitectura respondió de forma eficiente, manteniendo tiempos de respuesta bajos, sin errores, y con una capacidad clara de escalar ante el aumento de usuarios concurrentes. Estos resultados permiten validar la robustez del sistema y ofrecen una base confiable para futuras optimizaciones o despliegues en producción.



