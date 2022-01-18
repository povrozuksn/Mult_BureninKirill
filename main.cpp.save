#include "TXLib.h"

void Fon()
{
    txSetColor(TX_LIGHTBLUE,3);
    txSetFillColor( RGB ( 87, 168, 227));
    txRectangle(0,0,1900,913);
}

void Zemly()
{
    txSetColor(TX_GREEN,3);
    txSetFillColor(TX_GREEN);
    txRectangle(0,462,1900,913);
}

void home()
{
    txSetColor(TX_RED,3);
    txSetFillColor(TX_RED);
    txRectangle(1280,600,1570,760);
    txSetColor(TX_WHITE,3);
    txSetFillColor(TX_WHITE);
    txRectangle(1380,640,1450,760);
    txLine(1280,600,1420,510);
    txLine(1420,510,1570,600);

    txSetFillColor(TX_YELLOW);
    POINT Krusha[3] = {{1280,600}, {1420,510}, {1570,600}};
    txPolygon(Krusha, 3);
}
void door(int x, int y)
{
    txSetColor(TX_BROWN,3);
    txSetFillColor(TX_BROWN);
    POINT door[4] = {{x,y},
                     {1450,640},
                     {1450,760},
                     {x,y+120}};
    txPolygon(door,4);
}
void car(int x,int y, double a)
{

    int x0=x+65;
    int y0=y+125;
    int x1,y1,x2,y2,x3,y3;
    int r=35;

    txSetColor(TX_YELLOW,3);
    txSetFillColor(RGB (251, 251, 21));
    //кабина
    txRectangle(x+80 ,y-100+50 ,x+230, y-30+50 );
    txSetColor(TX_LIGHTBLUE,3);
    txSetFillColor(RGB (27, 243, 217));
    txRectangle(x+120,y-20,x+200,y+20);
    //Кузов
    txSetColor(TX_YELLOW,3);
    txSetFillColor(RGB (251, 251, 21));
    txRectangle(x ,y-30+50 ,x+300 ,y+80+30 );

    txSetColor(TX_BLACK,3);
    txSetFillColor(TX_BLACK);
    txCircle(x+65 ,y+125 ,r);
    txCircle(x+235 ,y+125 ,r);
    txSetColor(TX_WHITE);
    txSetFillColor(TX_WHITE);

    x1=x0+r*cos(a*3.14/180);
    y1=y0+r*sin(a*3.14/180);
    x2=x0+r*cos((a+120)*3.14/180);
    y2=y0+r*sin((a+120)*3.14/180);
    x3=x0+r*cos((a+240)*3.14/180);
    y3=y0+r*sin((a+240)*3.14/180);

    txLine(x0,y0,x1,y1);
    txLine(x0,y0,x2,y2);
    txLine(x0,y0,x3,y3);

    txLine(x0+170,y0,x1+170,y1);
    txLine(x0+170,y0,x2+170,y2);
    txLine(x0+170,y0,x3+170,y3);
}

void sun(int x, int y)
{
    txSetColor(TX_YELLOW,3);
    txSetFillColor(RGB (251, 251, 21));
    txCircle(x, y, 50);
}

void home2()
{
    txSetColor(TX_BLUE);
    txSetFillColor(TX_BLUE);
    txRectangle(100,600,370,760);
    txSetColor(TX_BROWN,3);
    txSetFillColor(TX_BROWN);
    txRectangle(190,640,270,760);


    txLine(100,600,250,510);
    txLine(250,510,370,600);

    txSetFillColor(TX_YELLOW);
    POINT Krusha1[3] = {{100,600}, {250,510}, {370,600}};
    txPolygon(Krusha1, 3);
}
void man(int x, int y)
{
    {
    txSetColor(TX_YELLOW,3);
    txSetFillColor(RGB(255,255,164));
    txCircle(x,y,30);
    txSetColor(TX_BLACK,3);
    txSetFillColor(TX_BLACK);
    txLine(x,y+40,x,y+90);
    txLine(x,y+40,x+40,y+70);
    txLine(x,y+40,x-40,y+70);
    txLine(x,y+90,x-40,y+120);
    txLine(x,y+90,x+30,y+120);
    }
}
void man2(int x, int y)
{

    txSetColor(TX_YELLOW,3);
    txSetFillColor(RGB(255,255,164));
    txCircle(x,y,30);
    txLine(x,y+40,x,y+110);
    txSetColor(TX_BLACK,3);
    txSetFillColor(TX_BLACK);
    txLine(x,y+40,x-40,y+80);
    txLine(x,y+40,x+40,y+80);
    txLine(x,y+110,x+20,y+150);
    txLine(x,y+110,x-20,y+150);

 }
void tree()
{
    txSetColor(TX_BROWN,3);
    txSetFillColor(TX_BROWN);
    txRectangle(1660,650,1730,850);
    txSetColor(TX_LIGHTGREEN,3);
    txSetFillColor(TX_LIGHTGREEN);
    txEllipse(1600,460,1780,655);

}
void drawStaticScena()
{
    Fon();
    Zemly();
    home();
    home2();
    tree();
}
void drawStaticScena2()
{
    Fon();
    Zemly();
    home();
    home2();
    tree();
}

void dialog(int x, int y, const char* text)
{
    txSetColor(TX_BLACK);
    txSetFillColor(TX_WHITE);
    txSelectFont("Times",20);
    txEllipse(x-50,y-20,x+50,y+20);
    txDrawText(x-50,y-20,x+50,y+20,text);
    txSleep(1000);
}

    int main()
{
    double a=0;
    txCreateWindow (1900, 913);
    int xSun=-100;
    int xCar=-100;
    int xMan=600;
    int xMan2;
    int xDoor=1380;
    int yDoor=640;
    int yText=1900;
    int yText1=1899;



    while(yText>-10)
    {
     txBegin();
     txSetColor(TX_WHITE,3);
     txSetFillColor(TX_WHITE);
     txRectangle(0,0,1900,913);
     txSetColor(TX_BLACK,3);
     txSetFillColor(TX_BLACK);
     txSelectFont("Times", 50);
     txDrawText(0,yText-913,1900,yText,
               "Dreamer animation "
               "\n"
               "Представляет\n"
               "\n"
               "Ccора друзей");
     yText=yText-15;
     txSleep(10);
     txEnd();
    }

    while (xSun<=100)
    {
    txBegin();
    drawStaticScena();
    //СОЛНЦЕ
    sun(900,xSun);
    xSun=xSun+10;
    man(xMan,600);
    door(xDoor,yDoor);
    txSleep(20);
    txEnd();
    }

    while (xCar<=1900)
    {
    txBegin();
    drawStaticScena();
    //СОЛНЦЕ
    sun(900,xSun);
    man(xMan,600);
    //машина
    car(xCar,315,a);
    xCar=xCar+20;
    a=a+10;
    door(xDoor,yDoor);
    txSleep(10);
    txEnd();
    }


    while (xDoor<1450)
    {
    txBegin();
    drawStaticScena();
    door(xDoor,yDoor);
    man(xMan,600);
    xDoor=xDoor+5;
    yDoor=yDoor+5;
    sun(900,xSun);
    txSleep(10);
    txEnd();
    }

    xMan2=xDoor;

    while(xMan2>=xMan+150)
    {
    txBegin();
    drawStaticScena();
    man2(xMan2,yDoor);
    door(xDoor,yDoor);
    xMan2=xMan2-10;
    man(xMan,600);
    sun(900,xSun);
    txSleep(10);
    txEnd();
    }

   while (xDoor>1380)
    {
    txBegin();
    drawStaticScena();
    door(xDoor,yDoor);
    man(xMan,600);
    man2(xMan2,yDoor);
    xDoor=xDoor-5;
    yDoor=yDoor-5;
    sun(900,xSun);
    txSleep(10);
    txEnd();
    }



    dialog(xMan2,  540, "Привет!");

    dialog(xMan, 540, "Привет..");
    dialog(xMan,  540, "Почему ты ");
    dialog(xMan, 540, "так долго?!");
    dialog(xMan2,  540, "Прости");
    dialog(xMan2, 540, "я маме ");
    dialog(xMan2, 540, "помогал");
    dialog(xMan,  540, "Ага,конечно");
    dialog(xMan, 540, "опять играл");
    dialog(xMan, 540, "в игрульки");
    dialog(xMan2, 540, "да нет");
    dialog(xMan2, 540, "я не вру");
    dialog(xMan, 540," признайся");
    dialog(xMan, 540,"что играл");
    dialog(xMan, 540,"в стрелялки");
    dialog(xMan2, 540,"Ecли ты ");
    dialog(xMan2, 540,"не веришь");
    dialog(xMan, 540,"Не верю");
    dialog(xMan2, 540,"Знаешь что?");
    dialog(xMan, 540,"Что?");
    dialog(xMan2, 540,"Я на тебя..");
    dialog(xMan2, 540,"Обиделся!!!!");



   while(yText1>-10)
    {
     txBegin();
     txSetColor(TX_BLACK,3);
     txSetFillColor(TX_BLACK);
     txRectangle(0,0,1900,913);
     txSetColor(TX_WHITE,3);
     txSetFillColor(TX_WHITE);
     txSelectFont("Times",50);
     txDrawText(0,yText1-913,1900,yText1,
               "Вот и мультику конец\n"
               "\n"
               "А кто смотрел\n"
               "\n"
               "Молодец!!!\n"
               "\n"
               "Автор:Кирилл");


    yText1=yText1-15;
    txSleep(10);
    txEnd();

    }

    return 0;
}

