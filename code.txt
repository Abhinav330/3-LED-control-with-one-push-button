 int y ;
 void setup() {
  Serial.begin(9600);
  pinMode(2 , OUTPUT);
  pinMode(3 , OUTPUT);
  pinMode(4 , OUTPUT);
  pinMode(5 , INPUT_PULLUP);
}

void loop() {
 int x  = digitalRead(5);
   
  if(x  == 0)
   {
     y++ ; 
    delay(200);
   }
  Serial.println(y);
  
   if(y == 1)
   {
    digitalWrite(2 , HIGH);
    digitalWrite(3 , LOW);
    digitalWrite(4 , LOW);
   }
  else if( y == 2)
  {
     digitalWrite(3 , HIGH);
    digitalWrite(2, LOW);
    digitalWrite(4 , LOW);
  }

 else if( y == 3)
  {
     digitalWrite(4 , HIGH);
    digitalWrite(2, LOW);
    digitalWrite(3 , LOW);
  } 
else if( y == 4)
  {
     digitalWrite(2 , LOW);
     digitalWrite(3, LOW);
     digitalWrite(4 , LOW);
     y = 0 ;
  }
}
