



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




run:
[x] 			  [e^x]
-10.0			1.342556137234173E-4
-9.0			1.2622023316151356E-4
-8.0			3.355216554362803E-4
-7.0			9.118827032332286E-4
-6.0			0.002478752181339452
-5.0			0.0067379469990957175
-4.0			0.0183156388887345
-3.0			0.04978706836786403
-2.0			0.13533528323661276
-1.0			0.36787944117144245
0.0			1.0
1.0			2.7182818284590455
2.0			7.389056098930649
3.0			20.08553692318766
4.0			54.598150033144265
5.0			148.41315910257654
6.0			403.42879349272846
7.0			1096.6331584273387
8.0			2980.957986946523
9.0			8103.083922752347
10.0			22026.465632423035
BUILD SUCCESSFUL (total time: 7 seconds)




