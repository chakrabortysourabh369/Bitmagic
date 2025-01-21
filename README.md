# Bitmagic
All the concepts of Bitmanipulation

/* 
import java.io.*;
public class bitmagic {
public static void main(String args[]){
    int x=6;
    System.out.println(~x);
}
    
}

//1. kth bit as set(optimised,loop naive approach)..............

import java.io.*;
public class bitmagic{
    //without loop (using left shift operator)
    public static boolean isset1(int n,int k){
        int x=(1<<(k-1));
        if((n&x)!=0){
            return true;
        }
        return false;
    }
    public static boolean isset(int n,int k){

        int x=1;
        for(int i=0;i<(k-1);i++){
            x=2*x;
        }
        if((n&x)!=0){
            return true;
        }
        return false;
    }
    public static void main(String args[]){
        int n=6;
        int k=2;
       System.out.println(isset1(n,k));
    }
}

     //3.Number of set bits(brian kerningams algo)

      import java.util.*;
      public class bitmagic{

        public static int setbits(int n){
            int res=0;
            while(n>0){
                n=n & (n-1);   
                res++;
            }
            return res;
        }
      public static void main(String args[]){

        int n=39;
        System.out.println(setbits(n));
      }
    }
      

      //3.IS Number power of two?
      
      import java.util.*;
      public class bitmagic{

        public static boolean poweroftwo(int n){
            if(n==0){
                return false;
            }
            return ((n&(n-1))==0);
        }
      public static void main(String args[]){

        int n=8;
        System.out.println(poweroftwo(n));
      }
    }
      
      
      //4. odd occuring number(Naive approach,optimised approach)
      import java.util.*;
      public class bitmagic{
        //optimised(O(n))
        public static int oddoccurrence1(int arr[]){

            int res=arr[0];
            for(int i=1;i<arr.length;i++){
                res=res^arr[i];
            }
            return res;
        }
        public static int oddoccurrence(int arr[]){

            for(int i=0;i<arr.length;i++)
            {
                int count=0;
                for(int j=0;j<arr.length;j++){
                    if(arr[i]==arr[j])
                        count++;
                    }
                    if(count%2!=0)
                        return arr[i];
            }
            return 0;  
            }   
        public static void main(String args[]){
 
            int arr[]={7,7,3,7,7,3,3};
            //System.out.println(oddoccurrence(arr))
            System.out.println(oddoccurrence1(arr));
        }
      }

      //6.power set using bitwise

      import java.util.*;
      public class bitmagic{
        public static void powerset(String str){
            int n=str.length();
            int ss=(1<<n);

            for(int i=0;i<ss;i++)
            {
                for(int j=0;j<n;j++){
                    if((i &(1<<j))!=0)
                       System.out.print(str.charAt(j));
                }
                System.out.println();
            }
        }
        public static void main(String args[]){
            String str="abc";
            powerset(str);
        }
      }*/
