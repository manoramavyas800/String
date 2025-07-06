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
