# Practica3_aprendizaje_automatico

### Enunciado: Práctica de aprendizaje automático

### Pasos a realizar 
Los pasos a realizar son los que se muestran a continuación:
1. Elegir el problema. La predicción de resultados de partidos en la ATPo en la WTA de tenis, una liga deportiva, una competición de deporteelectrónico, o cualquier otro problema del que se dispongan de datossuficientes como para aplicar algoritmos de aprendizaje automático.
2. Identificar la fuente de datos. Es necesario disponer de una serie dedatos históricos que sirvan para que el sistema aprenda.
 
3. Identificar las características relevantes de los hechos. Por ejemplo, enla predicción del resultado de un encuentro de tenis, algunas caracterís-ticas importantes pueden ser la posición en el ranking de cada jugador,la superficie en que se juega, la edad de cada jugador, etc.

4. Obtener un fichero .arff con los hechos codificados de acuerdo con lascaracterísticas anteriormente elegidas. Este fichero servirá como entra-da para la herramienta Weka2.

5. Evaluar distintos algoritmos de aprendizaje automático con los datosobtenidos. Este paso se llevará a cabo con la herramienta Weka, ytendrá como salida el algoritmo con mejor rendimiento para los datosdatos.

6. Generar en Java un objeto persistente con el algoritmo obtenido en el paso 5. También se realizará con Weka.

7. Implementar un prototipo de aplicación que consulte el objeto persis-tente generado en el paso 6. La aplicación cargará en memoria el objetopersistente, que tendrá como responsabilidad la resolución del proble-ma propuesto (p.ej. el pronóstico de un resultado deportivo), e interac-tuará con el usuario a través de una interfaz (que puede ser de texto) (véase la figura 1.2).

### Material a entregar

Deberá ser el siguiente:

1. Cógido fuente en Java.

2. Los ficheros adicionales necesarios para poder compilar dicho código.

3. El fichero .arff.

### Resolución de la práctica

El problema a resolver para abordar la resolución de la práctica es **el pronóstico de pacientes diabetéticos** en base a una serie de atributos que se comentarán a continuación.

### Fuente de datos 

El dataset utilizado para realizar el análisis se encuentra a través del siguiente enlace: [Fuente de datos](https://www.kaggle.com/code/chirag9073/diabetes-using-deep-learning/notebook)

### Preprocesado de datos

Observando los datos, se intuye que hay ciertos valores de atributos que deben ser modificados y, por tanto, filas que deben ser eliminadas:
* _BloodPressure_ >= 5 dado que en caso contrario, el paciente investigado habría fallecido.
* _Pregnancies_ <= 12 ya que resulta practicamente improbable que para una muestra de 2000 datos haya personas que hayan sufrido mas de 12 embarazos

Estas consideraciones se tienen en cuenta debido a que, al tratarse de una muestra de tamaño pequeño, puede resultar que haya existido un error en la obtención de los datos. 

Por otro lado, se ha transformado la variable numérica _Outcome_ a una variable categórica transformando los '1s' y '0s' a 'diabetes' y 'no_diabetes' respectivamente. Esto nos permite aplicar ciertos algoritmos de aprendizaje automático tales como ID3 que de otra forma no sería posible.

Terminado este proceso, se convierte el fichero .csv a .arff para abordar la solución de la práctica tal y como indica el enunciado. (<u>Fichero_diabetes_v4.csv</u> a <u>Fichero_diabetes_v4.arff</u>).


