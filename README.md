
package test2;
import java.util.*;
public class Occurence {
    
    public static void countNumberOfOccurences(){
        
        Map<Integer,Integer> map = new HashMap<>();
       
        Scanner sc = new Scanner(System.in);
        
        System.out.println("Please Enter the Integer Numbers");
        
        int number = sc.nextInt();
        
        while(number != 0){
            
            if(map.containsKey(number)){
                
                // map.get(key) will extract the value stored with respect to key
                
                
                map.put(number, (map.get(number)+1));
                
            }else{
                
                map.put(number, 1);
                
            }
          
            
            number = sc.nextInt();
        }
        
        
     
         // storing all values  in ArrayList
       
     
      
      ArrayList<Integer> values = new ArrayList<>();
        
      
        for(Map.Entry<Integer,Integer> access : map.entrySet()){
            
        
          
          values.add(access.getValue());
            
            
        }
        
       
      int max = Collections.max(values);
      
       for(Map.Entry<Integer,Integer> access : map.entrySet()){
            
        if(max == access.getValue())
          
          System.out.println("Maximum Occurences of  : "+access.getKey()+" : frequency -> "+max);
            
            
        }
        
      
        
        
        
        
        
    }
 public static void main(String[] args){
     
     
      countNumberOfOccurences();  // calling method
     
 }   
    
}
