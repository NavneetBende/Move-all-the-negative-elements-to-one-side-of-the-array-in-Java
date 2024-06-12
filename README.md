Move all negative elements to one side of the array  in Java
Here, in this page we will discuss the program to move all negative elements to one side of the array in Java . We use the concept of two pointers to do so . We are giving with the size of the array along with array elements.We have to print array as desired

Move all negative elements to one side
Algorithm :
Let ‘j’ point to the leftmost positive element in the array. Initially, we set ‘j’ to point to the first element.
Iterate over the array:
Let ‘i’ be the index of the current element.
If the current element is negative:
If ‘i’ not equal to ‘j’, then swap the ith and jth elements.
Increment ‘j’ by 1.
Return the resulting array
Java Code
Run

import java.util.*;
public
class Main {
    public
    static void shift(int[] arr) {
        int j = 0;
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] < 0) {
                if (i != j) swap(arr, i, j);
                j++;
            }
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }
    // used for swapping ith and jth elements of array
    public
    static void swap(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
    public
    static void main(String[] args) throws Exception {
        

        int[] arr = new int[]{ -1,0,3,1,-4}; 
       
        shift(arr);
    }
}
Output :
-1 -2 4 2 2
Login/Signup to comment


mstofficial19
public static void move(int arr[]){
int i=0;
int k=arr.length-1;
while(i<k){
if(arr[i]=0){
int temp=arr[k];
arr[k]=arr[i];
arr[i]=temp;
i++;
k–;
}

else if(arr[i]>=0&&arr[k]<0){
i++;
k–;
}
else if(arr[i]<0&&arr[k]=0&&arr[k]>=0){
i++;

}

}
for(int j=0;j<arr.length;j++){
System.out.print(arr[j]+" ");
}
}

Log in to Reply

PrepInsta Support
Hey there, Thanks for commenting , Kindly join our Discord for all the subject and technical queries.

Log in to Reply

SIVALI
import java.util.*;

public class Main
{
//P N -> SWAP and increment (l++ and r–)
// N P -> INCREMENT(L++ , R++)
//N N -> L++
//P P -> R–

static void negative(int n , int[] a ){
int l = 0 ;
int r = n-1 ;

while(l 0 && a[r] < 0) {
int temp = a[l] ;
a[l] = a[r] ;
a[r] = temp ;
l++ ;
r– ;
}
else if(a[l] 0) {
l++;
r– ;
}
else if(a[l] < 0 && a[r] <0){
l++ ;
}
else{
r– ;
}

}

System.out.println("array is ") ;
//for loop to print array
for(int i=0 ; i<n ; i++){
System.out.println(a[i]) ;
}
}

public static void main(String[] args) {
Scanner sc = new Scanner(System.in) ;
System.out.println("enter size") ;
int n = sc.nextInt() ;
int[] a = new int[n] ;
for(int i=0 ; i<n ; i++){
a[i] = sc.nextInt() ;
}

negative(n,a) ;

}
}

Log in to Reply

PrepInsta Support
Kindly drop your technical queries on discord: Discord

Log in to Reply

Gyanendra
import java.util.*;
public class Main{
public static void main(String[] args){
Scanner scn=new Scanner(System.in);
int n=scn.nextInt();
int[] arr=new int[n];

for(int i=0;i<n;i++){
arr[i]=scn.nextInt();
}

int i=0,j=0;

while(j<arr.length){
if(arr[j]<0){
int temp=arr[i];
arr[i]=arr[j];
arr[j]=temp;
i++;
j++;
}
else{
j++;
}
}

for(int temp: arr){
System.out.print(temp+" ");
}
}
}

Log in to Reply

Shyam
public class Shiftallnegative_to_inthe_last {
public static void shift(int[] arr) {
int a[] = new int[arr.length];
int j = 0;
for (int i = 0; i 0) {
a[j] = arr[i];
j++;
}
}
for (int i = 0; i < arr.length; i++) {
if (arr[i] <= 0) {
a[j]=arr[i];
j++;
}
}
for(int k=0;k<a.length;k++){
System.out.println(a[k]);
}

}

public static void swap(int []arr,int i,int j){
int temp=arr[i];
arr[i]=arr[j];
arr[j]=temp;
}

public static void main(String[] args) {
int a[]={-1,9,6,-2,-3,3};
shift(a);

}
}
