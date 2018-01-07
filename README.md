# libgpio

  A user-space library for controlling the axi GPIO controller core provided by Xilinx in Vivado.
  
  This library contains basic methods for controlling one GPIO or multiple GPIOs in one function call.
  
  The number of GPIO channels available is selected when placing the axi GPIO IP core into your Vivado project.
  Additionally, this library depends on having the GPIO IP core set up as a generic UIO device in the device tree. For examples, check out the device-tree at one of our other projects on github:[Arty-Z7-20](https://github.com/Digilent/Petalinux-Arty-Z7-20), and [Zybo-Z7-20](https://github.com/Digilent/Petalinux-Zybo-Z7-20).
  
  This library utilizes the libuio library located here: [libuio](https://github.com/mitchellorsucci/libuio). To properly initialize the GPIO hardware in your library, you must pass the UIO device number and the UIO map number to GPIO_init().
  
  For an example program that utilizes this library, check out our command-line gpio utility program, which can be found here: [GPIOutil](https://github.com/mitchellorsucci/gpioutil)
