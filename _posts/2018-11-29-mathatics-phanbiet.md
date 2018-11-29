---
title:  Phân biệt Joint probability p(x,y) và conditional probability p(x|y).
date: 2018-11-29 10:24:06
categories:
- Mathematics
tags:
- Xác xuất
---
Điều tiên mình đến với định nghĩa:
	Xét hai biến ngẫu nhiên x và y. Ta quan sát được rất nhiều cặp của x và y là đầu vào. Sẽ có những cặp xuất hiện nhiều hơn những cặp khác. Thông tin được biểu diễn bằng một phân phối gọi là joint probability của x và y, được viết là p(x,y). Có thể hiểm nôm na là: p(x,y) là xác suất xảy ra x và y.

	Cũng xét 2 biến ngẫu nhiên x và y như trên, thì xác suất của biến ngẫu nhiên x biết rằng biến ngẫu nhiêu y có giá trị y* được gọi là xác suất của x với điều kiện cho trước của y = y*. Ký hiệu là p(x|y=y*) (đọc là probability of x give that y takes value y*). Có thể hiểu nôm na là p(x|y) là xác suất xảy ra của x khi y được cho trước một giá trị nào đó.

	Tới đây, mình cũng bắt đầu mơ hồ hiểu được, nên mình sẽ bắt đầu với những câu hỏi?

	Vậy p(x, y =y*) có bằng p (x|y = y*) không ?
	$\sum p(x,y = y*) bằng bao nhiêu?
	$\sum p(x|y = y*) bằng bao nhiêu
	Ở đây mình giả sử x,y là rời rạc (discrete)

Mình bắt đầu bằng 1 bài toán. Lớp học A có 2 loại học sinh là giỏi và khó, họ thi một tiêng anh và kết quả của họ như sau:

|Loại học sinh | Đậu | Rớt|
|--------------|-----|----|
| Giỏi| 4 | 2|
| Khá | 3 | 3

Nhìn vào bài toán dễ thấy. Lớp A có tổng cộng: 4 + 2 + 3 + 3 = 12 học sinh.
Gọi x là biến ngẫu nhiên của loại học sinh (giỏi, dốt)
	y là biến ngẫu nhiên của kết quả thi (đậu, rớt)

Dễ thấy p(x = giỏi, y = đậu) được hiểu là: xác suất để một học sinh vừa giỏi và đậu là: 4/12.
Vậy phải hiểu p(x, y = đậu) là gì: Theo mình đó là xác suất để một học sinh với biến x và đậu.

$\sum p(x,y = đậu) = p(x = giỏi, y = đậu) + p(x = khá, y = đậu) = 4/12+ 3/12 = 7/12
Tức là tổng số lượng số học sinh đậu chia cho số lượng học sinh.

Vậy p(x|y) sẽ được hiểu như thế nào ở đây?
Ví dụ: p(x | y= đậu) sẽ được hiểu là xác suất để một học sinh đó với biến x và biết rằng học sinh đó đậu.
Haha, theo mình thì nó hơi mơ hồ, nhưng mà bạn thử tìm nghĩ về không gian sự kiện của p(x, y= đậu) và p(x | y= đậu).
Ở p(x, y = đậu) không gian sự kiện là 12 = số học sinh trong lớp.
Ở p(x|y= đậu) không gian sự kiện là 7 = số học sinh đậu.

p(x = giỏi | y = đậu) = 4/7
p(x = khá | y = đậu) 3/7
$\sum p(x|y = y*) = 1 ( với p(x,y) thì tổng nó bằng 7/12)

Vậy p(x,y) và p(x|y) có 2 không gian sự kiện khác nhau, ta có thể biểu diễn chúng bằng 1 công thức không?. Câu trả lời là có.

Ví dụ p(x = giỏi | y = đậu) sẽ được hiểu là số lượng học sinh vừa giỏi vừa đậu chia cho số lượng học sinh đậu ( có cả khá và giỏi).

Cộng thức là p(x = giỏi | y = đậu) = (\frac {p(x = giỏi , y = đậu) * 12 } {p (x, y = đậu) * 12}) =  (\frac {p(x = giỏi , y = đậu) } {p (x, y = đậu)})

Tổng quát: p(x|y) = (\frac {p(x,y) * N } {p (y) * N}) = (\frac {p(x,y)} {p (y)})
Với N là không gian sự kiện