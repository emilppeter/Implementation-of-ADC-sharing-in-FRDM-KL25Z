# Implementation-of-ADC-sharing-in-FRDM-KL25Z
Built an ADC server to enable sharing of ADC between buck converter controller and touchscreen code, while maintaining correct timing for the buck converter controller.The buck converter controller contols the brightness of an HBLED based on the set peak current.LCD used is 320x240 pixel color TFT LCD with touchscreen. The system is designed to do the following:
• A rectangular slider at the bottom of the screen slides across as per the orientation of the LCD based on the inputs from the       acclerometer attached to the shield on which the LCD is mounted. 
• On the top of the screen,the X and Y coordinates of the orientation of the LCD is displayed.
• If touched in upper portion of screen (above the Dim <--> Bright text),it draws a white line between previous and current touch     points.
• If touched in lower portion of screen (on or below the Dim <--> Bright text),it sets the peak current (g_peak_set_current) to       between 1 and 120 mA, based on the X position of the touch.
