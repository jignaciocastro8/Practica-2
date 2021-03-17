# LVA_practica
### Índices invertibles

## 1. Desarrollo de cálculo de índices:
* [x] Dado un grupo de instrumentos con precio poder calcular la rentabilidad y valor del índice que tiene en un periodo de tiempo.
* [x] Agregar rebalanceos con frecuencia mensual, semanal, quincenal.
* [x] Es importante que el criterio de selección de instrumentos esté desacoplado de manera que se pueda cambiar con facilidad. Todo lo que viene a continuación se testea como: crear un criterio de selección y calcular los valores que habría tenido el índice. Si no está bien separado van a tener que modificar mucho código.

### Consideraciones: 
Las siguientes fechas presentan problemas para el índice LKXCXLK. Se cree que es por el ingreso o salida de bonos al índice, pero al no tener claro las reglas de rebalanceo no se siguió ahondando en buscar una solución:
* [x] 2020-04-01
* [x] 2020-09-01
* [x] 2020-09-02
* [x] 2020-09-09
* [x] 2020-09-10

La fecha 09-09 es problema tanto para el índice LXCXLK como para el LKXCXRY. Se cree que los datos que se utilizan son diferentes a con los que se comparan para esta fecha en particular.

## 2. Encontrar empresas invertibles:
* [x] Obtener respuestas a preguntas como: porcentaje de fondos mutuos tiene al menos un X% invertido en instrumentos con montos menores o iguales a Y. Esta pregunta permite entender más o menos cuánto un fondo mutuo va a comprar de un instrumento en el que quiera invertir. Separar por tipo de fondo.
* [x] Definir criterios de invertibilidad en base al tamaño de las _posiciones_ en bonos y renta variable de los fondos mutuos. El criterio puede variar dependiendo del tipo de instrumento, bonos, depósitos, acciones.
* [x] Determinar universo de acciones e instrumentos de renta fija que cumplan los criterios.
* [x] Analizar si es necesario reajustar los criterios para lograr un mejor equilibrio entre buenos criterios y buen universo de instrumentos.

## 3. Análisis de sentiment de Twitter:
* [x] Revisar la API de Twitter y conectarse a ella.
* [x] Encontrar información relativa a empresas chilenas en Twitter del universo de empresas de la parte anterior.
* [x] Ver si es necesario homologar nombres de empresas para la búsqueda.
* [ ] Analizar volúmenes de data por empresa por periodo de tiempo. Cuánta data hay de Enelam, Falabella, Quiñenco? En una semana, en un mes?
* [ ] Listar todo el universo de empresas que hay en RV y en RF en la bolsa de comercio (BCS).
* [x] Hacer un score sobre sentiment de las empresas que transan en la bolsa de comercio.
* [ ] Ver si el score tiene correlación con la rentabilidad ([X] semanal, [X] mensual, [ ] anual) de la acción de la empresa o sus bonos.

## 4. Calcular índices con data de sentiment
* [ ] Definir una estrategia para determinar si invertir o no en una empresa según el score obtenido en el paso anterior.
* [ ] Analizar el rendimiento histórico del índice para un periodo de tiempo de al menos un año.

## 5. Hacer índices de otras estrategias:
* [ ] Momentum
* [ ] Carry trading con forwards de moneda
* [ ] Por apuesta a movimientos de curva de tasas

### Estructuras Generales

* Utilizar Visual Studio Code, con Liveshare. De manera que programen en un solo código.
* Crear un repositorio con el código.
* Evitar escribir funciones largas. Si la función es muy larga quizás son varios llamados a otras funciones.
* Comentar funciones. Lo que hacen, lo que reciben (qué tipos de datos son y qué deben tener) y lo que entregan.
* Poner nombres de variables que representen lo que son. Evitar nombrar variables como: data, parámetro, info, valor.
* Utilizar interfaces que obtengan la data. De forma de tener separada la obtención de data de los procesos de cálculo.