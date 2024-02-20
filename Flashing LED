from pyA20.gpio import gpio
from pyA20.gpio import port
import time

# Initialize the gpio module
gpio.init()

# Setup the pin PA7 as an output
led_pin = port.PA7
gpio.setcfg(led_pin, gpio.OUTPUT)

try:
    while True:
        # Turn the LED on
        gpio.output(led_pin, 1)
        # Wait for one second
        time.sleep(1)
        # Turn the LED off
        gpio.output(led_pin, 0)
        # Wait for one second
        time.sleep(1)
except KeyboardInterrupt:
    # Cleanup
    gpio.output(led_pin, 0)  # Make sure we turn off the LED
    gpio.cleanup()  # Release resources
