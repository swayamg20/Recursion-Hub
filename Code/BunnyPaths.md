---
Name: 'swayamg20'
Github: 'https://github.com/swayamg20'
WebSite: 'https://www.linkedin.com/in/ankitrao/'
Problem: 'Print all the possible paths to get to point n'
Description: 'There is a bunny which is standing at point 0,he wants to get to position n. At any given point, he can either jump 1 or 2 steps forward. Print all the possible ways to get to point n. '
Explanation: 'Same the Bubble Sort Algorithm But the Loop is being replaced By Recursion'
Language: 'c++' 
---

#include <stdio.h>

void bunny(int pos, int n, int a[], int count){
    int sum=0;
    if(pos>n)
        return;
    if(pos==n){
        a[count] = pos;
        count++;
        for(int i=0;i<count;++i)
            sum+=a[i];
        printf("%d", sum);
        return;
    }
    a[count] = pos;
    bunny(pos+1, n, a, count+1);
    bunny(pos+2, n, a, count+1);
}
int main(){
    int n;
    scanf("%d",&n);
    int a[50];
    bunny(0, n, a, 0);
    return 0;
}

#include <stdio.h>
int count(int n){
// add code for recursive function here
int tag=0;

}
int main() {
// scan input and call the function
   int n, val;
   scanf("%d", &n);
   val=count(n);
   printf("%d", val);
   return 0;
}