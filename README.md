# Demanda eléctrica y temperatura en Argentina

Análisis exploratorio de datos reales sobre cómo influye la temperatura en la demanda de electricidad en Argentina.
Proyecto basado en el trabajo práctico grupal de **Laboratorio de Métodos Cuantitativos Aplicados a la Gestión**
(Facultad de Ciencias Económicas, UBA · 2do Cuatrimestre 2026).

---

## Integrantes

| Integrante | Usuario de GitHub |
|---|---|
| Catalina Fiorini | [@catafiorini](https://github.com/catafiorini) |
| Rafael Seri | [@RafaelSeri](https://github.com/RafaelSeri) |
| Federico Mingorance | [@fedem2004](https://github.com/fedem2004) |
| Micaela Berzoni | [@micaelaberz](https://github.com/micaelaberz) |
| Genaro D'Angelo | [@GenaroDangelo](https://github.com/GenaroDangelo) |

Repositorio original del grupo: [RafaelSeri/TP_LABO_MET](https://github.com/RafaelSeri/TP_LABO_MET)

---

## Tema y pregunta de investigación

**Tema:** demanda de electricidad en Argentina.

**Pregunta principal:** ¿Cuánto influye la temperatura en la demanda eléctrica de Argentina y en qué épocas del año es más crítica?

**Motivación:** la demanda eléctrica cambia con el clima. Saber cuándo y cuánto sube ayuda a planificar la generación,
anticipar los picos de consumo y prevenir cortes en los momentos en que el sistema trabaja al límite.

**Fuente de los datos:** CAMMESA — Demanda de Electricidad (Cuadro 1.28), publicado por el Ministerio de Economía de la Nación
en *Economía en números*: https://www.argentina.gob.ar/economia/datos/nivel-de-actividad

**Cobertura:** serie anual 2005–2025, trimestral y mensual hasta agosto de 2026.

**Variables principales:** demanda total, demanda residencial, comercio e industria, grandes usuarios,
temperatura promedio, potencia máxima y demanda por distribuidora.

---

## Principales hallazgos

- **La relación no es lineal.** La demanda es mínima con temperaturas templadas (entre 15 y 21 °C) y sube hacia ambos extremos:
  ronda el 107 % del promedio anual tanto en los meses más fríos como en los más cálidos.
- **Invierno y verano son las épocas más críticas** para el sistema eléctrico.
- **El segmento residencial explica la mayor parte de este comportamiento**, con picos que superan el 120 % del promedio en el frío.
- **Comercio e Industria reacciona solo al calor**, mientras que **Grandes Usuarios** mantiene una demanda prácticamente
  independiente de la temperatura.


### Limitaciones

- Los datos son mensuales: no capturan olas de calor o de frío de pocos días, que concentran los picos de demanda.
- La temperatura es un promedio nacional y no refleja las diferencias entre regiones.
- Los rangos extremos de temperatura reúnen pocos meses.
- La demanda también depende de factores no considerados, como la actividad económica, las tarifas o el crecimiento de la población.

### Posibles extensiones

- Usar datos diarios u horarios para estudiar los picos de corta duración.
- Incorporar información regional.
- Estimar un modelo que cuantifique el efecto de la temperatura controlando por otros factores económicos.

---

## Estructura del repositorio

```
├── DF/                          # Datasets
│   ├── actividad_ied.xlsx       # Base cruda (hoja 1.28 Electricidad), la lee el notebook
│   └── base_limpia.xlsx         # Base depurada, la genera el notebook
├── notebooks/
│   └── Tp_labo.ipynb            # Notebook de Google Colab: carga, limpieza, análisis y gráficos
├── graficos/                    # Gráficos 
├── Informe/
│   ├── informe.tex              # Código LaTeX del informe
│   └── Tp_LabMetCuant.pdf       # Informe académico compilado
├── PPT/
│   └── Presentacion_Oral.html   # Presentación de la defensa
├── GuiaTP/                      # Enunciado del TP
└── README.md
```

---

**Herramientas:** Python (pandas, NumPy, Matplotlib, seaborn), Google Colab, LaTeX/Overleaf.

---

## Uso de inteligencia artificial

Se usaron herramientas de IA como asistentes en el código, la redacción y la interpretación de resultados.
Todas las salidas fueron revisadas y contrastadas con los datos; el criterio analítico y las conclusiones son del grupo.
