# Grocery Dataset
Se esta utilizando el repositorio mostrado en el articulo de vision de imagenes para tiendas, este repositorio es libre y se ha utilizado en diferentes proyectos abieros.

este DataSet de imagenes comupuesto por:
* imagenes recolactadas de 40 tiendas con 4 camaras,
* mas de 10 categorias de productos
* creado en Primavera del 2014  - Idea Teknoloji, Istanbul, Turkey.
la informacion se encuentra en los siguientes links:


## Download links
Here are [part1](https://github.com/gulvarol/grocerydataset/releases/download/1.0/GroceryDataset_part1.tar.gz) and [part2](https://github.com/gulvarol/grocerydataset/releases/download/1.0/GroceryDataset_part2.tar.gz) for downloading the image files. The total disk space is around 3GB. You can equally find these links under the releases of this repository. 

## Organization of the folders

### ShelfImages
este archivo contiene 354 imagenes de articulos

The naming is as follows:
```
			"C<c>_P<p>_N<n>_S<s>_<i>.JPG"
			where
				<c> := camera id (1: iPhone5S, 2: iPhone4, 3: Sony Cybershot, 4: Nikon Coolpix)
				<p> := planogram id
				<n> := the rank of the top shelf on the image according to the planogram
				<s> := number of shelves on the image
				<i> := copy number
```
	
### ProductImages
Esta carpeta contiene imágenes de 10 categorías de productos diferentes, numeradas del 1 al 10. Cada categoría tiene un directorio independiente

The naming is as follows:
```
		"B<b>_N<N>.JPG"
			where
				<b> := brand id
				<n> := copy number
```

		
### BrandImages

Esta carpeta contiene las versiones recortadas del directorio ProductImages. Las imágenes se recortan para que solo se conserve el logotipo de la marca.


### ProductImagesFromShelves

Esta carpeta contiene imágenes de productos recortadas de imágenes de estantería. Se dividen en 10 categorías de productos, más una categoría negativa donde se agrupan los productos que no pertenecen a ninguna de las 10 clases.

The naming is as follows:
```
			"<shelf image name>_<x>_<y>_<w>_<h>.png"
			where
			<shelf image name>   := the source image where the image is cropped from
			<x>                  := x-coordinate of the image's top-left corner on the source image
			<y>                  := y-coordinate of the image's top-left corner on the source image
			<w>                  := width of the image on the source image
			<h>                  := height of the image on the source image
```

### BrandImagesFromShelves
Esta carpeta contiene las versiones recortadas del directorio ProductImagesFromShelves. Las imágenes se recortan para que solo se conserve el logotipo de la marca.

*******************************
## Annotation files

### annotation.txt
Este archivo resume la información de anotación de las imágenes de los estantes en un solo archivo de texto. Cada fila explica una imagen de los estantes.

The format of one line is as follows:

```
			<shelf image name> <n> <x_1> <y_1> <w_1> <h_1> <b_1> <x_2> <y_2> <w_2> <h_2> <b_2> ... <x_n> <y_n> <w_n> <h_n> <b_n>
			where
			<shelf image name>   := shelf image name
			<n>                  := number of product on the shelf image
			<x_i>                := x-coordinate of the i'th product image
			<y_i>                := y-coordinate of the i'th product image
			<w_i>                := width of the i'th product image
			<h_i>                := height of the i'th product image
			<b_i>                := brand of the i'th product image
```

### subset.txt
Este archivo enumera los nombres de los archivos de imagen utilizados para el entrenamiento y las pruebas. Es un subconjunto del contenido de BrandImages y BrandImagesFromShelves.

## Citation
If you use this dataset, please cite the following:
> @article{varol16a,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TITLE = {{Toward Retail Product Recognition on Grocery Shelves}},  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;AUTHOR = {Varol, G{\"u}l and Kuzu, Ridvan S.},  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;JOURNAL =  {ICIVC},  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;YEAR = {2014}  
}

## Acknowledgements
The dataset is collected as part of a TUBITAK funded project carried out by Idea Teknoloji.



