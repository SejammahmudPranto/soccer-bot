int lmp=49; //left motorplus
int lmm=48; //left motorminus
int lmpwm=3;  //left motorpwm

int fmp=45; //front motorplus
int fmm=44; //front motorminus
int fmpwm=8;  //front motorpwm

int rmp=53; //right motorplus
int rmm=52; //right motorminus
int rmpwm=5;  //right motorpwm

int bmp=41; //back motorplus
int bmm=40; //backmotorminus
int bmpwm=7;  //rightmiddlemotorpwm

const int ms=255; //max speed
const int mids=200;//middle speed
const int ss=150;//slow speed

String readString;

void lmforf() {      //leftmotorforwardfast
  digitalWrite(lmp,HIGH);
  digitalWrite(lmm, LOW);
  analogWrite(lmpwm,ms);
}

void lmform() {      //leftmotorforwardmid
  digitalWrite(lmp,HIGH);
  digitalWrite(lmm, LOW);
  analogWrite(lmpwm,mids);
}

void lmfors() {      //leftmotorforwardslow
  digitalWrite(lmp,HIGH);
  digitalWrite(lmm, LOW);
  analogWrite(lmpwm,ss);
}

void lmrevf() {      //leftmotorrevfast
  digitalWrite(lmm,HIGH);
  digitalWrite(lmp, LOW);
  analogWrite(lmpwm,ms);
}

void lmrevm() {      //leftmotorrevmiddle
  digitalWrite(lmm,HIGH);
  digitalWrite(lmp, LOW);
  analogWrite(lmpwm,mids);
}

void lmrevs() {      //leftmotorrevslow
  digitalWrite(lmm,HIGH);
  digitalWrite(lmp, LOW);
  analogWrite(lmpwm,ss);
}

void rmforf() {      //rightmotorforwardfast
  digitalWrite(rmp,HIGH);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,ms);
}

void rmform() {      //rightmotorforwardmid
  digitalWrite(rmp,HIGH);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,mids);
}

void rmfors() {      //rightmotorforwardslow
  digitalWrite(rmp,HIGH);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,ss);
}

void rmrevf() {      //rightmotorreversefast
  digitalWrite(rmp,LOW);
  digitalWrite(rmm, HIGH);
  analogWrite(rmpwm,ms);
}

void rmrevm() {      //rightmotorreversemid
  digitalWrite(rmp,LOW);
  digitalWrite(rmm, HIGH);
  analogWrite(rmpwm,mids);
}

void rmrevs() {      //rightmotorreverseslow
  digitalWrite(rmp,LOW);
  digitalWrite(rmm, HIGH);
  analogWrite(rmpwm,ss);
}

void fmfor() { //frontmotorforward
  digitalWrite(fmp,HIGH);
  digitalWrite(fmm, LOW);
  analogWrite(fmpwm,ms);
}

void fmrev() {//frontmotorreverse
  digitalWrite(fmm,HIGH);
  digitalWrite(fmp, LOW);
  analogWrite(fmpwm,ms);
}

void bmfor() {//backmotorforward
  digitalWrite(bmp,HIGH);
  digitalWrite(bmm, LOW);
  analogWrite(bmpwm,ms);
}

void bmrev() {//backmotorreverse
  digitalWrite(bmm,HIGH);
  digitalWrite(bmp, LOW);
  analogWrite(bmpwm,ms);
}

void rmstop() {//rightmotorstop
  digitalWrite(rmp,LOW);
  digitalWrite(rmm, LOW);
  analogWrite(rmpwm,0);
}

void lmstop(){//leftmotorstop
  digitalWrite(lmp,LOW);
  digitalWrite(lmm, LOW);
  analogWrite(lmpwm,0);
}

void fmstop(){//frontmotorstop
  digitalWrite(fmp,LOW);
  digitalWrite(fmm, LOW);
  analogWrite(fmpwm,0);
}

void bmstop() {//backmotorstop
  digitalWrite(bmp,LOW);
  digitalWrite(bmm, LOW);
  analogWrite(bmpwm,0);
}

void forfast() {//forwardfast
  lmforf();
  rmforf();
  fmstop();
  bmstop();
}

void formid() {//forwardmidspeed
  lmform();
  rmform();
  fmstop();
  bmstop();
}

void forslow() {//forwardslow
  lmfors();
  rmfors();
  fmstop();
  bmstop();
}

void revfast() {//reversefast
  lmrevf();
  rmrevf();
  fmstop();
  bmstop();
}

void revmid() {//reversemid
  lmrevm();
  rmrevm();
  fmstop();
  bmstop();
}

void revslow() {//reverseslow
  lmrevs();
  rmrevs();
  fmstop();
  bmstop();
}

void rightspinfast() {//rightspinfast
  lmforf();
  rmrevf();
  fmstop();
  bmstop();
}

void rightspinslow() {//rightspinslow
  lmfors();
  rmrevs();
  fmstop();
  bmstop();
}

void rightspinmid() {//rightspinmid
  lmform();
  rmrevm();
  fmstop();
  bmstop();
}

void leftspinfast() {//leftspinfast
  rmforf();
  lmrevf();
  fmstop();
  bmstop();
}

void leftspinmid() {//leftspinmid
  rmform();
  lmrevm();
  fmstop();
  bmstop();
}

void leftspinslow() {//leftspinslow
  rmfors();
  lmrevs();
  fmstop();
  bmstop();
}

void rightturnfast() {//rightturnfast
  lmforf();
  rmstop();
  fmstop();
  bmstop();
}

void rightturnmid() {//rightturnmid
  lmform();
  rmstop();
  fmstop();
  bmstop();
}

void rightturnslow() {//rightturnslow
  lmfors();
  rmstop();
  fmstop();
  bmstop();
}

void leftturnfast() {//leftturnfast
  rmforf();
  lmstop();
  fmstop();
  bmstop();
}

void leftturnmid() {//leftturnmid
  rmform();
  lmstop();
  fmstop();
  bmstop();
}

void leftturnslow() {//leftturnslow
  rmfors();
  lmstop();
  fmstop();
  bmstop();
}

void leftbackturnfast() {//leftbackturnfast
  rmrevf();
  lmstop();
  fmstop();
  bmstop();
}

void leftbackturnmid() {//leftbackturnmid
  rmrevm();
  lmstop();
  fmstop();
  bmstop();
}

void leftbackturnslow(){//leftbackturnslow
  rmrevs();
  lmstop();
  fmstop();
  bmstop();
}

void rightbackturnfast() {//rightbackturnfast
  lmrevf();
  rmstop();
  fmstop();
  bmstop();
}

void rightbackturnmid() {//rightbackturnmid
  lmrevm();
  rmstop();
  fmstop();
  bmstop();
}

void rightbackturnslow() {//rightbackturnslow
  lmrevs();
  rmstop();
  fmstop();
  bmstop();
}

void vehstop() {//vehstop
  lmstop();
  rmstop();
  fmstop();
  bmstop();
}

void leftgo() {//leftgo
  lmstop();
  rmstop();
  fmfor();
  bmfor();
}

void rivghtgo() {//right go
  lmstop();
  rmstop();
  fmrev();
  bmrev();
}

void leftfrontcorner() {//leftfrontcorner
  fmfor();
  bmfor();
  lmforf();
  rmstop();
}

void leftbackcorner() {//leftbackcorner
  fmfor();
  bmfor();
  lmrevf();
  rmstop();
}

void rightbackcorner() {//rightbackcorner
  fmrev();
  bmrev();
  rmrevf();
  lmstop();
}

void rightfrontcorner() {//rightfrontcorner
  fmrev();
  bmrev();
  rmforf();
  lmstop();
}


void setup() {
  pinMode(fmp,OUTPUT);
  pinMode(fmm,OUTPUT);
  pinMode(bmp,OUTPUT);
  pinMode(bmm,OUTPUT);
  pinMode(fmpwm,OUTPUT);
  pinMode(bmpwm,OUTPUT);
  pinMode(rmp,OUTPUT);
  pinMode(rmm,OUTPUT);
  pinMode(rmpwm,OUTPUT);
  pinMode(lmp,OUTPUT);
  pinMode(lmm,OUTPUT);
  pinMode(lmpwm,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  /*
   lmforf();
   rmforf();
   fmfor();
   bmfor();
   */

  while(Serial.available()){
    delay(50);
    char c = Serial.read();
    readString+=c;
  }

  if(readString.length() > 0) {
    Serial.println(readString);


    if(readString == "FORWARD"){
      Serial.println("forfast");
      forfast();
    }
    
    if(readString == "formid"){
      formid();
      Serial.println("formid");
    }

    if(readString == "forslow"){
      forslow();
      Serial.println("forslow");
    }

    if(readString == "BACK"){
      revfast();
      Serial.println("revfast");
    }

    if(readString == "backmid"){
      revmid();
      Serial.println("revmid");
    }
    if(readString=="backslow") {
      revslow();
      Serial.println("revslow");
    }
    if(readString=="leftspinfast") {
      leftspinfast();
      Serial.println("leftspinfast");
    }
    if(readString=="leftspinmid") {
      leftspinmid();
      Serial.println("leftspinmid");
    }
    if(readString=="leftspinslow") {
      leftspinslow();
      Serial.println("leftspinslow");
    }
    if(readString=="rightspinfast") {
      rightspinfast();
      Serial.println("rightspinfast");
    }
    if(readString=="rightspinmid") {
      rightspinmid();
      Serial.println("rightspinmid");
    }
    if(readString=="rightspinslow") {
      rightspinslow();
      Serial.println("rightspinslow");
    }
    if(readString=="STOP") {
      vehstop();
      Serial.println("stop");
    }
    if(readString=="rightfast") {
      rightturnfast();
      Serial.println("rightturnfast");
    }
    if(readString=="rightmid") {
      rightturnmid();
      Serial.println("rightturnmid");
    }
    if(readString=="rightslow") {
      rightturnslow();
      Serial.println("righturnslow");
    }
    if(readString=="leftfast") {
      leftturnfast();
      Serial.println("leftturnfast");
    }
    if(readString=="leftmid") {
      leftturnmid();
      Serial.println("leftturnmid");
    }
    if(readString=="leftslow") {
      leftturnslow();
      Serial.println("leftturnslow");
    }
    if(readString=="backrightfast") {
      rightbackturnfast();
      Serial.println("rightbackturnfast");
    }
    if(readString=="backrightmid") {
      rightbackturnmid();
      Serial.println("rightbackmid");
    }
    if(readString=="backrightslow") {
      rightbackturnslow();
      Serial.println("rightbackturnslow");
    }
    if(readString=="backleftfast") {
      leftbackturnfast();
      Serial.println("leftbackturnfast");
    }
    if(readString=="backleftmid") {
      leftbackturnmid();
      Serial.println("backleftturnmid");
    }
    if(readString=="backleftslow") {
      leftbackturnslow();
      Serial.println("leftbackturnslow");
    }
    if(readString=="rightgo") {
      rightgo();
      Serial.println("rightgo");
    }
    if(readString=="leftgo") {
      leftgo();
      Serial.println("leftgo");
    }
    if(readString=="frontrightgo") {
      rightfrontcorner();
      Serial.println("frontrightcorner");
    }
    if(readString=="frontleftgo") {
      leftfrontcorner();
      Serial.println("frontleftcorner");
    }
    if(readString=="backrightgo") {
      rightbackcorner();
      Serial.println("backrightcorner");
    }
    if(readString=="backleftgo") {
      leftbackcorner();
      Serial.println("backleftcorner");
    }
    readString = "";
 }
}
