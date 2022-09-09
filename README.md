# Array Tridimensional

**Se declara y se define**
```c++
int arreglo[caras][filas][columnas] = { {{1, 2, 3}, {4, 5, 6}},
                                        {{7, 8, 9}, {10, 11, 12}}
```

**Se selecciona**
```c++
int matriz = arreglo[caras][filas][columnas];
```

# Para Recorrer una matriz
```c++
//Se crea el arreglo y se define
int matriz[2][2][3] = { {{1, 2, 3}, {4, 5, 6}},
                        {{7, 8, 9}, {10, 11, 12}}
};
void setup()
{
  Serial.begin(9600); //Se inicia el puerto serial
}

void loop()
{
  int caras = 2; //Cantidad de caras
  int filas = 2; //Cantidad de filas
  int columnas = 3; //Cantidad de columnas

  int i, j, k; //Variables a recorrer

  //Para recorrer un areglo tridimensional
  //Se utiliza tres bucles for
  for (i = 0; i < caras; i++)
  {
    for (j = 0; j < filas; j++)
    {
      for (k = 0; k < 3; k++)
      {
        Serial.println(matriz[i][j][k]); //Se imprime el arreglo
      }
    }
  }
  delay(2000); //Retardo de 2 segundos
}
```
