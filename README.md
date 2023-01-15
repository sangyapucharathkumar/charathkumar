\\# charathkumar
\\addition or subtraction of two matrix
import java.util.*;
class matrix {
    public static void main (String[] args){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter first matrix number of rows:");
        int w=sc.nextInt();
        System.out.print("Enter first matrix number colums:");
        int x=sc.nextInt();
        int[][] Mat1=new int[w][x];
        for (int i=0;i<w;i++){
            for(int j=0;j<x;j++){
                Mat1[i][j]=sc.nextInt();
            }
        }
        System.out.println("your first matrix is:");
        for (int i=0;i<w;i++){
            for(int j=0;j<x;j++){
                System.out.print(Mat1[i][j]+"\t");
            }
            System.out.println();
        }
        System.out.print("Enter second matrix number of rows:");
        int y=sc.nextInt();
        System.out.print("Enter second matrix number colums:");
        int z=sc.nextInt();
        int[][] Mat2=new int[w][x];
        for (int i=0;i<y;i++){
            for(int j=0;j<z;j++){
                Mat2[i][j]=sc.nextInt();
            }
        }
        System.out.println("your second matrix is:");
        for (int i=0;i<y;i++){
            for(int j=0;j<z;j++){
                System.out.print(Mat2[i][j]+"\t");
            }
            System.out.println();
        }
        if(w==y||x==z){
            int[][] sol=new int [w][z];
            System.out.println("what opperation you want to do(for addition type'+'for subtraction type '-':)");
            char a=sc.next().charAt(0);
            if(a=='+'){
                for(int i=0;i<w;i++){
                    for(int j=0;j<x;j++){
                        sol[i][j]=Mat1[i][j]+Mat2[i][j];
                    }
                }
                for(int i=0;i<y;i++){
                    for(int j=0;j<z;j++){
                        System.out.print(sol[i][j]+"\t");    
                    }
                    System.out.println();
                }
            }
            else if(a=='-'){
                for(int i=0;i<w;i++){
                    for(int j=0;j<x;j++){
                        sol[i][j]=Mat1[i][j]-Mat2[i][j];
                    }
                }
                for(int i=0;i<y;i++){
                    for(int j=0;j<z;j++){
                        System.out.print(sol[i][j]+"\t");    
                    }
                    System.out.println();
                }
            }
            else{
                System.out.println("doesn't vallid");
            }
        }
        else{
            System.out.println("The matrix 1 rows or columes are not equal to matrix 2.");
        }
    }
}
