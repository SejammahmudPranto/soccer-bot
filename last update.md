int lmp=9; //left motorplus
int lmm=8; //left motorminus
int lmpwm=10;  //leftmotorpwm

int rmp=7; //rightmotorplus
int rmm=6; //rightmotorminus
int rmpwm=11;  //rightmotorpwm

int tp=4;
int tm=2;
int tpwm=3;

void lmfor() {      //leftmotorforward
  digitalWrite(lmp,HIGH);
  digitalWrite(lmm, LOW);
  analogWrite(lmpwm,255);
}

void lmrev() {      //leftmotorreverse
  digitalWrite(lmm,HIGH);
  digitalWrite(lmp, LOW);
  analogWrite(lmpwm,255);
}

void rmfor() {    //rightmotorforward
  digitalWrite(rmp,HIGH);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,255);
}

void rmrev() {    //rightmotorreverse
  digitalWrite(rmm,HIGH);
  digitalWrite(rmp, LOW);
  analogWrite(rmpwm,255);
}

void rmstop() {    //rightmotorstop
  digitalWrite(rmp,LOW);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,0);
}

void lmstop() {      //leftmotorstop
  digitalWrite(lmm,LOW);
  digitalWrite(lmp, LOW);
  analogWrite(lmpwm,0);
}

void leftgo() {    //front back motor forward
  rmstop();
  lmstop();
  digitalWrite(tp,HIGH);
  digitalWrite(tm, LOW);
  analogWrite(tpwm,255);
}

void rightgo() {    //front back motor reverse
  rmstop();
  lmstop();
  digitalWrite(tm,HIGH);
  digitalWrite(tp, LOW);
  analogWrite(tpwm,255);
}

void tstop() {    //front back motor stop
  digitalWrite(tp,LOW);
  digitalWrite(tm, LOW);
  analogWrite(tpwm,0);
}

void forward() {      //car forward
  rmfor();
  lmfor();
  tstop();
}

void reverse() {      //car reverse
  rmrev();
  lmrev();
  tstop();
}

void left() {       //car left
  rmfor();
  lmrev();
  tstop();
}

void right() {      //car right
  lmfor();
  rmrev();
  tstop();
}

void vehstop() {      //vehicle stop
  rmstop();
  lmstop();
  tstop();
}

void setup() {

  pinMode(lmp,OUTPUT);
  pinMode(lmm, OUTPUT);
  pinMode(lmpwm,OUTPUT);
  pinMode(rmp,OUTPUT);
  pinMode(rmm, OUTPUT);
  pinMode(rmpwm,OUTPUT);
  pinMode(tp,OUTPUT);
  pinMode(ltm, OUTPUT);
  pinMode(tpwm,OUTPUT);
  Serial.begin(9600);
  /*pinMode(rmp,OUTPUT);
  pinMode(rmm, OUTPUT);
  pinMode(rmpwm,OUTPUT);*/
  // put your setup code here, to run once:

}

void loop() {
  // put your main code here, to run repeatedly:

}
