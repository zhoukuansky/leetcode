# 出行计划
难度：	中等偏难   
题目地址：http://118.190.20.162/view.page?gpid=T142 
题目出处：  202203-2
完成时间：  2022/6/12   
# 题目

这里就不记录题目了。直接点击题目地址，可进入官网。

# 思路

**总体思路：**
+ 暴力解法：70分
+ 差分数组 + 前缀和： 100分

**过程：**    



# 代码  
java暴力解法（70分）：   
```
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		// 出行计划数目
		int n = sc.nextInt();
		// 查询个数
		int m = sc.nextInt();
		// 等待核酸检测结果所需时间
		int k = sc.nextInt();
		
		int[][] pos = new int[n][2];
		for (int i = 0; i < n; i++) {
			pos[i][0] = sc.nextInt();
			pos[i][1] = sc.nextInt();
		}
		
		int[] res = new int[m];
		for (int i = 0; i < m; i++) {
			// 核酸出结果的时间
			int time = k + sc.nextInt();
			for (int j = 0; j < n; j++) {
				if (time <= pos[j][0] && pos[j][0] - pos[j][1] < time) {
					res[i]++;
				}
			}
		}
		
		for (int i = 0; i < m; i++) {
			System.out.println(res[i]);
		}
		
	}

}
```
java差分数组+前缀和（100分）：   
```
import java.util.Scanner;

// 题目是CSP考试，202203-2，网址：http://118.190.20.162/view.page?gpid=T142
// 解法：差分数组 + 前缀和
public class Main {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int m = sc.nextInt();
		int k = sc.nextInt();
		int[] pos = new int[400002]; // 这里的取值只需要大于2*10^5即可
		// 计算差分数组
		for (int i = 0; i < n; i++) {
			int x = sc.nextInt();
			int y = sc.nextInt();

			// 满足条件的时间段的起始和结束地址
			int start = x - y - k + 1;
			int end = x - k + 1;
			if (start <= 0) {
				start = 0;
			}
			if (end <= 0) {
				end = 0;
			}
			// 起始地址+1
			pos[start]++;
			// 结束地址-1
			pos[end]--;
		}
		// 前缀和
		for (int i = 1; i < 400002; i++) {
			pos[i] = pos[i] + pos[i - 1];
		}
		
		int[] res = new int[m];
		for (int i = 0; i < m; i++) {
			res[i] = pos[sc.nextInt()];
		}
		for (int i = 0; i < m; i++) {
			System.out.println(res[i]);
		}
	}
}
```
# 其他



