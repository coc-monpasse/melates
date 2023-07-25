# Análisis del Chispazo - Proyecto de Investigación
*[chispazo loteria nacional pagina oficial](https://www.pronosticos.gob.mx/Chispazo/Resultados)
## Descripción

Este es un proyecto de investigación y análisis del juego de lotería mexicana llamado "El Chispazo". El objetivo del proyecto es analizar los resultados históricos del juego y encontrar patrones y tendencias que puedan ayudar a entender las probabilidades de ganar.

## Instalación

1. Clonar el repositorio desde GitHub:

```
git clone https://github.com/tuusuario/chispazo-analysis.git
```

2. Instalar las dependencias requeridas:

```
pip install pandas numpy matplotlib requests
```

3. Descargar los datos históricos del Chispazo:

los datos historicos ya fueron descargados, de cualquier forma puedes descargarlos manualmente en la pagina oficial de la lotenia nacional

## Uso

El proyecto contiene varias clases y funciones para realizar el análisis del Chispazo. A continuación, se describen las principales funcionalidades:

### `Chispazo`

La clase `Chispazo` contiene todas las funciones y métodos para el análisis del juego.

#### Generar combinaciones aleatorias

```python
ch = Chispazo()
combinacion = ch.generate_random_combination()
print(combinacion)
```

#### Calcular probabilidad de una combinación

```python
ch = Chispazo()
probabilidad = ch.calculate_probability_v3(pd.Series(combinacion, index=['R1', 'R2', 'R3', 'R4', 'R5']))
print(probabilidad)
```

#### Generar combinaciones probables

```python
ch = Chispazo()
combinaciones_probables = ch.generate_combinations(n=10)
for i, c in enumerate(combinaciones_probables):
    print(f'{i+1}. {c[0]} - probabilidad: {c[1]*100:.2f}%')
```

#### Guardar combinaciones probables en archivo CSV

```python
ch = Chispazo()
ch.guardar_combinaciones_probables(file_name='combinaciones_probables.csv', threshold=0.01, iterations=100000)
```

## Contribuciones

Siéntase libre de realizar contribuciones al proyecto. Puedes enviar un pull request con tus mejoras, correcciones o nuevas funcionalidades.

## Licencia

Este proyecto está bajo la licencia MIT. Puedes ver más detalles en el archivo LICENSE.

## Agradecimientos

Agradecemos a Pronósticos para la Asistencia Pública por proporcionar los datos históricos del Chispazo.

## Contacto

Si tienes alguna pregunta o sugerencia puedes concactarme via linkedin [coc linkedin](https://www.linkedin.com/in/acontreras-mp/)

## Descargo de responsabilidad

Este proyecto tiene fines de investigación y entretenimiento. No garantizamos que las estrategias o análisis aquí presentados mejoren las probabilidades de ganar en el Chispazo. Jugar a la lotería siempre conlleva un riesgo y se debe hacer de manera responsable.
