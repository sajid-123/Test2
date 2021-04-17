
//Point.java

public class Point {
 
    //Instance variable

private int x;

private int y;

//Default constructor

public Point()

{
//initializing instance variables 
    
    x = 0;
    
    y = 0;
    
    
}

//Other Constructor

public Point(int x, int y)

{

this.x = x;

this.y = y;

}

//Copy Constructor

public Point(Point p)

{

this(p.x, p.y);

}

//Accessor method

public double getDistance(Point p)

{

 double distance = Math.sqrt((this.x-p.x) * (this.x-p.x) + (this.y-p.y) * (this.y-p.y));   
    
return distance;

}

public int getX()

{

return x;

}

public int getY()

{

return y;

}

//Mutator method

public void set(int x, int y)

{

this.x = x;

this.y = y;

}

//toString method

public String toString()

{

return String.format("Given Point (" + x + "," + y + ")");

}

}






//Line.java






package Count;

public class Line {
   //Instance variable

private Point p1;

private Point p2;

//Default constructor

public Line()

{

    p1 = null;

    p2 = null;
    
    
    
}

//Other constructor

public Line(Point p1, Point p2)

{

this.p1 = new Point(p1);

this.p2 = new Point(p2);

}

//Copy constructor

public Line(Line aLine)

{

this(aLine.p1, aLine.p2);

}

//Accessor method

//Compute the distance

public double getDistance()

{

double distance = p1.getDistance(p2);

return distance;

}

public Point getP1()

{

return p1;

}

public Point getP2()

{

return p2;

}

//Mutator method

public void set(Point p1, Point p2)

{

this.p1 = p1;

this.p2 = p2;

}

//toString Method

public String toString()

{

return "Line ( Point("+ p1.getX() + ", " + p1.getY() + "), Point("+p2.getX() + 

           "," + p2.getY() +"),   distance = "+String.format(" %.4f",getDistance())+")";

}

} 



//  YunLiangNikosGo_A2.java






import java.util.Random;

public class YunLiangNikosGo_A2 {
    
    //To generate random numbers

private static int getInt()

{

int rand = (int)(Math.random() * 200) - 100;

return rand;

}

//To generate two points

private static void getTwoPoints(Point p1, Point p2)

{

// passing these two points for line information 

Line aLine = new Line(p1, p2);

System.out.println(aLine.toString());

}

private static Random rand = new Random();

public static void main(String[] args)

{

for(int i = 1; i <= 5; i++)

{
if(i <=4 ){
    
System.out.println("Set " + i);

Point p1 = new Point(getInt(), getInt());

System.out.println(p1.toString());

Point p2 = new Point(getInt(), getInt());

System.out.println(p2.toString());


// passing two points for line information 

getTwoPoints(p1,p2);

System.out.println("----------------");


}else{
    
    System.out.println("Set " + i);
Point p1 = new Point(getInt(), getInt());


System.out.println(p1.toString());

Point p2 = new Point(getInt(), getInt());

System.out.println(p2.toString());


// passing two points for line information 

getTwoPoints(p1,p2);




    
}
}

}
}





Click here to see output : [SampleOutput.txt](https://github.com/sajid-123/Test2/files/6329125/SampleOutput.txt)
