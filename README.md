Control de Corriente y Sensores para Motores
El documento aborda el uso de sensores para medir la corriente en motores eléctricos, destacando las limitaciones de los sensores de efecto Hall para aplicaciones de baja corriente y recomendando el uso de resistencias shunt para una medición más precisa.
1. Sensores de efecto Hall vs. Resistencias Shunt
•	Sensores de efecto Hall: Funcionan midiendo el campo magnético generado por la corriente, pero su precisión es baja en motores de bajo consumo (<1 A). No se recomienda su uso en aplicaciones de corriente baja debido a la baja señal de voltaje obtenida.
•	Resistencias Shunt: Se colocan en serie con la carga para medir el voltaje a través de la resistencia, permitiendo calcular la corriente mediante la Ley de Ohm. Es un método más confiable para motores de baja potencia.
•	Se menciona que el puente H L298 permite la instalación de una resistencia shunt en un pin específico, facilitando la medición de corriente sin afectar el funcionamiento del circuito.
Drivers de Potencia y Modulación PWM
El documento explica el uso de drivers de potencia como el puente H y los transistores de conmutación en la alimentación de motores eléctricos.
2. Puentes H y PWM
•	Se destaca el uso de PWM (Modulación por Ancho de Pulso) para controlar la velocidad de motores DC mediante la variación del ciclo de trabajo.
•	Se menciona que el puente H L298 es uno de los más utilizados, ya que permite controlar hasta 2 A en dos motores.
•	En motores AC, en lugar de PWM convencional, se usa una técnica llamada SPWM (PWM senoidal), donde la señal de control es una onda senoidal modulada con una señal triangular para generar un patrón de conmutación.
3. Inversores de Potencia para Motores AC
•	Se describe el funcionamiento de los inversores de potencia, utilizados para alimentar motores AC.
•	Se menciona la necesidad de sincronizar las señales de conmutación para generar una onda senoidal, asegurando una alimentación eficiente del motor.
•	Se indica que en motores trifásicos se requiere la coordinación de los disparos de los transistores para obtener el movimiento adecuado del motor.
•	En aplicaciones comerciales, los motores eléctricos suelen incluir estos sistemas de inversores con filtros para convertir la señal PWM en una onda senoidal más estable.
Implementación Práctica en Motores con Arduino
•	Se menciona que muchas tarjetas de Arduino con módulos L298 no incluyen acceso al pin de medición de corriente, lo que impide el uso directo de resistencias shunt.
•	Se recomienda utilizar el integrado L298 directamente para poder medir la corriente correctamente sin modificaciones en la tarjeta.
Conclusión
•	Para aplicaciones de baja corriente, se recomienda el uso de resistencias shunt en lugar de sensores de efecto Hall.
•	Se enfatiza la importancia del uso de PWM en el control de motores DC, y SPWM en motores AC.
•	Se sugiere la implementación de inversores de potencia con filtrado para mejorar la calidad de la señal de alimentación de motores AC.
•	Se advierte sobre las limitaciones de algunos módulos de Arduino con L298 y la necesidad de modificaciones para medir corriente con resistencias shunt.

