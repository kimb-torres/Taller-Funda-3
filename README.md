#*Descripción del problema*

*El presente proyecto consiste en el desarrollo de un SumadorCompletoUnBit utilizando el lenguaje de descripción de hardware Verilog. El objetivo del circuito es realizar la suma de dos bits de entrada, representados por bitEntradaA y bitEntradaB, junto con un bit adicional denominado acarreoEntrada. Como resultado de la operación, el circuito genera un bit de suma llamado bitResultadoSuma y un bit de acarreo de salida denominado acarreoSalida.*

*Para realizar el cálculo de la suma, primero se obtiene el valor intermedio resultadoXorEntradas, el cual corresponde a la operación XOR entre bitEntradaA y bitEntradaB. Posteriormente, este resultado se combina con acarreoEntrada mediante una segunda operación XOR para obtener el valor de bitResultadoSuma.*

*El cálculo del acarreo se realiza mediante dos señales internas. La primera, acarreoGeneradoPorEntradas, se activa cuando tanto bitEntradaA como bitEntradaB tienen un valor lógico de 1. La segunda, acarreoGeneradoPorAcarreo, se activa cuando acarreoEntrada es igual a 1 y además resultadoXorEntradas es igual a 1. Finalmente, ambas señales son combinadas mediante una operación OR para generar acarreoSalida.*

*Con el fin de verificar el funcionamiento del circuito, se implementó un módulo denominado BancoDePruebas. Este módulo asigna las ocho combinaciones posibles de valores para bitEntradaA, bitEntradaB y acarreoEntrada, permitiendo comprobar que los valores obtenidos en bitResultadoSuma y acarreoSalida coinciden con la tabla de verdad de un sumador completo de un bit. Además, los resultados son mostrados en pantalla mediante instrucciones $display, incluyendo el resultado binario completo formado por acarreoSalida y bitResultadoSuma.*

#*Retos afrontados*

*Uno de los principales retos durante el desarrollo fue comprender cómo implementar un sumador completo utilizando únicamente operaciones lógicas. Para ello fue necesario analizar la función de las señales internas resultadoXorEntradas, acarreoGeneradoPorEntradas y acarreoGeneradoPorAcarreo, entendiendo cómo contribuyen al cálculo de bitResultadoSuma y acarreoSalida.*

*Otro desafío consistió en la construcción del módulo BancoDePruebas, ya que fue necesario definir correctamente todas las combinaciones posibles de entrada para verificar el funcionamiento del circuito. Asimismo, se requirió comprender la forma de conectar las señales del módulo SumadorCompletoUnBit mediante la instanciación circuitoSumador.*

#*Conclusiones*:
*Este proyecto permitió comprender mejor el funcionamiento de un sumador completo y la forma en que las operaciones lógicas pueden utilizarse para realizar sumas binarias. Además, el uso de Verilog facilitó la simulación y verificación del circuito mediante las diferentes combinaciones de entrada, comprobando que los resultados obtenidos fueron los esperados,es un taller bastante curiosa y el lenguaje no era malo además de tener que implementar conceptos anteriores al curso,muy interesante.*
