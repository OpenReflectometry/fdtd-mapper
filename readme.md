FDTD Mapper
-----------


Creates the 2D map inputs for the FDTD simulator



# Functions



```python
def mapper_mesh( size_x, size_y, dx, dy):
    """
    Creates an empty meshgrid of xx, yy with the correct discretization


    Parameters
    ----------
    size_x, size_y : float
        Size of the simulation map in meters
    dx, dy : float
        Discretization step of the map
        Should be around minimum wavelength/20
    
    Returns
    -------
    xx, yy : 2d array
        Meshgrid of the xx and yy points
    """
```



```python
def mapper_slabify(x, z, newy, axis=0):
    """
    Slabifies a 1D vector into a 2D vector repeated along the y axis

    Parameters
    ----------
    x : array
        x value of the input vector to repeat
    z : array
        z value of the input vector to repeat
    newy : array
        Array of the new axis to input
    
    Returns
    -------
    xx, yy, zz : 2d arrays
        Repeated values 
    
    """

```



```python
def save_output_ascii(m, filename):
    """
    Saves the 2D matrix into the output file

    Parameters
    ----------
    m : array 2d
        Matrix to be stored
    
    """
    with open(filename, 'w') as f:

        for line in m:
            l = ''
            for el in line:
                l += '%e'%el
                l += ' '
            l += '\n'
            f.write(l)
            print(l)

```