# Quick-Assembly-Sorting-Algorithm
This AVR assembly project for the ATxmega128A1U reads 8-bit values from program memory and processes them based on specific conditions. Depending on bit 7, values are multiplied or divided with adjustments. The filtered output, when viewed in ASCII, spells "EElabworld."





This AVR assembly project for the ATxmega128A1U begins by reading a predefined table of 8-bit values stored in program memory starting at address 0xCAFE. The program processes each byte in a loop until it encounters a NULL value, which marks the end of the input data. For every byte, it first checks the status of bit 7: if bit 7 is not set, the byte is multiplied by 2 and then, if the result is greater than or equal to 70, 37 is subtracted before storing it; if bit 7 is set, the byte is divided by 2 and, if the result is less than 110, it is incremented by 1. Each processed value is then stored sequentially in an output table allocated in data memory starting at address 0x311A, and a NULL terminator is added at the end. When the output data is viewed as ASCII characters, it spells out the message “EElabworld,” showcasing various embedded programming techniques such as conditional branching, arithmetic manipulation, and memory management.
