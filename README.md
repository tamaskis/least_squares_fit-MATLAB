# `lsqcurvefit_approx`

Fits linear and polynomial models to data using linear least squares and approximates nonlinear models through linearization.


## Syntax

`[c,r2,eqn] = lsqcurvefit_approx(x,y)`\
`[c,r2,eqn] = lsqcurvefit_approx(x,y,'linear')`\
`[c,r2,eqn] = lsqcurvefit_approx(x,y,'poly',n)`\
`[c,r2,eqn] = lsqcurvefit_approx(x,y,'power')`\
`[c,r2,eqn] = lsqcurvefit_approx(x,y,'exp')`\
`[c,r2,eqn] = lsqcurvefit_approx(x,y,'log')`


## Description

`[c,r2,eqn] = lsqcurvefit_approx(x,y)` returns the model coefficient vector `c = [m,b]` for the linear fit <img src="https://latex.codecogs.com/svg.latex?\inline&space;y=mx+b"/> to a data set defined by the vectors `x` (independent variable) and `y` (dependent variable).

`[c,r2,eqn] = lsqcurvefit_approx(x,y,'linear')` does the exact same thing as the syntax above.

`[c,r2,eqn] = lsqcurvefit_approx(x,y,'poly',n)` returns the model coefficient vector `c = [a0,...,an]` for the <img src="https://latex.codecogs.com/svg.latex?\inline&space;n^{\textrm{th}}"/> degree polynomial fit <img src="https://latex.codecogs.com/svg.latex?\inline&space;y=a_0&space;+a_1&space;x+a_2&space;x^2&space;+\dots&space;+a_n&space;x^n"/> to a data set defined by the vectors `x` (independent variable) and `y` (dependent variable).

`[c,r2,eqn] = lsqcurvefit_approx(x,y,'power')` returns the model coefficient vector `c = [a,b]` for the power fit <img src="https://latex.codecogs.com/svg.latex?\inline&space;y=ax^b"/> to a data set defined by the vectors `x` (independent variable) and `y` (dependent variable).

`[c,r2,eqn] = lsqcurvefit_approx(x,y,'exp')` returns the model coefficient vector `c = [a,b]` for the exponential fit <img src="https://latex.codecogs.com/svg.latex?\inline&space;y=ae^{bx}"/> to a data set defined by the vectors `x` (independent variable) and `y` (dependent variable).

`[c,r2,eqn] = lsqcurvefit_approx(x,y,'log')` returns the model coefficient vector `c = [a,b]` for the logarithmic fit <img src="https://latex.codecogs.com/svg.latex?\inline&space;y=a+b\ln&space;x"/> to a data set defined by the vectors `x` (independent variable) and `y` (dependent variable).

**NOTE:** Additionally, for all the syntaxes, the coefficient of determination (`r2`) and a string (`eqn`) storing the fitted equation (for use in figure text with LaTeX interpreter) are also returned.


## Warning
**Only the linear and polynomial fits are true linear least squares fits**. The nonlinear fits (power, exponential, and logarithmic) are _approximated_ through transforming the model to a linear form and then applying a least squares fit.


## Examples and Additional Documentation

   -  See "EXAMPLES.mlx" or the "Examples" tab on the File Exchange page for examples.
   -  See "Linear Least Squares.pdf" (included with download, also available at https://tamaskis.github.io/documentation/Linear%20Least%20Squares.pdf) for additional documentation.
