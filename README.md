# Flashing-LED-Window-Lights-with-Raspberry-Pi
Example code for creating flashing LED window lights with Raspberry Pi.
import RPi.GPIO as GPIO
import time

led_pin = 17

GPIO.setmode(GPIO.BCM)
GPIO.setup(led_pin, GPIO.OUT)

try:
    while True:
        GPIO.output(led_pin, GPIO.HIGH)
        time.sleep(1)
        GPIO.output(led_pin, GPIO.LOW)
        time.sleep(1)
except KeyboardInterrupt:
    GPIO.cleanup()
