import java.rmi.AlreadyBoundException;
import java.util.Random;
import java.util.Scanner;

public class NNN{
	

	public static void main(String[] args) {
		System.out.println("welcome to hacker game");
		System.out.println("should we strat");
	  
		
		System.out.println("1.yes");
		System.out.println("2.no");
		
		Scanner sc=new Scanner(System.in);
		 int a=sc.nextInt();
		 
		 while(a!=1) {
                System.out.println("Shall we start ?");
				System.out.println("1.yes");
				System.out.println("2.no");
				
				 a =sc.nextInt();
		
		 }
		Random random=new Random();
		int x=random.nextInt(20);
		System.out.println("please guess a number: ");
		int guess=sc.nextInt();
		
	     int timeperiod=0;
	     boolean haswon=false;
	     boolean shouldfinished=false;
	    while(!shouldfinished) { 
	    	
	    timeperiod++;
	     if(timeperiod<5) {
	    	 if(guess==x) {
	    		 haswon=true;
	    	 }
	    	 else if(guess<x){
	    		 System.out.println("guess some higher value");
	    		 guess=sc.nextInt();
	    		
	    		 
	    	 }
	    	 else{
	    		 System.out.println("gues some lower value");
	             guess=sc.nextInt();
	    	 }
	    
	     }
	     else {
	    	 shouldfinished=true;
	     }
		
	    }
	    if(haswon) {
	    	System.out.println("WON THE GAME In "+x+ " guess");
	    	
	    }
	    else {
	    	System.out.println("Game over");
	    	System.out.println("try some next-time"+x);
	    }
	}
}
