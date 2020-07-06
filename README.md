# Insertion-sort-in-java
in java

import java.util.*;
import java.io.*;
public class HelloWorld{

     public static void main(String []args)
     {
         Scanner sc=new Scanner(System.in);
         int n=sc.nextInt();
         int[] arr=new int[n];
         for(int i=0;i<n;i++)
         {
           arr[i]=sc.nextInt();   
        
         }
         int[] result=check(arr);
         for(int j=0;j<n;j++)
         {
         System.out.println(result[j]);
         }
        
     }
     static int[] check(int[] arr)
     {
        for(int i=1;i<arr.length;i++)
        {
            int key=arr[i];
            int j=i-1;
            while(j>=0 && arr[j]>key)
            {
                arr[j+1]=arr[j];
                j=j-1;
            }
            arr[j+1]=key;
        }
        return arr;
     }
}
