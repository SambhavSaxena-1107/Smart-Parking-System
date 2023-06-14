#include <Servo.h> //includes the servo library
#include <Wire.h> 
#include <LiquidCrystal_I2C.h> //includes LiquidCrystal_I2C library
LiquidCrystal_I2C lcd(0x27, 20, 4);

Servo myservo;

#define ir_enter 2
#define ir_back  4

#define ir_car1 5
#define ir_car2 6
#define ir_car3 7
#define ir_car4 8

int S1=0, S2=0, S3=0, S4=0 ;
int flag1=0, flag2=0; 
int slot = 6;  

void setup(){
Serial.begin(9600);
// initialize digital pins as input.
pinMode(ir_car1, INPUT);
pinMode(ir_car2, INPUT);
pinMode(ir_car3, INPUT);
pinMode(ir_car4, INPUT);

pinMode(ir_enter, INPUT);
pinMode(ir_back, INPUT);
  
myservo.attach(9); // Servo motor pin connected to D9
myservo.write(90); // sets the servo at 0 degree position

// Print text on display
lcd.begin(20, 4);  
lcd.setCursor (0,1);
lcd.print("    Smart Car   ");
lcd.setCursor (0,2);
lcd.print(" Parking System ");
delay (2000);
lcd.clear();   

Read_Sensor();

int total = S1+S2+S3+S4;
slot = slot-total; 
}

void loop()
{

 Read_Sensor();

 lcd.setCursor (0,0);
 lcd.print("   Have Slot: "); 
 lcd.print(slot);
 lcd.print("    ");  

 lcd.setCursor (0,1);
  if(S1==1)
   {
    lcd.print("S1:Fill ");
   }
  else
   {
    lcd.print("S1:Empty");
   }

 lcd.setCursor (10,1);
  if(S2==1)
   {
    lcd.print("S2:Fill ");
    }
  else
   {
    lcd.print("S2:Empty");
    }

 lcd.setCursor (0,2);
  if(S3==1)
   {
    lcd.print("S3:Fill ");
    }
  else
   {
    lcd.print("S3:Empty");
    }

 lcd.setCursor (10,2);
  if(S4==1)
   {
    lcd.print("S4:Fill ");
    }
  else
   {
    lcd.print("S4:Empty");
    }
    
/* Servo Motor Control
***********************/
  if(digitalRead (ir_enter) == 0 && flag1==0) // read degital data from IR sensor1
   {
    if(slot>0)
     {
      flag1=1;
      if(flag2==0)
       {
        myservo.write(180); 
        slot = slot-1;
        }
     }
    else
     {
      lcd.setCursor (0,0);
      lcd.print(" Sorry Parking Full ");  
      delay(1500);
      }   
   }

  if(digitalRead (ir_back) == 0 && flag2==0) // read degital data from IR sensor2
   {
    flag2=1;
    if(flag1==0)
     {
      myservo.write(180); // sets the servo at 180 degree position
      slot = slot+1;
      }
   }

  if(flag1==1 && flag2==1)
   {
    delay (1000);
    myservo.write(90); // sets the servo at 90 degree position
    flag1=0, flag2=0;
    }
    delay(1);
}

void Read_Sensor()
{
 S1=0, S2=0, S3=0, S4=0;
 if(digitalRead(ir_car1) == 0){S1=1;} // read degital data from IR sensor3
 if(digitalRead(ir_car2) == 0){S2=1;} // read degital data from IR sensor4
 if(digitalRead(ir_car3) == 0){S3=1;} // read degital data from IR sensor5
 if(digitalRead(ir_car4) == 0){S4=1;} // read degital data from IR sensor6
}
