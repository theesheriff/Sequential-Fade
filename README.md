# Sequential-Fade
// Fade multiple LEDs in a sequence back and forth

int LED1= 9;
int LED2=10;
int LED3= 11;
int LED4=12;
int myPins[5] = {9, 10, 11, 12};

void setup() {
  // put your setup code here, to run once:
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(12, OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
    
    for (int i=9; i<=12; i++)
    {
      fade();
    }
}

void fade(){
    for(int i=0; i<=255; i++)
    {
      analogWrite(i, i);
      delay(100);
    }
      delay(500);
      
    for(int i=255; i>=1; i--)
    {
      analogWrite(i, i);
      delay(100);
    }
    delay(500);
    }
