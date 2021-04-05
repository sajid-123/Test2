  


package Math;

import java.util.HashMap;
import java.util.Scanner;


public class Cryptography {
  
    public static HashMap<Character,Integer> map=new HashMap<>(); 
    
     public static HashMap<Integer,Character> map1=new HashMap<>();
    
    
    public static String encrypt(String message, int key){
        
        String upperCaseMsg = message.toUpperCase();
        
        String encryptedMsg = "";
        
		// this map will store integer value corresponding to Capital letttes

       map=new HashMap<>(); //Substitution Algorithm is used for Encryption

        map.put('A',1);
        map.put('B',2);
        map.put('C',3);
        map.put('D',4);
        map.put('E',5);
        map.put('F',6);
        map.put('G',7);
        map.put('H',8);
        map.put('I',9);
        map.put('J',10);
        map.put('K',11);
        map.put('L',12);
        map.put('M',13);
        map.put('N',14);
        map.put('O',15);
        map.put('P',16);
        map.put('Q',17);
        map.put('R',18);
        map.put('S',19); 
        map.put('T',20);
        map.put('U',21);
        map.put('V',22);
        map.put('W',23);
        map.put('X',24);
        map.put('Y',25);
        map.put('Z',26);

        
        
        
        
     // this map will provide capital letters according to it's integer value    
         
       map1=new HashMap<>();
    
        map1.put(1,'A');
        map1.put(2,'B');
        map1.put(3,'C');
        map1.put(4,'D');
        map1.put(5,'E');
        map1.put(6,'F');
        map1.put(7,'G');
        map1.put(8,'H');
        map1.put(9,'I');
        map1.put(10,'J');
        map1.put(11,'K');
        map1.put(12,'L');
        map1.put(13,'M');
        map1.put(14,'N');
        map1.put(15,'O');
        map1.put(16,'P');
        map1.put(17,'Q');
        map1.put(18,'R');
        map1.put(19,'S'); 
        map1.put(20,'T');
        map1.put(21,'U');
        map1.put(22,'V');
        map1.put(23,'W');
        map1.put(24,'X');
        map1.put(25,'Y');
        map1.put(26,'Z');
        
        
        
        
        for(int i=0; i<upperCaseMsg.length(); i++){
       
            
            char c = upperCaseMsg.charAt(i);
        
            if( c <= 'Z' && c >= 'A'){
                
                int val = map.get(c);
                
                int newValue = val + key;
                
                if(newValue > 26){
                    
                    
                    newValue = newValue%26;
                    
                    encryptedMsg =  encryptedMsg + map1.get(newValue);
                    
                }else{
                    
                     encryptedMsg =  encryptedMsg + map1.get(newValue); 
                   
                }
                
                
            }else{
                
                encryptedMsg =  encryptedMsg + c; 
                
                
            }
        
        
        }
        
        return encryptedMsg;
    }
    public static String decrypt(String message,int key){
        
        String decryptMsg = "";
        
        for(int i=0; i<message.length(); i++){
       
            
            char c = message.charAt(i);
        
            if( c <= 'Z' && c >= 'A'){
                
                int val = map.get(c);
                
                int newValue = val - key;
                
                if(newValue < 0){
                    
                    
                    newValue = newValue+26;
                    
                    decryptMsg  =  decryptMsg  + map1.get(newValue);
                    
                }else{
                    
                     decryptMsg  =  decryptMsg  + map1.get(newValue); 
                   
                }
                
                
            }else{
                
                decryptMsg  =  decryptMsg  + c; 
                
                
            }
        
        
        }
        
        
        
        
        
        
        
        
        return decryptMsg ;
    }
    public static void run(Scanner sc){
        
        
        System.out.println("How many times you want to use the app :");
        
        int number = Integer.parseInt(sc.nextLine());
        
        for(int i=0; i<number; i++){
            
            System.out.print("your message :");
            
            String PlaneText = sc.nextLine();
            
            System.out.print("Encoding key :");
            
            int key =  Integer.parseInt(sc.nextLine());
            
            String encrypted = encrypt(PlaneText,key);
            
            
            
            System.out.println("The encrypted message is  :");
            
            System.out.println(encrypted);
            
            
           System.out.println("The decrypted message is  :");
              
            String decrypted = decrypt(encrypted,key);
            
            
             System.out.println(decrypted);
            
            
        }
        
        
        
        
        
        
    }
  
    public static void main(String[] args){
        
        Scanner input = new Scanner(System.in);
        
        run(input);
        
        
        
        
        
    }
    
    
    
    
}





//output on console :


run:
How many times you want to use the app :
4
your message :i love java programming
Encoding key :5
The encrypted message is  :
N QTAJ OFAF UWTLWFRRNSL
The decrypted message is  :
I LOVE JAVA PROGRAMMING
your message :i will see you at the movie theater
Encoding key :7
The encrypted message is  :
P DPSS ZLL FVB HA AOL TVCPL AOLHALY
The decrypted message is  :
I WILL SEE YOU AT THE MOVIE THEATER
your message :my password if ertudfg
Encoding key :8
The encrypted message is  :
UG XIAAEWZL QN MZBCLNO
The decrypted message is  :
MY PASSWORD IF ERTUDFG
your message :i have to go home
Encoding key :12
The encrypted message is  :
U TMHQ FA SA TAYQ
The decrypted message is  :
I HAVE TO GO HOME
BUILD SUCCESSFUL (total time: 3 minutes 11 seconds)
