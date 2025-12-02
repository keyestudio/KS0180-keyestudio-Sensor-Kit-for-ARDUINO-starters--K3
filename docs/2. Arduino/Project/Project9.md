### Project 9 Passive buzzer

![](media/image-20251127175144214.png)

**1.Introduction**

We can use Arduino to make many interactive works of which the most commonly used is acoustic-optic display. All the previous experiment has something to do with LED. However, the circuit in this experiment can produce sound. Normally, the experiment is done with a buzzer or a speaker while buzzer is simpler and easier to use. The buzzer we introduced here is a passive buzzer. It cannot be actuated by itself, but by external pulse frequencies. Different frequencies produce different sounds. We can use Arduino to code the melody of a song, which is actually quite fun and simple.

**2.Hardware required** 

- Passive buzzer*1
- Key *1
- Breadboard*1
- Breadboard jumper wires

![](media/wps11.jpg)

**3.Sample program**

```c
int buzzer=8;// select digital IO pin for the buzzer

void setup() 
{ 
	pinMode(buzzer,OUTPUT);// set digital IO pin pattern, OUTPUT to be output 
} 
void loop() 
{ 
	unsigned char i,j;//define variable
    while(1) 
    { 
        for(i=0;i<80;i++)// output a frequency sound
        { 
            digitalWrite(buzzer,HIGH);// sound
            delay(1);//delay1ms 
            digitalWrite(buzzer,LOW);//not sound
            delay(1);//ms delay 
        } 
        for(i=0;i<100;i++)// output a frequency sound
        { 
            digitalWrite(buzzer,HIGH);// sound
            digitalWrite(buzzer,LOW);//not sound
            delay(2);//2ms delay 
        }
    } 
} 
```

After downloading the program, buzzer experiment is finished.