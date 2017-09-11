# Informe Bioinformática IV
Luciano Frez

**¿Qué cosas ofrece este portal?** 
 
A sido diseñado para proporcionar una plataforma de alto rendimiento que transcribe de forma transparente los programas relevantes para el análisis filogenético. La filosofía primaria de Phylogeny.fr es ayudar a los biólogos sin experiencia en la filogenia en el análisis de sus datos.

 La plataforma Phylogeny.fr ofrece una línea de filogenia que se puede ejecutar a través de tres modos principales:
El **"One Click" mode:** se dirige a los usuarios que no desean tratar con la selección de programas y parámetros. ya está configurada para ejecutar y conectar programas reconocidos por su precisión y velocidad (MUSCLE para alineación múltiple y PhyML para filogenia) para reconstruir un árbol filogenético a partir de un conjunto de secuencias.
En el **Advanced mode:**, el servidor Phylogeny.fr propone la sucesión de los mismos programas, pero los usuarios pueden elegir los pasos a realizar (alineación de secuencias múltiples, reconstrucción filogenética, dibujo de árboles) y las opciones de cada programa.
El **"A la carte" mode:** ofrece la posibilidad de correr y probar más programas de alineación y filogenia, como MUSCLE, ClustalW, T-Coffee, PhyML, BioNJ, TNT, etc)

**¿Para qué tipo de usuario está diseñado?**

La plataforma está diseñada para usuarios que estén interesados en realizar un árbol filogenético, pero sin tener experiencia en este proceso. Ayuda a manejar grandes cantidades de información y así llegar a un producto de manera más rápida y efectiva a través de los diferentes programas que utiliza para generar estos procesos.(MUSCLE para alineación múltiple y PhyML para filogenia, ClustalW, T-Coffee, PhyML, BioNJ, TNT, etc) 

*Menciona 5 tipos de análsis que se pueden realizar en el portal de acuerdo a la documentación*

**"One Click" mode:** Este es un modo "predeterminado" que propone una fuente de información ya configurada para ejecutar y conectar programas reconocidos por su precisión y velocidad (MUSCLE para alineación múltiple, opcionalmente Gblocks para alineación curation, PhyML para phylogeny y finalmente TreeDyn para dibujo de árboles) para reconstruir un árbol filogenético de un conjunto de secuencias. 

**Advanced mode:** La fuente de información es la misma que en el modo "One Click", pero es lo suficientemente flexible como para permitir a los usuarios seleccionar los pasos a realizar. De esta manera, los datos de entrada pueden ser un conjunto de secuencias no alineadas en formato FASTA, una alineación de múltiples secuencias en formato FASTA, PHYLIP o Clustal, o un árbol en formato NEWICK.
Los usuarios disponen de opciones para establecer los parámetros de los diferentes programas de la tubería.

**"A la carte" mode:** El servidor ofrece la posibilidad de ejecutar otros programas de alineación y filogenia que los preseleccionados en los modos "One Click" y "Advanced mode":
-Una alineación de secuencias múltiples utilizando MUSCLE, T-Coffee, 3D-Coffee, ProbCons o ClustalW según la preferencia del usuario
-Una reconstrucción filogenética utilizando PhyML, TNT, MrBayes, BioNJ o Vecino y
-La generación de una imagen de calidad de publicación del árbol filogenético resultante usando TreeDyn, Drawgram o Drawtree

**Blast: Explore your sequence neighbors:** El sistema facilita la selección de secuencias homólogas, basadas en una representación filogenética "rápida y sucia" usando los resultados de BLAST y un estimador de la longitud de alineación múltiple final.


**¿A qué se refiere el paso de *Alignment curation* y para qué sirve?**

''Alignment curation'' se refiere a las secuencias sin ''errores''. Es un proceso por el cual la plataforma elimina posibles ''errores'' dentro de la secuencia, en el caso de ''Gblocks'' el cual elimina posiciones mal alineadas y regiones divergentes y ''Remove position with gaps'', esta elimina literalmente las posiciones en las que haya algún gap, haciendo el alineamiento mucho más atildado.

**¿Cuál es la diferencia entre BioNJ y Neighbor?** *(Pista: revisa la documentación)*
 
Las diferencias entre BIoNJ y Neighbor es qué: BIoNJ es más adecuado para estimar distancias a partir de secuencias de ADN o proteínas. Este tiene mejor precisión topológica que NJ(Neighbor-Joining) en todas las condiciones evolutivas; esto se hace notorio cuando las tasas de sustitución son altas y varían entre los linajes. Sin embargo, los árboles BIONJ y NJ a menudo son cercanos o idénticos, especialmente cuando el número de taxones es bajo. BIONJ mantiene la velocidad de NJ y puede aplicarse a conjuntos de datos muy grandes (> 1000 taxones). BIONJ también se puede ejecutar en varias matrices para construir árboles bootstrap, pero las distancias deben ser corregidas.(1)

*Corre de nuevo las filogenias pero esta vez sin *Alignment curation*.* **¿Cuál es el efecto en las filogenias?**

No hubo cambios en los árboles filogenéticos al eliminar el ''Alignment curation''. Si se hubiesen usado todas las demás secuencias, tal vez se pudo evidenciar algún tipo de diferencias, ya que, el ''Alignment curation'' es un prcedimiento el cual permite eliminar los ''errores'' presentes en las secuencias, y al eliminar este método correctivo, los alineamientos no puede ser correjidos generando errores a la hora de generar el árbol(algunas especies pueden aparecer más cerca de lo que realmente son u otras pueden separarse por mucha mayor distancia)

*Describe las diferencias entre las filogenias que has estimado: cantidad de grupos monofiléticos, relaciones que potencialmente cambiaron, etc.*

![imagen](https://github.com/MrPiggie/Informe-Bioinform-tica-IV/blob/master/ClustalW,Remove%20positions%20with%20gap,%20TNT,%20y%20TreeDyn%20the%20real.png?raw=true)
**Imagen I:** ClustalW,Remove positions with gap, TNT, y TreeDyn.

![imagen](https://github.com/MrPiggie/Informe-Bioinform-tica-IV/blob/master/ClustalW,%20TNT,%20y%20TreeDyn.png?raw=true)
**Imagen II:** ClustalW, TNT, y TreeDyn

![imagen](https://github.com/MrPiggie/Informe-Bioinform-tica-IV/blob/master/ProbCons,%20GBlocks,%20MrBayes,%20y%20TreeDyn%20the%20real.png?raw=true)
**Imagen III:** ProbCons, GBlocks, MrBayes, y TreeDyn.

![imagen](https://github.com/MrPiggie/Informe-Bioinform-tica-IV/blob/master/ProbCons,%20MrBayes,%20y%20TreeDyn.png?raw=true)
**Imagen IV:** ProbCons, MrBayes, y TreeDyn.

# **Bibliografía:**

(1) http://www.atgc-montpellier.fr/bionj/ 11/09/17 19:25
