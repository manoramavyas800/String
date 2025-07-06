# String
//CHACK STRING IS PANAGRAM  (A pangram is a sentence containing every letter).
import java.util.Scanner;

public class CodeforcesQus {
    public static boolean isPanagram(String str) {
        // Check if given string is panagram
        int n = str.length();
        if (n < 26) {
            return false;
        }
            boolean[] chack = new boolean[26];
            for (int i = 0; i < n; i++) {
                char ch = str.charAt(i);
                if (ch >= 'a' && ch <= 'z') {
                    chack[ch - 'a'] = true;
                }
                if (ch >= 'A' && ch <= 'Z') {
                   chack[ch - 'A'] = true;
                }
            }
           for (int i = 0; i < 26; i++) {
           if (!chack[i]) {
           return false;
           }
           }
           return true;
    }


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str =sc.nextLine();
       System.out.println(isPanagram(str));
        }
    }
    //Find one extra character.
/*Time Complexity: O(n*log*n).
Auxiliary Space: O(n).*/

    import java.util.Arrays;
import java.util.Scanner;

public class CodeforcesQus {
    static char findex(String str,String str1){
       char[] a1=str1.toCharArray();
       char[] a2=str.toCharArray();
       Arrays.sort(a1);
       Arrays.sort(a2);
       int n=a1.length;
       for(int i=0;i<n;i++){
           if(a1[i]!=a2[i]){
               return a1[i];
           }

       }
       return a2[n];
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str =sc.nextLine();
        String str1 = sc.nextLine();
        System.out.println(findex(str,str1));

        }
    }
    //second method.
