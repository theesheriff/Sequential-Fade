# Sequential-Fade
// Fade multiple LEDs in a sequence back and forth

int LED1= 5;
int LED2=10;
int LED3= 11;
int LED4=6;


void setup() {
  // put your setup code here, to run once:
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(11, OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
    
    for (int i=5; i<=11; i++)
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
