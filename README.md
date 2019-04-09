import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int num = scan.nextInt();
        String s = String.valueOf(num);
        System.out.println(s.length());
        if(judgeNum(num)){
            System.out.println("Y");
        }else{
            System.out.println("N");
        }
    }

    public static boolean judgeNum(int num){
        String s = String.valueOf(num);
        int i,j;
        for (i=0, j=s.length()-1; i<j; i++,j--){
            if(s.charAt(i)!=s.charAt(j)){
//                System.out.println("N");
                return false;
            }
        }
        return true;
    }
}
