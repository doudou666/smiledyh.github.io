## 欢迎到蚂蚁CSDN博客

今天我给大家介绍的是[二分查找算法的实现和算法复杂度的介绍](https://github.com/doudou666/smiledyh.github.io/edit/master/binarySearch.md)

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```二分排序Java代码实现
public static int search(int[] arr, int num) {
		int l = 0;
		int r = arr.length - 1;
		int m = (l + r) >> 1;
		if (arr[m] == num) {
			return m;
		}
		while (l <= r) {
			if (arr[m] > num)
				r = m - 1;
			else
				l = m + 1;
			m = (l + r) >> 1;
		}
		if (arr[m] == num)
			return m;
		return -1;
}
```
### 特征：排好序---升序
### 时间复杂度:nlogn
```
arr=[0,1,5,9,13,25,28,33,46,49,56] 找出33
1步：将33与arr[11/2]比较，33>arr[11/2]
2步：在后半个数组中进行比较
重复步骤1和2最后找出33
```
