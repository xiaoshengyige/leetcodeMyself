'''java
public class Solution {
    public String reverseWords(String str) {
        	if ((str != null) && (str.trim() != "")) {
			String[] strs = str.split(" ");
	        StringBuffer stringBuffer = new StringBuffer();
	        
	        for (int i = 0; i < strs.length; i++) {
	        	stringBuffer.append(revereseSingleWord(strs[i]));
	        	if(i != strs.length -1)
	        	    stringBuffer.append(" ");
			}
	        return stringBuffer.toString();
		}
		
		return str;
    }
    private  String revereseSingleWord(String singleStr) {
		if (singleStr != null) {
			char[] strToChars = singleStr.toCharArray();
			char tmp = ' ';
			for (int i = 0; i < strToChars.length/2; i++) {
				tmp = strToChars[i];
				strToChars[i] = strToChars[strToChars.length -1 - i];
				strToChars[strToChars.length -1 - i] = tmp;
			}
			return  new String(strToChars);
		}
		return singleStr;
	}
}
'''
