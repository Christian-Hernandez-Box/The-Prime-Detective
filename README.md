# The-Prime-Detective
Prime numbers are a fundamental concept in mathematics and are used in various applications, such as cryptography and data encryption. In this project, I will create a Java program that can determine if a number is prime or not, and then use this program to traverse through a list of numbers and create a new list with only prime numbers.
'''
// Importing the ArrayList Module and Creating the Prime Detective Class
import java.util.ArrayList;
class PrimeDirective {
  
  // Creating a Method That Determines if a Number is Prime
  public boolean isPrime(int number){
    
    if (number == 2){
      return true;
    } else if (number < 2){
      return false;
    }
    
    for (int i = 2; i < number; i++){
      if (number % i == 0){
        return false;
      } 
    }
    return true;
  }
  
  // Creating a Method That Sorts Through the List and Adds Prime Numbers Into its Own Array
  public ArrayList<Integer> onlyPrimes(int[] numbers){
    ArrayList<Integer> primes = new ArrayList<Integer>();

    for (int number : numbers){
      if (isPrime(number)){
        primes.add(number);
      }
    }
    return primes;
  }

  // Main Method; Initiating a New Instance of our Class and Testing the Methods we Created Above
  public static void main(String[] args) {

    PrimeDirective pd = new PrimeDirective();
    int[] numbers = {6, 29, 28, 33, 11, 100, 101, 43, 89};

    System.out.println(pd.isPrime(7));
    System.out.println(pd.isPrime(28));
    System.out.println(pd.isPrime(2));
    System.out.println(pd.isPrime(0));
    System.out.println(pd.onlyPrimes(numbers));

  }  

}
'''
Expected Output:
```
true
false
true
false
[29, 11, 101, 43, 89]
```
