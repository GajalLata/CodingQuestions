#Spiral Matrix Print
import java.util.ArrayList;
public class Solution {
    public static ArrayList<Integer> spiralPathMatrix(int[][] a, int m ,int n){
         ArrayList<Integer> list=new  ArrayList<>();
//         int row=a.length;
//         int col=a[0].length;
       int s_row=0;
        int e_row=m-1;
        int s_col=0;
        int e_col=n-1;
        
        int cnt=0;
        int total=m*n;
        while(cnt<total)
        //for start row
        {
            for(int j=s_col;cnt<total && j<=e_col;j++){
list.add(a[s_row][j]); 
                 cnt++;
            }
        s_row++;
        
        //for end col
        for(int i=s_row;cnt<total && i<=e_row;i++){
            list.add(a[i][e_col]); 
            cnt++;
        }
        e_col--;
        
        
        //for end row
        for(int j=e_col;cnt<total && j>=s_col;j--){
            list.add(a[e_row][j]);
             cnt++;
        }
        e_row--;
        
        
        //for start col
        for(int i=e_row;cnt<total && i>=s_row;i--){
            list.add(a[i][s_col]);
            cnt++;
        }
        s_col++;
        
        }
        return list;
    }
}
