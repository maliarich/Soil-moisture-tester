# Soil-moisture-tester
A soil moisture prototype

Soil moisture project/ sensor measures the volumetric water content in soil.

# Objective 

This  project is to help farmers and  households to keep track of their moisture content of the soil in their farms and kitchen garden respectively within the  Refugee camps.

*Features of the project*

Works with a battery (7v) and solar panels
 Digital counter of :-
      3 displays “Low /dry moisture level 
      6 displays “ Moderate moisture level 
      9 displays “ High moisture level
3. Buzzer for sound – This Bips when there is high moisture level
4. Light weight.

Expected Improvements 
-    Casing 
 Adjustments in accuracy
 Soldering components on soldering Board.
 
 ![photo_2022-03-28_14-37-18](https://user-images.githubusercontent.com/56769901/160479811-5ad5eb20-04d4-4f6b-a735-e2c0622d77a8.jpg)


![photo_2022-03-28_14-37-47](https://user-images.githubusercontent.com/56769901/160478942-f1038606-6d46-46f5-870d-c77791aadd55.jpg)


# Images.

The three stages of the soil moisture level 

*DRY 

![photo_2022-03-28_14-38-28](https://user-images.githubusercontent.com/56769901/160479071-4ba658b3-2a34-498b-81d9-177cf4645483.jpg)

Mid - Moistured

![photo_2022-03-28_14-38-34](https://user-images.githubusercontent.com/56769901/160479176-c7cec990-84e4-4571-8183-a79efa8f3815.jpg)

Most - Moistured

![photo_2022-03-28_14-38-44](https://user-images.githubusercontent.com/56769901/160479271-4c510e4b-9e84-4c8e-9ea4-cc2f55ea08e2.jpg)

![photo_2022-03-28_14-31-33](https://user-images.githubusercontent.com/56769901/160479885-31edc906-7bca-43c2-b966-ce757f2c1a32.jpg)


# Codes 

`` int a =13;
int b =12;
int c =11;
int d =10;
int e = 9;
int f = 8;
int g = 7;
int sound =6;
void setup() {
  // put y  
  pinMode(a,OUTPUT);
  pinMode(b,OUTPUT);
  pinMode(c,OUTPUT);
  pinMode(d,OUTPUT);                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  
  pinMode(e,OUTPUT);
  pinMode(f,OUTPUT);
  pinMode(g,OUTPUT);
 pinMode(sound,OUTPUT);
}
void loop() {
  // put your main code here, to run repeatedly:
  int value = analogRead(A5);   
  Serial.println(value);
  if(value>500){
    digitalWrite(a,HIGH);
    digitalWrite(b,HIGH);
    digitalWrite(c,HIGH);
    digitalWrite(d,HIGH);
    digitalWrite(e,LOW);
    digitalWrite(f,HIGH);
    digitalWrite(g,HIGH);
    digitalWrite(sound,HIGH);
    delay(2000);
    digitalWrite(sound,LOW);
    }
  else if(value<500&value>300){
     digitalWrite(a,HIGH);
    digitalWrite(b,LOW);
    digitalWrite(c,HIGH);
    digitalWrite(d,HIGH);
    digitalWrite(e,HIGH);
    digitalWrite(f,HIGH);
    digitalWrite(g,HIGH);
    
   
  }
else{
   digitalWrite(a,HIGH);
    digitalWrite(b,HIGH);
    digitalWrite(c,HIGH);
    digitalWrite(d,HIGH);
    digitalWrite(e,LOW);
    digitalWrite(f,LOW);
    digitalWrite(g,HIGH); 
}
} ``


