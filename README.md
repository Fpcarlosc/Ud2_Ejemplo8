# Ud2_Ejemplo8
_Ejemplo 8 de la Unidad 2._

Vemos un ejemplo de cómo posicionar elementos relativos a otros en _RelativeLayout_ haciendo uso de los atributos _layout_toRightOf_ y _layout_below_. 

Sólo hemos de fijarnos en el fichero _activity_main.xml_:

```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imagen"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:src="@drawable/grand_canyon"
        android:scaleType="centerCrop" />

    <TextView
        android:id="@+id/gran_cañon"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="El Gran Cañón"
        android:textAppearance="?android:textAppearanceLarge"
        android:layout_toRightOf="@+id/imagen"/>

    <TextView
        android:id="@+id/arizona"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Arizona"
        android:textAppearance="?android:textAppearanceMedium"
        android:layout_toRightOf="@+id/imagen"
        android:layout_below="@id/gran_cañon"/>

    <TextView
        android:id="@+id/eeuu"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="EEUU"
        android:textAppearance="?android:textAppearanceSmall"
        android:layout_toRightOf="@+id/imagen"
        android:layout_below="@id/arizona"/>

</RelativeLayout>
```
Donde podemos ver que el nombre de la imagen es _grand_canyon_ y se puede encontrar en el directorio _res/drawable_. Notad cómo accedemos al recurso _drawable_ usando el símbolo @.

En este caso no se ha insertado los textos de los _TextView_ en el fichero _strings.xml_ para facilitar su localización en el código.

_Imagen de Pixabay.com (Licencia CC0)_
