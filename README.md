# CountToSumK

import java.io.*; // for handling input/output
import java.util.*; // contains Collections framework

// don't change the name of this class
// you can add inner classes if needed
class Main {
	public static  int findPairsWithGivenSum(int[] arr,int n, int k){
	HashMap <Integer,Integer> hm = new HashMap<>();
	int count =0;
	for(int i=0;i<n;i++){
		if(hm.containsKey(arr[i])){
			hm.put(arr[i], hm.get(arr[i])+1);
		}
		else{
			hm.put(arr[i],1);
		}
	}
	//arr[i]=1,2,3,4,5,6 k=7-6=1
	for(int i=0;i<n;i++){
		int remSum=k-arr[i]
		if(hm.containsKey(remSum))
		   count++;	
	}
	count=count/2;
	}

	public static void main (String[] args) {
        Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int k = sc.nextInt();
		int arr [] = new int[n];
		for(int i=0;i<n;i++){
			arr[i] = sc.nextInt();
		}
		System.out.println(findPairsWithGivenSum(arr,n,k));
	}
}
