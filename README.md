# medio.curso..
ejercicio1.1

int c1x=50;
int c1y=50;
int c2x=50;
int c2y=550;
int c3x=550;
int c3y=50;
int c4x=550;
int c4y=550;
int w=50;
int b=255;

void setup(){
background(b);
size(600,600);
}

void draw(){
  background(b);
  if(mousePressed&&(mouseButton==LEFT)) {
    c1x=c1x+20;
    c1y=c1y+20;
    c2x=c2x+20;
    c2y=c2y-20;
    c3x=c3x-20;
    c3y=c3y+20;
    c4x=c4x-20;
    c4y=c4y-20;
fill(0);
ellipse(c1x,c1y,w,w);
ellipse(c2x,c2y,w,w);
ellipse(c3x,c3y,w,w);
ellipse(c4x,c4y,w,w);

}
}

ejercicio 1.2

int l1a=300;
int l1b=300;
int l2a=0;
int l2b=300;

int l3b=0;

void setup(){
background(255);
size(300,300);
}

void draw(){
  background(255);
  if(mousePressed&&(mouseButton==LEFT)) {
  l1a=l1a-1;
  l1b=l1b-1;
  l2a=l2a+1;
  l2b=l2b-1;
  l3b=l3b+1;
  
line(150,150,l1a,l1b);
line(150,150,l2a,l2b);
line(150,150,150,l3b);
}
}

ejericio1.3

float click=0;

void setup(){
background(255);
size(500,500);
}

void draw(){
  fill(255);
  if(mousePressed&&(mouseButton==LEFT)) {
    click++;
  }
     if(click%3==0) {
    fill(0,0,255);
  }
    else if(click%2==0) {
    fill(0,255,0);
  }
  else if(click%1==0){
    fill(255,0,0);
  }
println(click);
println(click%3);

rect(50,50,400,400);
fill(255);
ellipse(251,251,200,200);

}

ejercicio.2

float random;
int c;

void setup(){
  size(200,320);
  background(100);
}
void draw(){
  if(mousePressed){ 
    c=int(random(0,4)); 
  }  
  switch(c)  //Creamos un caso para cada cara del dado
  {
    case 1: C1();break;
    case 2: C2();break;
    case 3: C3();break;

  }
}

void C1(){   //evento para el caso de la cara 1
  background(100);
  fill(255,0,0);
  ellipse(100,80,50,50);
  fill(0);
  ellipse(100,160,50,50);
  fill(0);
  ellipse(100,240,50,50);
}

void C2(){   //evento para el caso de la cara 1
  background(100);
  fill(0);
  ellipse(100,80,50,50);
  fill(#FAFF00);
  ellipse(100,160,50,50);
  fill(0);
  ellipse(100,240,50,50);
}

void C3(){   //evento para el caso de la cara 1
  background(100);
  fill(0);
  ellipse(100,80,50,50);
  fill(0);
  ellipse(100,160,50,50);
  fill(0,255,0);
  ellipse(100,240,50,50);
}
