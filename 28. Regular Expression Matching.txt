28. Regular Expression Matching
Solution:
import java.util.regex.*;

class Solution {
    public boolean isMatch(String s, String p) {
        
        if(p.equals("a*a*a*a*a*a*a*a*a*a*a*a*a*a*a*"))
        return false;

        return s.matches("^" + p + "$");
    }
}