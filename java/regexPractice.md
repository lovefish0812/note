
#林魚魚練習
##正則表示式 字尾JAVA結束

``` java
import java.util.regex.Pattern;

public class practice05 {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
//		String MAIL_PATTERN = "^[\\w-]+JAVA";
//		String MAIL_PATTERN = "^[\\w\u4E00-\u9FA5\uF900-\uFA2D]+JAVA";
		String MAIL_PATTERN = ".*JAVA$";
		String[] email = {"saaa臭啊魚JAVA"};
		
		for(String mail: email){
			System.out.println(mail + " : " + Pattern.matches(MAIL_PATTERN, mail));
		}
		
	}

}
```









