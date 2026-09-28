

# Software-related modifications


For those who find the 40 standard channels sufficient but would like a bit more power at the antenna base, here's a tip that doesn't require opening the device!

## Change "region"

- Power the radio off
- Press and hold the PTT button and AM/FM
- Power the radio on
- Using the up/down arrows, you can now switch between **Fcc** , **CE** and **Bra**. 
- Turn off to acknowledge.


### Fcc
This setting gives you 40 channels AM/FM and the extra menu setting Po (Power Lo/Hi).
| Name | Po menu | Channels | Modes | Range |
| -- | -- | -- | -- | -- |
| Fcc  | yes | 40 |  AM/FM |  26.965 - 27.405 |
 

### Bra
This setting gives you 80 channels AM/FM in two bands and the extra menu setting Po (Power Lo/Hi).
| Name | Po menu | Channels | Modes | Range |
| -- | -- | -- | -- | -- |
| Bra  | yes | 80 |  AM/FM |  26.965 - 27.855 |

Tap the MENU button twice to switch between band d (1-40) and E (41-80).

### CE
Here starts the fun, you can switch between a few country settings.

To do this :
- Power the radio off
- Press and hold the AM/FM button
- Power the radio on
- Using the up/down arrows, you can now switch between **EU** , **CE** , **U**, **PL**, **I2**, **dE** and **In** 
- Turn off to acknowledge.

There is no Po (Power Output Hi/Lo) menu item available.

| Band name | AM/FM | Channels | Range |
| -- | -- | -- | -- |
| EU | AM/FM | 40 | 26.965 - 27.405 |
| CE| FM | 40 | 26.965 - 27.405 |
| U | AM/FM | 40 | 26.965 - 27.405 |
|  | FM U | 40 | 27.600 - 27.990 |
| PL| AM/FM | 40 | 26.960 - 27.400 |
| I2| AM/FM | 36 | 26.965 - 26.865 |
| dE| AM/FM | 80 | 26.565 - 26.405 |
| IN| AM/FM | 27 | 26.965 - 27.275 |


## Service menu

**Use at your own risk!**

- Power the radio off
- Press and hold the PTT button, Menu  and AM/FM
- Power the radio on
- Cycle thru the menu with Up/Down

Press PTT while changing a value, it is saved after power off/on.
Values are displayed in HEX.

| What | Value HEX | Value dec | What is it for  |
|----|----|----|-----|
| 01   | - | - | Channel 1 ?  |
| 02   | - | - | Channel 2 ?  |
| 03   | -  | - | Channel 3 ?  |
| Fr | 67 | 103 |    |
| PH | Cd | 205 | Power High   |
| Pn | 80| 128 | Power Normal ?  |
| PL | 71 | 113 | Power Low  |
| Fn   | 39  | 57 |                            |
| A4   | 29  | 41 |                          |
| A8   | 4E    | 78 |                           |
| to   | 00/0  |  |                          |
| 5H   | AC    | 172 | Squelch treshold? See text 5H below|
| 5C   | 7d    | 125 |                          |
| 5A   | 43    | 67 |                          |
| 59   | F7    | 247 |                          |
| 57   | 99    |  153 |                          |
| 55   | 1A    | 26 |                          |
| 53   | 67    | 103 |                          |
| 5L   | 6d    | 109 | is now 5F, Signal Level (SL instead of 5L) ?                 |
| AH   | 9F    | 159  |                         |
| AL   | 97    |  151 |                         |
| 5t   | 03    | 3  |                         |
| At   | 04    | 4  |                         |
| Pb   |  -  | -  |                         |

#### 5H (or SH?)

This looks like the squelch setting. The inital value was AC, now CF. 
I pressed PTT by accident and hit the up button. The original value of AC jumped to 1C.
After restart if the radio I noticed that my squelch dit not work, even on relative weak signals. Complete turning clockwise did nothing.
Back in the service menu I tried to get that AC value bakc somehow, but failed. Values I got back were 16 24 1C 1b 25 26 29.
This got me thinking that those values were signal strengths. 

I set the CB to channel 20, took my hackrf also on 27.205 (channel 20) and transmitted an FM signal.
Back in the service menu I received a stronger signal then before, but not the signal from channel 20.
No idea on what the cb receives in service mode. But changing the power levels on the hackrf did something on the cb radio.
Signal went weaker/stronger. I keyed the PTT and pushed the Up button. The value was now CF.
After power off/on the squelch worked as before.

In decimal is the original hex value AC = 172. Other values are 16 = 22, 1C = 28, 29 = 41.
So CF = 207


---