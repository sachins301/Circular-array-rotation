#Circular-array-rotation

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        
        Scanner sc =new Scanner(System.in);
        int n=sc.nextInt();
        int[] a=new int[n];
        int k=sc.nextInt();
        int q=sc.nextInt();
        if(1<=n && n<=100000 && 1<=k && k<=100000 && 1<=q && q<=500)
            {
              for(int i=0;i<n;i++)
                  {
                  a[i]=sc.nextInt();
              }
            
            for(int j=0;j<k;j++)
                {
                int temp=a[n-1];
                for(int h=n-2;h>=0;h--)
                    {
                    a[h+1]=a[h];
                    
                }
                a[0]=temp;
            }
            int[] m=new int[q];
            for(int l=0;l<q;l++)
                {
                m[l]=sc.nextInt();
                
            }
            int l=0;
            for(l=0;l<q;l++)
                {int m1=m[l];
                System.out.println(a[m1]);
            }
        }
        
    }
}
