# Ejercicio-5-pandas-
pd.DataFrame, los cuales tienes datos (producto, precio), uso de .apply(), Ejemplo para pasar de minusculas a mayusculas.

import pandas as pd
data = {"Producto": ["Manzana", "Naranjas", "Platanos", "Uvas", "Peras"], 
         "Precio": [100,80,60,120,90]
}

df = pd.DataFrame(data)
print (df)

def descuento (x):
    return x * 0.85
df["Precio_descuento"] = df ["Precio"].apply(descuento)
print (df)

#Pasar a mayuscular 
cadena = "hola"
print (cadena.upper())

df ["Producto"] = df ["Producto"].apply(lambda x: x.upper())
print (df)
