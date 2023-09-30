# Welcome!

This Python template lets you get started quickly with a simple one-page playground.

```python runnable
import sys
import time


def fade_in(start, end, steps, delay):
    for i in range(steps):
        alpha = i / (steps - 1)
        current_char = chr(int(start + alpha * (end - start)))
        sys.stdout.write(current_char)
        sys.stdout.flush()
        time.sleep(delay / steps)
        sys.stdout.write('\b')
        sys.stdout.flush()

def print_fade(message="", delay=0.1, fade_steps=15):
    for char in message:
        fade_in(ord(' '), ord(char), fade_steps, delay)
        sys.stdout.write(char)
        sys.stdout.flush()
    print()  

if __name__=='__main__':
    print_fade("Welcome Everyone 😈!")
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced Python template](https://tech.io/select-repo/429)
