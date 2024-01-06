
#separar_texto_en_columnas

1. Función para tomar valores antes de separador, en este caso "," en python:

* df_filtered['Category']: Esta parte del código hace referencia a la columna 'Category' del DataFrame 'df_filtered'. Estás accediendo a todos los datos que se encuentran en esa columna específica.
* .apply(lambda x: ...): .apply() es un método de pandas que se utiliza para aplicar una función a lo largo de un eje del DataFrame. En este caso, estás aplicando una función a cada elemento en la columna 'Category'. La función que estás aplicando está definida por la expresión lambda dentro de los paréntesis. lambda x define una función anónima con x siendo el parámetro que representa cada valor individual en la columna 'Category'.
* x.split(','): split(',') es un método de cadena que divide una cadena en una lista donde cada elemento es una subdivisión de la cadena original separada por comas. Si tienes una cadena como "drama, otra, otra", split(',') la convertirá en la lista ['drama', ' otra', ' otra'].
* [0]: Después de dividir la cadena en una lista, [0] selecciona el primer elemento de esa lista. Siguiendo el ejemplo anterior, si tu lista es ['drama', ' otra', ' otra'], el primer elemento [0] será 'drama'.
* .strip(): strip() es un método de cadena que elimina los espacios en blanco al principio y al final de una cadena. Si el primer elemento seleccionado tiene espacios adicionales (por ejemplo, ' drama '), strip() lo limpiará a 'drama'.
* df_filtered['Category'] = ...: Finalmente, después de aplicar todas estas operaciones a cada valor en la columna 'Category', reasignas los resultados limpios y transformados de nuevo a la columna original 'Category' en tu DataFrame.