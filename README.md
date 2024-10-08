## Task 26: Frequency Counter

#### Overview
This task involves implementing a **frequency counter** using a timer and external interrupts on the **STC89C52 microcontroller**. The goal is to measure the frequency of a square wave signal provided by a frequency generator. The measured frequency will be displayed on a **seven-segment display**.

#### Instructions

1. **Setup External Interrupt:**
   - Enable an **external interrupt** on a capable pin (e.g., INT0) of the STC89C52 microcontroller.

2. **Triggering the Timer:**
   - When the **rising edge** of the input signal arrives, it should trigger the **external interrupt**.
   - In the **Interrupt Service Routine (ISR)**, start the **16-bit timer** to count the elapsed time.

3. **Measuring Frequency:**
   - On the arrival of the **next rising edge**, stop the timer.
   - Read the count value from the timer.
   - Calculate the frequency of the input signal based on the timer count and the clock frequency that is running the timer.

4. **Handling Timer Overflow:**
   - If the input signal frequency is too slow, the timer may overflow after the first rising edge.
   - In the case of an overflow, display an **"Error"** message on the **LCD** or show **"--------"** on the **seven-segment display**.

5. **Frequency Range Assessment:**
   - Determine the practical frequency range that can be measured with your setup.
   - Analyze and document the theoretical reasons for the **upper** and **lower limits** of the frequency measurement capabilities.
