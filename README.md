README: Análisis de datos de expresión génica de miR-29

Descripción General

Este repositorio contiene un análisis detallado de datos de expresión génica relacionados con el microRNA miR-29, utilizando técnicas avanzadas de bioinformática y enriquecimiento funcional. El proyecto incluye pasos desde la carga y limpieza de datos hasta la creación de redes de interacción génica, análisis de términos GO, búsqueda automatizada en PubMed y enriquecimiento mediante GSEApy.

Estructura del Proyecto
	1.	Carga y limpieza de datos
	•	Importación de librerías esenciales.
	•	Carga de un archivo de Excel que contiene valores de Ct de qPCR relacionados con miR-29.
	•	Extracción de pruebas, pozos y genes objetivo.
	•	Clasificación de datos en controles y muestras.
	•	Procesamiento de valores indeterminados de Ct y normalización con el gen de referencia GAPDH.
	2.	Análisis de expresión génica
	•	Cálculo de ΔCt, ΔΔCt y Fold Change.
	•	Comparación de controles vs muestras.
	•	Filtrado de genes subexpresados, estables y sobreexpresados.
	3.	Consulta de interacciones génicas
	•	Uso de la API de STRING para obtener redes de interacción génica.
	•	Exportación de los resultados para su visualización en Cytoscape.
	4.	Enriquecimiento funcional
	•	Análisis de términos GO, términos referenciados por PMID y categorías específicas como HPO, KEGG, Reactome y WikiPathways.
	•	Filtrado de términos GO relevantes y generación de gráficos de categorías.
	5.	Búsqueda automatizada en PubMed
	•	Uso de la API de Entrez para buscar artículos relacionados con términos GO.
	•	Clasificación de artículos en tres categorías: miRNA, cáncer y ambas categorías.
	•	Exportación de artículos recuperados a archivos CSV.
	6.	Análisis de enriquecimiento mediante GSEApy
	•	Enriquecimiento funcional utilizando conjuntos de genes personalizados.
	•	Combinación de resultados de GSEApy con información detallada de términos GO.
	7.	Análisis de enriquecimiento de hallmarks del cáncer
	•	Análisis de hallmarks del cáncer utilizando un conjunto de genes de fondo generado a partir de bases de datos públicas.
	•	Visualización de términos enriquecidos significativos mediante gráficos detallados.

Requisitos

Dependencias
	•	Python 3.8 o superior
	•	Librerías requeridas:

pip install pandas numpy matplotlib seaborn requests networkx gseapy biopython tqdm fpdf



Archivos de entrada
	•	data_mir-29_automatización.xlsx: Archivo de Excel con los valores de Ct de qPCR.
	•	gen-sets_GSEA_MSigDB: Carpeta que contiene conjuntos de genes en formato .gmt y archivos JSON con descripciones de términos GO.

Instrucciones de Uso
	1.	Clonar el repositorio

git clone https://github.com/tu_usuario/miR-29-expression-analysis.git
cd miR-29-expression-analysis


	2.	Ejecutar el análisis completo
Abre el archivo miR-29_analysis.ipynb en Jupyter Notebook o ejecuta el script correspondiente en un entorno compatible.
	3.	Explorar los resultados
Los resultados se generan en la carpeta ./resultados e incluyen:
	•	Archivos CSV con términos GO, redes de interacción y bibliografía.
	•	Gráficos en formato PNG y visualizaciones interactivas.

Resultados Esperados
	•	Términos GO enriquecidos: Identificación de términos relevantes asociados a la expresión diferencial de genes.
	•	Redes de interacción génica: Visualización de interacciones relevantes entre genes subexpresados.
	•	Artículos de PubMed: Listado de artículos científicos relacionados con términos GO y clasificados por categoría.
	•	Análisis de hallmarks del cáncer: Términos enriquecidos relevantes según los hallmarks del cáncer.

Archivos Clave

Archivo	Descripción
miR-29_analysis.ipynb	Notebook principal que ejecuta todo el análisis.
gen-sets_GSEA_MSigDB/	Carpeta con archivos .gmt y JSON utilizados en el análisis de enriquecimiento.
./resultados/	Carpeta donde se guardan los resultados generados, incluyendo CSVs y gráficos.
README.md	Documento que describe el repositorio y su uso.

Autores
	•	Sergio Alberto Castelar Fernández – Desarrollo y análisis bioinformático

Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulte el archivo LICENSE para obtener más detalles.

Contribuciones

Las contribuciones son bienvenidas. Si deseas contribuir a este proyecto, por favor sigue estos pasos:
	1.	Haz un fork del repositorio.
	2.	Crea una rama con tus cambios: git checkout -b feature/nueva-funcionalidad.
	3.	Realiza un commit de tus cambios: git commit -m 'Agregada nueva funcionalidad'.
	4.	Sube tus cambios a tu repositorio fork: git push origin feature/nueva-funcionalidad.
	5.	Abre un pull request.

Contacto

Para cualquier duda o consulta relacionada con el proyecto, por favor contacta a:
📧 sergio.castelarf@gmail.com

Agradecimientos

Este trabajo fue posible gracias al apoyo del Laboratorio de Biología Molecular Tumoral, Unidad de Investigación Médica en Enfermedades Oncológicas, y el uso de bases de datos públicas como STRING, GO y KEGG.
