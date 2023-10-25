# Other Machine Functions and Loops

## Infinite Loops
An infinite loop in Python is like telling your computer to do something over and over forever, without stopping unless you, the user, intervene.

Imagine you're playing a video game, and your character keeps walking in a single direction endlessly without any end. It won't stop unless you press a button to make it stop.

In Python, you can create a loop that works the same way. It will keep doing something repeatedly until you tell it to stop.

However, you need to be careful with infinite loops because if you forget to tell it to stop, your program might run forever, which can be a problem. So, it's important to have a plan to stop the loop when you want it to end.

An example of an infinite loop would be something like:
```python
import time
while True:
    print("It's still going")
    time.sleep(3)
```

## Other Machine package functions 
The `machine` package in MicroPython provides various functions for controlling hardware components on microcontrollers like the Raspberry Pi Pico. To control an LED on the Pico, you typically use the `machine.Pin` function as you did in your provided code, but you can also use additional functions for more advanced control. Here are some of the common functions in the `machine` package that you can use to control an LED on the Raspberry Pi Pico:

1. **`pin.on()`**: Turns the specified pin (e.g., LED) on.

2. **`pin.off()`**: Turns the specified pin off.

3. **`pin.value(value)`**: Sets the pin to the specified value (1 for on, 0 for off).

4. **`pin.toggle()`**: Toggles the state of the pin, turning it on if it's off and off if it's on.

5. **`pin.irq(handler, trigger)`**: Configures an interrupt handler function for the pin. This allows you to execute a function when the pin changes state.

6. **`machine.freq([value])`**: Gets or sets the CPU frequency. Adjusting the frequency can impact how fast your code runs.

7. **`machine.sleep([time])`**: Puts the microcontroller to sleep for a specified time, conserving power. This can be used for low-power applications.

8. **`machine.Timer(freq, mode)`**: Allows you to set up hardware timers for precise timing operations.

These are just some of the functions provided by the `machine` package in MicroPython for controlling hardware components, including LEDs, on the Raspberry Pi Pico. Depending on your project's requirements, you can choose the appropriate functions to control the LED's behavior.