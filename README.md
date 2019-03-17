# ou_noise

A collection of function for simulation and parameter estimation of 
Ornstein-Uhlenbeck processes.

## Installtion 

Clone the repository and install the packaged with `pip install .`.

## Usage

The following IPython session demonstrates the package usage.

    from ou_noise import ou
    import numpy
    import matplotlib.pyplot as plt
    %matplotlib

    t = numpy.arange(0, 100, 0.01)
    # simulate a path of the OU process on a given grid t, starting with x_0 = 0.8
    ou.path(0.8, t, 2.0, 0.5, 0.05)                                           
    plt.plot(t,x)

    params = ou.mle(t, x)
    print(params)

    # Output: [2.09360033 0.49863601 0.04992896]

The plot generated by the above script:

![Ornstein-Uhlenbeck process path](ou.png)

## License

ou_noise is released unter GNU GENERAL PUBLIC LICENSE Version 3. 
See LICENSE file for details.

Copyright (c) 2016--2019 Julian Wergieluk