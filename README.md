
int yendsecond, xendsecond;
int xendminute, yendminute;
int xendhour, yendhour;
float theta; 
void setup()
{
  
  size(600,600);
  background(303,0,0);
  xendsecond= 85;
  yendsecond= 0;


  xendminute= 65;
  yendminute= 0;

  xendhour= 40;
  yendhour= 0;
  frameRate(1);
}

void draw()
{
   
background(159,195,230);
translate(width/2, height/2);
fill(color(#A86FBA));

stroke(153,102,51);
strokeWeight(20);
ellipse(0,0,200,200);
fill(color(0));

strokeWeight(1);
stroke (color(55,0,0));
line(0,0,xendsecond,yendsecond);


strokeWeight(2);
stroke(color(0));
line(0,0,xendminute, yendminute);

strokeWeight(3);
stroke(color(144,0,0));
line(0,0,xendhour, yendhour);

ellipse(0,0,5,5);
text("12",-5,-100);
text("6",-5,100);
text("9",-100,0);
text("3",100,0);
 theta+= TWO_PI/60;
 
 xendsecond= int(85*cos(theta));
 yendsecond= int(85*sin(theta));
 xendminute= int(65*cos(theta/60));
 yendminute= int(65*sin(theta/60));
 xendhour= int(40*cos(theta/3600- PI/2));
 yendhour= int(40*sin(theta/3600- PI/2));

}

