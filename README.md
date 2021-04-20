


import java.util.Scanner;
abstract class Polygon {
    
    
   abstract  double area();
    
   abstract double perimeter(); 
   
   
}


public class Triangle extends Polygon {

    
    double sideA;
    
    double sideB;
    
    double sideC;
    
    
    Triangle(){
        
        sideA = 0.0;
        
        sideB = 0.0;
        
        sideC = 0.0;
        
        
        
    }

    public void setSideA(double sA) {
        this.sideA = sA;
    }

    public void setSideB(double sB) {
        this.sideB = sB;
    }

    public void setSideC(double sC) {
        this.sideC = sC;
    }
    
    
    
    
    
    
    @Override
    double area() {
        
      
       double s =   perimeter()/2;
        
      double Area =  Math.sqrt(s*(s-sideA)*(s-sideB)*(s-sideC));
        
        return Area;
        
    }

    @Override
    double perimeter() {
        
        double Perimeter = (sideA +sideB + sideC);
        
        return Perimeter;
        
    }
   
    
    
    public static void main(String[] args){
        
        
        
        Scanner sc = new Scanner(System.in);
        
        // creating object of Triangle class
        
        Triangle ob = new Triangle();
        
        
        System.out.println("Please enter the three(3) sides of Triangle");
        
        double a = sc.nextDouble();
        
        double b = sc.nextDouble();
        
        
        double c = sc.nextDouble();
        
        
        
        // validating input values 
        
        
        if( (a+b) > c && (a+c) > b && (b+c) > a){
            
            
            ob.setSideA(a);
            
            ob.setSideB(b);
            
            ob.setSideC(c);
            
            
            double Perimeter_Of_Triangle = ob.perimeter();
            
            double Area_Of_Triangle = ob.area();
            
            
            // this String.format("%.2f", Perimeter_Of_Triangle ) is used for precision  and will take only two decimal place of Perimeter_Of_Triangle 
            
            System.out.println("Perimeter of Triangle is : "+String.format("%.2f", Perimeter_Of_Triangle ));
            
            
            // this String.format("%.2f", Area_Of_Triangle  ) is used for precision  and will take only two decimal place of Area_Of_Triangle  
            
            
            System.out.println("Area of Triangle is : "+String.format("%.2f", Area_Of_Triangle ));
            
            
        }else{
            
            System.out.println("INVALID!!!");
            
        }
        
        
    
        
        
    }
    
    

    
    
}



