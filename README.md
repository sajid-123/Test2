


import java.util.*;
public class ArrayListWithDuplicates {
    
    public static void insertIntoSortedOrder(ArrayList<Integer> list, int number){
        
        
        
          
   System.out.println("Elements of Array before insertion : "+list);
       
   // coversion of premitive to Wrapper class object caue ArrayList only accepts objects     
   
   
   Integer num = number;
   
        for (int i = 0; i < list.size(); i++) {
        // if the element you are looking at is smaller than number, 
        // go to the next element
        if (list.get(i) < number)
        {
            continue;
            
        }
        // if the element equals number, return, because we don't add duplicates
        if (list.get(i) == number)
        {
            
             list.add(i, num);
            return;
            
        }
            
            
        // otherwise, we have found the location to add number
        list.add(i, num);
        return;
    }
    // we looked through all of the elements, and they were all
    // smaller than number, so we add number to the end of the list
    list.add(num);
    
    
   
    
     
    
}
        
        
    public static void main(String[] args){
        
        Scanner sc = new Scanner(System.in);
        
        
        
       // Creating Integer array instead of int array cause ArrayList only stores object and Integer is wrapper class object 
        
        Integer[] ar = {1,2,4,9,7,3,6,10,11};
        
        //converting array into Arraylist
        
        ArrayList<Integer> inputlist = new ArrayList<Integer>(Arrays.asList(ar));
        
        
        Collections.sort(inputlist);
        
        
        System.out.println("Sorted ArrayList is : "+ inputlist);
        
        
        
        String choice ="Yes";
        
        
        do{
            
            if(choice.equalsIgnoreCase("Yes")){
            
             System.out.println("Please enter the number to store in ArrayList : ");
        
            
             // here i'm pasring String into integer to avoid all kind of exception and errors cause we are taking diffrent ->
             
             //types of input from user 
             
            int number = Integer.parseInt(sc.nextLine());
            
            
            insertIntoSortedOrder(inputlist,number);
            
            
            
            // changes after insertion will reflect in input array so we can print it here 
            
            System.out.println("Elements of Array after insertion : "+inputlist);
            
            }  
            
             System.out.println("Do you want to add more elements  in ArrayList [Yes/NO]: ");
            
            
             choice = sc.nextLine();
            
            
        }while( !choice.equalsIgnoreCase("No"));
        
        
        
        
        
    }    
        
        
  
    
    
}




output on console :


run:
Sorted ArrayList is : [1, 2, 3, 4, 6, 7, 9, 10, 11]
Please enter the number to store in ArrayList : 
5
Elements of Array before insertion : [1, 2, 3, 4, 6, 7, 9, 10, 11]
Elements of Array after insertion : [1, 2, 3, 4, 5, 6, 7, 9, 10, 11]
Do you want to add more elements  in ArrayList [Yes/NO]: 
yes
Please enter the number to store in ArrayList : 
5
Elements of Array before insertion : [1, 2, 3, 4, 5, 6, 7, 9, 10, 11]
Elements of Array after insertion : [1, 2, 3, 4, 5, 5, 6, 7, 9, 10, 11]
Do you want to add more elements  in ArrayList [Yes/NO]: 
yes
Please enter the number to store in ArrayList : 
8
Elements of Array before insertion : [1, 2, 3, 4, 5, 5, 6, 7, 9, 10, 11]
Elements of Array after insertion : [1, 2, 3, 4, 5, 5, 6, 7, 8, 9, 10, 11]
Do you want to add more elements  in ArrayList [Yes/NO]: 
yes
Please enter the number to store in ArrayList : 
8
Elements of Array before insertion : [1, 2, 3, 4, 5, 5, 6, 7, 8, 9, 10, 11]
Elements of Array after insertion : [1, 2, 3, 4, 5, 5, 6, 7, 8, 8, 9, 10, 11]
Do you want to add more elements  in ArrayList [Yes/NO]: 
yes
Please enter the number to store in ArrayList : 
12
Elements of Array before insertion : [1, 2, 3, 4, 5, 5, 6, 7, 8, 8, 9, 10, 11]
Elements of Array after insertion : [1, 2, 3, 4, 5, 5, 6, 7, 8, 8, 9, 10, 11, 12]
Do you want to add more elements  in ArrayList [Yes/NO]: 
no
