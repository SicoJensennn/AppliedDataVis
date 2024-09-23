# Applied Data Visualization

## Lec.01

Tasks: finish 5 critiques.

Office hour: 4:30 - 5:30 Wednesday, WEB 3887.

https://www.dataviscourse.net/2023-applied/syllabus/

Use slack for communication, and canvas to submit homework.

<font color =#e07a5f>2 Exams: Wed after fall break and a final one. </font>

Some Markdown skills:

+ changing colors: <font color></font>

+ highlight: <mark></mark>




## Lec.02

Our perception is based on our prior.

### Color

Color != wavelength, but rather a combination of wavelength and energy.

1. Dimensions of  Color
   + Hue: wavelength
   + Saturation: the purity of a color
   + Value

2. Gamut

  Set of all colors that can be produced by a device. 

3. What is a colormap
    specifies a mapping between color and values.

4. Gestalt effect

   Gestalt psychology focuses on how people perceive objects, shapes, and forms as whole entities rather than separate parts.

- [x] activity 1 homework.



## Lecture 04

1. `iloc`

   ```python
   bands_founded.iloc[[0,3]]
   ```

2. `dropna`

   Can be used in the homework to filter out the nan data.

3. map function

   can be passed in a dictionary.

   ```python	
   new_sorted_numbers.map({1965:1945, 2012:1999, 1968:"What"})
   ```

4. `axes`

   While a series has only one axis, a dataframe has two, one for the rows (the index or '0' axis), one for the columns (the column or '1' axis). 

5. `corr`

   We can look at whether the numerical columns in our data frame are correlated using the [`corr()`](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.corr.html) method. By default, this calculates a Pearson correlation between the column, excluding NaN values. Not surprisingly, we see a rather strong correlation (0.81) between certified and claimed sales. 

   ![image-20240828151756990](C:\Users\u1474799\AppData\Roaming\Typora\typora-user-images\image-20240828151756990.png)

6. Transpose a dataframe

   ```python
   hit_albums.T
   ```

7. `set_index`

   We can set a column to be the index.

   ```python
   sf.set_index("column name")
   ```

8. The second argument in the `loc` array can be used to access columns 

### Grouping

1. `ffill`

   But first, let's take care of some NAN values by running [`ffill`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.ffill.html) on it. `ffill` fills in the certified sales based on the claimed sales if necessary. 

2. `grouped.sum()`

   `count`, `mean` work.

3. `agg`

    A very generic solution is the `agg()` function, which we can pass a function to do things with the data:

   ```python
   # here we pass the sum function, which calcualtes the sum of a list, to the group
   grouped.agg('sum').head()
   ```

### plot

1. format strings

   They work like this: ```fmt = '[marker][line][color]'```
   For example, a marker could be a square `s`, a line can be dotted `:` and the color can be green `g`, so that would be the format string `s:g`.

   

### Data semantic
semantic: real world meaning
data types: link, item, attribute, position, grids

+ Item & attribute

  attribute: observed property of items
  
+ links

+ positions

  spatial data → location in 2D or 3D
  
+ Grids
  sampling strategy for continuous data, like weather stations in the U.S.
  
### Dataset type
+ table
+ network/graph
  + node link graph
  + matrix
  + treemap
+ collections
  how we group items.

  + sets
  + lists
  + clusters
+ Fields
+ Geometry
+ nominal, ordinal, interval, or ratio 





## Scales

1. Start from 0?
2. Log scale?
3. normalize
4. slopegraph
5. 
