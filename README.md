# EX 7 : THREE DIMENSIONAL TRANSFORMATIONS

## AIM :
 
 To implement the various transformations on three dimensional odjects using a c coding.

## EQUIPMENT REQUIRED:

●	Hardware: Personal Computer (PC)

●	Software: C Compiler

## ALGORITHM :


   Step 1 : Start.

   Step 2 : Draw an image with default parameters.

   Step 3 : Get the choice from user.

   Step 4 : Get the parameters for transformation.

   Step 5 : Perform the transformation.

   Step 6 : Display the output.

   Step 7 : Stop.

## Program :

    #include<stdio.h>  
    #include<conio.h> 
    #include<graphics.h> 
    #include<math.h>  
    int maxx,maxy,midx,midy; 
    void axis() 
    { 
    getch(); 
    cleardevice(); 
    line(midx,0,midx,maxy); 
    line(0,midy,maxx,midy); 
    } 
    void main() 
    {  
    int gd,gm,x,y,z,o,x1,x2,y1,y2; 
    detectgraph(&gd,&gm); 
    initgraph(&gd,&gm," "); 
    setfillstyle(0,getmaxcolor()); 
    maxx=getmaxx(); 
    maxy=getmaxy(); 
    midx=maxx/2; 
    midy=maxy/2; 
    axis(); 
    bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
    printf("Enter Translation Factor"); 
    scanf("%d%d%d",&x,&y,&z); 
    axis();  
    printf("after translation"); 
    bar3d(midx+(x+50),midy-(y+100),midx+x+60,midy-(y+90),5,1); 
    axis(); 
    bar3d(midx+50,midy+100,midx+60,midy-90,5,1); 
    printf("Enter Scaling Factor"); 
    scanf("%d%d%d",&x,&y,&z); 
    axis(); 
    printf("After Scaling"); 
    bar3d(midx+(x*50),midy-(y*100),midx+(x*60),midy-(y*90),5*z,1); 
    axis(); 
    bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
    printf("Enter Rotating Angle"); 
    scanf("%d",&o); 
    x1=50*cos(o*3.14/180)-100*sin(o*3.14/180); 
    y1=50*cos(o*3.14/180)+100*sin(o*3.14/180); 
    x2=60*sin(o*3.14/180)-90*cos(o*3.14/180); 
    y2=60*sin(o*3.14/180)+90*cos(o*3.14/180); 
    axis(); 
    printf("After Rotation about Z Axis"); 
    bar3d(midx+x1,midy-y1,midx+x2,midy-y2,5,1); 
    axis(); 
    printf("After Rotation about X Axis"); 
    bar3d(midx+50,midy-x1,midx+60,midy-x2,5,1); 
    axis(); 
    printf("After Rotation about Y Axis"); 
    bar3d(midx+x1,midy-100,midx+x2,midy-90,5,1); 
    getch(); 
    closegraph(); 
    }

## Output :


![Screenshot 2025-05-07 170215](https://github.com/user-attachments/assets/9d2dde59-6184-4b03-a6ea-e6e0ff124e43)

![Screenshot 2025-05-07 170221](https://github.com/user-attachments/assets/6f05fb47-1da5-492b-8edb-87a70061a26e)

![Screenshot 2025-05-07 170229](https://github.com/user-attachments/assets/68aac124-cc84-4b1e-aeb9-4e814925fec6)

![Screenshot 2025-05-07 170237](https://github.com/user-attachments/assets/ec951e40-735b-4b06-93e3-b8ae5cfc51a5)

![Screenshot 2025-05-07 170244](https://github.com/user-attachments/assets/8f3e7054-8a5d-497e-8213-e92ce2859b3b)


![Screenshot 2025-05-07 170253](https://github.com/user-attachments/assets/a85f82d7-5ed5-4c46-a560-7a643c104289)


![Screenshot 2025-05-07 170300](https://github.com/user-attachments/assets/a79b426f-2569-4a0c-8610-6f306e2bec73)


![Screenshot 2025-05-07 170306](https://github.com/user-attachments/assets/74312470-8c6f-44e6-9b6f-87912679da2d)

## name:yashwanth.asv
## reg no:212224230309

## Result :

Thus, the C program for performing three-dimensional transformations — including translation, scaling, and rotation about the X, Y, and Z axes — was successfully implemented and the output was verified through graphical representation.
