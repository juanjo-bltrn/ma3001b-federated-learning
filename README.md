# ma3001b-federated-learning

## Conclusiones

La exactitud (accuracy) de las cuatro funciones de agregación implementadas son los siguientes:

- FedAvg: 0.25
- FedMedian: 0.33
- FedAdam: 0.10
- FedTrimmedAvg: 0.37

Como se puede observar, en este caso, la mediana tuvo mejores resultados que la media, aunque esto no es algo que pueda ser extrapolado necesariamente a otros casos, ya que en teoría ambas métricas deberían de funcionar con una exactitud similar.

Las otras dos funciones fueron realizadas con ayuda de la librería Flowers, especializada en aprendizaje federado automatizado y optimizado en línea, por lo que, al ser utilizado de una forma diferente a la que fue creada, es decir, localmente, no se hace uso de su máximo potencial. Esto se puede ver especialmente con la función FedAdam, la cual se basa en el algoritmo de optimización ADAM, cuyo éxito requiere de ser iterado múltiples veces. Esto explica por qué dicha función tuvo un desempeño tan pobre. 

La función de media truncada fue la de mejor desempeño, ya que es simplemente una versión mejorada de FedAvg, lo que viene bien para este caso.