Bitácora del proyecto
Mi proyecto consiste en controlar el movimiento de un servomotor usando un potenciómetro. A medida que giro el potenciómetro, el servo se mueve según la posición que tenga.
Al principio del proyecto tuve que investigar para qué servía cada componente y cómo funcionaban. Aprendí que el potenciómetro entrega una señal variable y que el servomotor se mueve según la señal que reciba desde la placa. Al comienzo me costó entender cómo relacionar esos dos valores, pero con ejemplos y pruebas lo fui entendiendo mejor.
Después armé el circuito. Conecté el potenciómetro a una entrada analógica y el servo a otro pin , además de la alimentación y la tierra. En los primeros intentos el servomotor no se movía y el problema era que había hecho mal algunas conexiones. Revisando todo con más atención pude corregirlo.
Luego pasé a la parte de programación. Cargué una libreria (servo) que lee el valor del potenciómetro y lo transforma en un ángulo para mover el servomotor. Al principio no entendia como se pasaba el valor analogico a grados por lo cual el potenciometro no se movia, pero pude resolverlo viendo un tutorial sobre la libreria.
Cuando terminé el armado y la programación, hice varias pruebas girando el potenciómetro de a poco. Finalmente logré que el servomotor se mueva de manera proporcional al movimiento del potenciómetro, cumpliendo con el objetivo del proyecto.
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
