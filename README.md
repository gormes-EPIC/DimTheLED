# Dim the LED


https://github.com/user-attachments/assets/74ec4b4b-1feb-487e-8267-b091f2e91435



## Objective

1. Create a program to dim an LED with a rotary encoder
## Materials

1. 2 M to M jumper wires
2. 4 M to F jumper wires
3. 1 5mm LED
4. 1 65 Ω (Ohm) resistor
5. 5 pin rotary encoder

## Part 1: Light the LED Again!

1. Create a new script `dimmable.py` and wire your LED like in the last lab. 
2. Rather than setting up our LED like the last time, we are going to use a `PWMLED` or a pulse-width-modulation LED. 
3. Use the [code provided here](https://gpiozero.readthedocs.io/en/latest/recipes.html#led-with-variable-brightness) to set up your `PWMLED`. We will take advantage of the `PWMLED`'s variable `value` to achieve different brightness's. Try a few different values of `value` between 0 and 1 to set your LED.

- [ ] There is nothing to submit for this part.
## Part 2: Adding the Rotary Encoder

<img width="756" height="491" alt="re" src="https://github.com/user-attachments/assets/aff1df01-db8c-4e22-9190-639572d1da4b" />

1. Wire your 5 pin rotary encoder with the diagram above. See [this website](https://thepihut.com/blogs/raspberry-pi-tutorials/how-to-use-a-rotary-encoder-with-the-raspberry-pi) for more information on wiring and how they work.
2. Next we are going to write the code. The position on the rotary encoder should start at 0 then slowly increase to 180. You need to translate that value into a value between 0-1 to set the led based on the rotary encoder.  See the starter code below. See [this website](https://gpiozero.readthedocs.io/en/latest/recipes.html#rotary-encoder) for more information. *Note: this example is more complex than what I am asking you to do.* 

```python
from gpiozero import RotaryEncoder

rotor = RotaryEncoder(16, 20, wrap=True, max_steps=180) # DT goes to 16, CLK goes to 20

while True:
	print(rotor.steps) # the value of rotor.steps will change as you rotate the device

```

- [ ] Upload a video of your functional program and `dimable.py`

## Deliverables
- Uploaded a video and your final program to GitHub
- Answers to the following questions
    - What debugging strategies did you use to identify and fix these problems?
    - How could you systematically test whether the issue was in hardware or code?
    - Write the equation that converts an encoder value x (from 0–180) into a brightness value b (from 0–1)
## Rubric

- 6 points - All required items are present.  
- 5 points - Task was completed, but supplementary materials are weak or missing.    
        - Code is complete, but poorly communicates necessary information
- 4 points - Task was attempted, but is missing major components.    
        - Missing comments, videos/photos, or reflection questions
- 3 points - Did not attempt or student should reattempt.  
        - Inappropriate use of AI tools.
