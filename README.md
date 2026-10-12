# telecom-analysis
Analizar el comportamiento de los usuarios de ConnectaTel (empresa de telecomunicaciones LATAM) para identificar segmentos de clientes según edad y nivel de uso, detectar problemas de calidad en los datos, y generar recomendaciones accionables para optimizar la oferta de planes.
📂 Datasets utilizados

| Archivo | Descripción |
|---------|-------------|
| `plans.csv` | Información de los planes disponibles (Básico / Premium) |
| `users_latam.csv` | Datos demográficos de los usuarios registrados en LATAM |
| `usage.csv` | Registros de uso: llamadas y mensajes por usuario |

>  Los datasets son ficticios y fueron proporcionados con fines educativos.

---

##  Etapas del análisis

1. **Carga e inspección inicial** — revisión de columnas, tipos de datos y valores nulos
2. **Detección de calidad de datos** — identificación de sentinels, fechas imposibles y nulos estructurales
3. **Limpieza de datos** — corrección de valores erróneos en `age`, `city` y `reg_date`
4. **Análisis MAR** — validación de nulos en `duration` y `length` según tipo de evento
5. **Construcción de perfil de usuario** — agregación de uso por `user_id` y merge con `users`
6. **Análisis exploratorio (EDA)** — histogramas, boxplots y distribución por plan
7. **Detección de outliers** — método IQR en variables de uso
8. **Segmentación** — clasificación por `grupo_uso` y `grupo_edad`
9. **Conclusiones y recomendaciones** — hallazgos accionables para el negocio

---

##  Cómo ejecutar el notebook

### Opción 1 — Google Colab (recomendado)
1. Abre [Google Colab](https://colab.research.google.com/)
2. Ve a `Archivo → Abrir notebook → GitHub`
3. gh repo clone scordonf07-svg/telecom-analysis
4. Selecciona el archivo `.ipynb` y ejecútalo celda por celda

### Opción 2 — Local con Jupyter
```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/connectatel-user-analysis.git

# 2. Instalar dependencias
pip install pandas numpy matplotlib seaborn

# 3. Abrir Jupyter
jupyter notebook

##  Estructura del repositorio
connectatel-user-analysis/
│
├── datasets/
│ ├── plans.csv
│ ├── users_latam.csv
│ └── usage.csv
│
├── connectatel_analysis.ipynb # Notebook principal
└── README.md

##  Autor

**Sebastian Cordón Flórez**  
Data Analyst
