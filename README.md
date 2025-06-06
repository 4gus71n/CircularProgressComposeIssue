### CircularProgressIndicator bug

I think there is a bug with the `CircularProgressIndicator` if it is ever used within an `AndroidFragment`, it freezes all other Composables `onClick` callbacks. 

### Repro steps

1. Run this code here
2. Click the "Click me!" button, you wills see a test Toast go off.
3. Scroll down
4. Scroll up
5. Click the Click me!" button again.

Expected: You see the toast go off.
Actual: The click even seems to be completely ignored, not even the ripple effect gets triggered.

### Demo vid

https://github.com/user-attachments/assets/52d5b019-26c1-4743-a281-c76af64aa83f

### Notes

- As soon as we comment out the `CircularProgressIndicator` everything works fine.
