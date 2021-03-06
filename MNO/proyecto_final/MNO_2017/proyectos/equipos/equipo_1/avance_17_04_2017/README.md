![logo](images/logoitam.gif)
# Maestría en Ciencia de Datos
## Proyecto Final
  * Avance 17 de abril de 2017
  * Alumnas:
    - Gabriela Flores Bracamontes | Clave: 160124 |
    - Guillermina Montanari Luján | Clave: 101421 |
    - Paulina Salgado Figueroa    | Clave: 160314 |

## Trabajo Individual

---

### **Paulina**

_*Referencias de Word Embeddings, Word2Vec y Redes Neuronales.*_

  1. Word embedding es un conjunto de modelos que se usan en técnicas de aprendizaje en procesamiento del lenguaje natural, donde las palabras son mapeadas de un texto (corpus) a vectores con entradas reales. La idea es tomar un corpus (texto) de entrada y producir un espacio vectorial de salida de cientos de dimensiones, ya que cada palabra única de corpus tiene un vector asignado. Los vectores son posicionados en el espacio de tal manera que aquellos que comparten espacios comunes están cercanos. Para ello se utilizan redes neuronales, (aprendizaje no supervisado) con una capa oculta. Las neuronas en la capa oculta son todas lineales. La capa de entrada está configurada para tener tantas neuronas como hay palabras en el vocabulario para el entrenamiento. El tamaño de la capa oculta se ajusta a la dimensionalidad de los vectores de palabras resultantes. El tamaño de la capa de salida es el mismo de la capa de entrada.
  
  
    * [Continuos Bag of words (CBOW), From Data to Decisions, Integrated Knowledge Solutions] (https://drive.google.com/open?id=0ByF7NuX9EW1IbE1YczA0aWRpVlU)
    
    * [Exploiting Similarities among Languages for Machine Translation, Tomas Mikolov, Quoc V. Le, Ilya Sutskever, 2013.] (https://drive.google.com/open?id=0ByF7NuX9EW1IN012Y05GMlM3M28)
    
    * [Distributed Representations for Natural Language Processing, Tomas Mikalov-Facebook ML Prague 2016] (https://drive.google.com/open?id=0ByF7NuX9EW1IZE5MN2Z1WDBSUEU)
    
---              

### **Gabriela**: 

_*Revisión de la implementación del algoritmo, posibles formas de optimizarlo.*_

  1. Revisión de la implementación del algoritmo en python para identificar que partes de código se pueden paralelizar y/o optimizar.
      - Se localizó un repositorio en github donde se explica claramente el algoritmo y su implementación en python.
          * [Repositorio de Victor Mijangos](https://github.com/VMijangos/PLN/blob/master/word_embeddings.ipynb)
          
      - Se localizaron artículos acerca de la paralelización de redes neuronales con back-propagation en CUDA, así como la optimización del Word2Vec en Sistemas de Memoria Distribuida, a continuación se listan los artículos:
      
          * [1] Shunlu Zhang, Pavan Gunupudi, Qi-Jun Zhang, ["Parallel back-propagation neural network training technique using CUDA on multiple GPUs"](https://drive.google.com/a/ci.itam.mx/file/d/0B9UK_UtOYJ8IRldNWjBEMk1yV3M/view?usp=sharing), Numerical Electromagnetic and Multiphysics Modeling and Optimization (NEMO) 2015 IEEE MTT-S International Conference on, pp. 1-3, 2015.
          * [2] H. Jang, A. Park, K. Jung, ["Neural Network Implementation Using CUDA and OpenMP"](https://drive.google.com/a/ci.itam.mx/file/d/0ByF7NuX9EW1IMjgyX0tneS0zdUU/view?usp=sharing), Digital Image Computing: Techniques and Applications 0 (2008) 155-161.
          * [3] Lopes N., Ribeiro B. (2009) ["GPU Implementation of the Multiple Back-Propagation Algorithm"](https://drive.google.com/a/ci.itam.mx/file/d/0B9UK_UtOYJ8IZ2pQeXFBTzd2UE0/view?usp=sharing). In: Corchado E., Yin H. (eds) Intelligent Data Engineering and Automated Learning - IDEAL 2009. IDEAL 2009. Lecture Notes in Computer Science, vol 5788. Springer, Berlin, Heidelberg, pp. 449–456, Springer, 2009. 
          * [4] S. Zhang, C. Zhang, Z. You, R. Zheng, and B. Xu, ["Asynchronous Stochastic Gradient Descent for DNN Training"](https://drive.google.com/a/ci.itam.mx/file/d/0B9UK_UtOYJ8IQk81Ul9lZTdXSFU/view?usp=sharing), ICASSP, 2013.
          * [5] Honghoon Jang, Anjin Park, and Keechul Jung (2008), ["Neural Network Implementation using CUDA and OpenMP"](https://drive.google.com/a/ci.itam.mx/file/d/0ByF7NuX9EW1IMjgyX0tneS0zdUU/view?usp=sharing), Proceedings of the 2008 Digital Image Computing: Techniques and Applications, pp 155–161.
          * [6] Thulasiram, R. K., Rahman, R. M., & Thulasiraman, P. (2003, October). [Neural network training algorithms on parallel architectures for finance applications](https://drive.google.com/a/ci.itam.mx/file/d/0B9UK_UtOYJ8IV3B4cE1WbnBXeXc/view?usp=sharing). In Parallel Processing Workshops, 2003. Proceedings. 2003 International Conference on (pp. 236-243). IEEE.
          * [7] Ji, S., Satish, N., Li, S., & Dubey, P. (2016). [Parallelizing word2vec in shared and distributed memory](https://drive.google.com/a/ci.itam.mx/file/d/0ByF7NuX9EW1IU1VaX0puUjM2WFE/view?usp=sharing). arXiv preprint arXiv:1604.04661.
          * [8] Sierra-Canto, X., Madera-Ramirez, F., & Uc-Cetina, V. (2010, December). [Parallel training of a back-propagation neural network using cuda](https://drive.google.com/a/ci.itam.mx/file/d/0B9UK_UtOYJ8ITFE2Uy1JQlRhSjg/view?usp=sharing). In Machine Learning and Applications (ICMLA), 2010 Ninth International Conference on (pp. 307-312). IEEE.

  2. Investigación de las opciones para ejecutar código de Cuda C y Python. Esta semana se revisaron las diversas formas en las que se puede integrar y ejecutar código CUDA C desde python, a continuación se listan:
      - [PyCUDA and PyOpenCL](https://developer.nvidia.com/pycuda).
      - [NumbaPro](https://docs.continuum.io/numbapro/).
      - [Theano](http://deeplearning.net/software/theano/tutorial/using_gpu.html).
      - [gnumpy](http://www.cs.toronto.edu/~tijmen/gnumpyTr.pdf).
      - [CUDA C++ functions in Python via *.so and ctypes](http://bikulov.org/blog/2013/10/01/using-cuda-c-plus-plus-functions-in-python-via-star-dot-so-and-ctypes/)

---

### **Guillermina**
_*Plataforma CUDA*_

  - [Instalacion del driver y toolkit de CUDA](http://docs.nvidia.com/cuda/cuda-installation-guide-linux/#axzz4eMvndrn1)
      
 - Prueba de un programa CUDA en entorno UBUNTU:
 
      * [Hardware para el proyecto](https://drive.google.com/open?id=0ByF7NuX9EW1IZU1XaWdodVJSXzQ)
      * [Tarjeta grafica](https://drive.google.com/open?id=0ByF7NuX9EW1IZnRudEJoWlNWVUk)
      * [Codigos compilados y ejecutados como primera prueba de la instalacion de CUDA](https://drive.google.com/open?id=0ByF7NuX9EW1IS1M3aWJBMnhGRGs)
      * La compilacion de los programas en CUDA se realiza con: ```nvcc <archivo.cu> -o <archivo.out>```
      * La ejecucion se hace con: ```./<archivo.out> ```

  - Versiones instaladas:
      * [gcc](https://drive.google.com/open?id=0ByF7NuX9EW1ISVhPd0JhMmVsWEE)
      * [nvcc](https://drive.google.com/open?id=0ByF7NuX9EW1IYTJETHFQSWpRRlU)
    

## Trabajo en Equipo

### Redefinición del alcance del proyecto.
  1. Una vez revisado todo el material bibliográfico decidimos redefinir el objetivo del proyecto, que se describe a continuación:
      - **Objetivo:** _*Optimizar el algoritmo Word2Vec (CBOW) a través de la paralelización de redes neuronales de retro propagación implementado con PyCuda*_
  2. Se propone una implementación basada en el FrameWork que se explica en el artículo [1] Parallel back-propagation neural network training technique using CUDA on multiple GPUs.
![framework](images/FrameworkNN_B-P.png)
  3. Entre las opciones que se investigaron para la integración de python y CUDA, se elige utilizar **PyCUDA** debido a que nos permite reutilizar código que ya se tiene desarrollado en python para los primeros pasos que son: 
      - Leer un archivo.
      - Dividir el texto en sentencias, cuando se encuentre un punto o un retorno de carro.
      - Convertir a minúsculas.
      - Eliminar signos de puntuación y acentos.
      - Generar el vocabulario de las palabras, utilizando la estructura de diccionarios.
      - La generación de matrices con la librería numpy de python.
      - Los vectores de palabras tendrán una dimensión = 2(x,y), para que sea fácil graficar el resultado de las palabras.