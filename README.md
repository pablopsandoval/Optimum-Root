# 🌱 Optimización Estocástica para Reforestación Sostenible

Este proyecto fue desarrollado como parte del curso **MA2004B - Optimización Estocástica** en el Tecnológico de Monterrey (semestre Agosto-Diciembre 2024). El objetivo fue diseñar un modelo matemático y computacional que optimice la reforestación en una hectárea, considerando incertidumbre en la disponibilidad y competencia entre especies vegetales.

## 📌 Objetivo del proyecto

Diseñar una distribución de plantación óptima para minimizar la competencia entre especies y evitar el monocultivo, utilizando técnicas de:

- Modelado matemático
- Simulación de Monte Carlo
- Algoritmos genéticos

## 🔍 Contexto

La reforestación enfrenta retos como:

- Compra excesiva de especies
- Especies preexistentes no removidas
- Competencia entre plantas que disminuye su supervivencia

Este proyecto responde a estos desafíos con una solución basada en datos y optimización estocástica.

## 🧠 Modelo matemático

### Conjuntos
- `E`: especies consideradas (10 especies nativas)
- `P`: posiciones posibles en el terreno (658 puntos en una hectárea)

### Parámetros
- `Cᵢₖ`: matriz de competencia entre especies (1–100)
- `aᵢ`: disponibilidad por especie
- `dⱼⱼ'`: distancia entre posiciones (4m, 6.4m o no adyacente)

### Variables de decisión
- `xᵢⱼ`: especie *i* plantada en posición *j*
- `yₖⱼ'`: especie *k* plantada en posición adyacente *j'*

### Restricciones
- No exceder disponibilidad de cada especie
- Evitar monocultivos en posiciones adyacentes

### Función objetivo
Minimizar la competencia total ponderada entre todas las plantas en el terreno.

## 🧬 Algoritmo genético

- Cromosoma: vector numérico de 658 posiciones
- Inicialización: mezcla de plantas fijas y asignaciones aleatorias
- Selección: torneo
- Mutación: intercambio pseudoaleatorio
- Paro: 100 generaciones
- Población: 5 individuos

## 🎲 Simulación de Monte Carlo

Se simularon múltiples distribuciones de especies para:

- Calcular probabilidad de ocurrencia por especie
- Determinar transiciones óptimas entre especies
- Evaluar la robustez del modelo ante incertidumbre
  ![image](https://github.com/user-attachments/assets/40be71cf-8d31-4330-a090-5f13cc2f574f)


## 📈 Resultados clave

- Plantas totales: **658**
- Competencia promedio reducida a **66.17%** respecto a un diseño aleatorio
- Tiempo de ejecución: **754 minutos**
- Mejora significativa en la supervivencia esperada por especie

## 💻 Herramientas utilizadas

- Lenguaje: **Python**
- Editor: **Visual Studio Code**
- Simulación: **algoritmo genético + Monte Carlo**
- Hardware: **MacBook Pro M2 Max, 96GB RAM**

## 🧪 Equipo de trabajo

- Pablo Pérez Sandoval  
- Juan Pablo Guzmán Segura  
- Valeria Mariane Cárdenas Rodríguez  
- Rodrigo Leal Torres  
- Máximo Caballero Vargas  

## 🔗 Acceso al código

> El código está disponible [aquí](https://drive.google.com/drive/folders/16iJzZIDdOybX2jc-ODEl0IS5Ya5nt0Ra?usp=sharing)

## 📌 Conclusión

Este proyecto demuestra cómo las herramientas de optimización estocástica pueden aplicarse para resolver problemas reales de sostenibilidad, maximizando el uso eficiente del terreno y reduciendo los riesgos ecológicos asociados al monocultivo.

