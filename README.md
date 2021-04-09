



package Count;

public class Exponential {
    
    public static double exp(double power){
        
         
        //this is the answer which will be return in last after calculation 
        
        double answer = 1.0;
        
        // this is the first step in calculation
        
        double temp = 1.0;
        
        int accuracy = 32;
        
        
        
        for(int i=1; i<=accuracy; i++){
            
            
          temp = (temp*power)/i;
            
            
            answer = answer + temp ;
            
            
            
            
        }
        
        
        
        
        
        return answer;
        
        
    }
    
    public static void main(String[] args){
        
        
        
        System.out.println("[x] \t\t\t  [e^x]");
        
       for(double i = -10.0; i<=10.0; i++){
           
           
           double exponential = exp(i);
           
       System.out.println(i+"\t\t\t"+exponential);    
           
           
           
           
       } 
       
        
        
        
    }
    
}





[Output.txt](https://github.com/sajid-123/Test2/files/6283285/Output.txt)



