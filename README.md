# Sending ELR message(s) to MLLP endpoint
To set up the environment,
* install python
* install hl7 by running "pip install -U hl7"

Prepare the hl7 message. The message needs to wrapped with the following character.

**<SB>message<EB><CR> for MLLP**
* <SB>: \x0b
* <EB>: \x1c
* <CR>: \x0d

Some ascii editor changes the end of line with a carriage return. In this case, it may cause
an error sending data.

To send the data, 
```mllp_send --file hl7v2msg251.txt --port 6661 localhost```
