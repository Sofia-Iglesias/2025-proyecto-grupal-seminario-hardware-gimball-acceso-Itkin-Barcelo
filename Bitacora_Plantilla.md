Bitácora de Control de Servomotor con Potenciómetro
Tecnología de los Sistemas de Información - Seminario Avanzado
Ciclo Lectivo 2025

Mi proyecto consiste en controlar el movimiento de un servomotor usando un potenciómetro. A medida que giro el potenciómetro, el servo se mueve según la posición que tenga.
Integrante/s
José Barcelo


Agustín Samuel Itkin



Semanas 1-2
Actividades Realizadas:
Investigación sobre el funcionamiento del potenciómetro y el servomotor.


Análisis de cómo se relaciona la señal del potenciómetro con el movimiento del servo.


Dificultades:
Dificultad para entender cómo convertir el valor analógico del potenciómetro en un movimiento concreto del servomotor.


Falta de experiencia inicial con este tipo de componentes.


Próximos Pasos:
Armar el circuito completo.


Conectar correctamente el potenciómetro y el servomotor a la placa.


Semana 3-4
Actividades Realizadas:
Armado del circuito conectando el potenciómetro a una entrada analógica y el servomotor a un pin correspondiente, junto con alimentación y tierra.


Corrección de errores en las conexiones que impedían el movimiento del servomotor.


Carga de la librería Servo y programación para leer el valor del potenciómetro.


Conversión del valor analógico a grados para mover el servomotor.


Pruebas finales girando el potenciómetro y verificando el movimiento proporcional del servo.


Dificultades:
El servomotor no se movía en los primeros intentos por conexiones incorrectas.


No se entendía al principio cómo transformar el valor del potenciómetro en un ángulo.




Como reflexión final, este proyecto me ayudó a entender mejor cómo se relacionan los sensores con los actuadores, y cómo la programación permite controlar componentes electrónicos. También aprendí que es muy importante revisar bien las conexiones y tener paciencia para detectar errores.
Como posibles mejoras, se podría agregar una pantalla para mostrar el ángulo del servo, hacer que el movimiento sea más suave o usar este sistema para controlar algún mecanismo más complejo, como un brazo robótico.

Esquemas:




Simulacion:
https://www.tinkercad.com/things/evgIxTyheN9-brilliant-leelo/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=tfhZ33THhKdLGBjRE77FewtrGdRQgXCRu1yl0B8ik7M



Codigo explicado:

int lectura1 = analogRead(pot1);
  int grados1 = map(lectura1, 0, 1023, 0, 180);
  Servo1.write(grados1);

  int lectura2 = analogRead(pot2);
  int grados2 = map(lectura2, 0, 1023, 0, 180);
  Servo2.write(grados2);

lo mas importante y especifico del codigo del proyecto es esto que funciona leyendo los potenciometros primeramente y luego usando la funcion mapear para pasar de un valor de un rango a otro rango proporcional. Luego el servo actua respecto a esto.
