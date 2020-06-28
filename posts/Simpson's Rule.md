---
layout: page
title: Posts
tagline: 
permalink: /posts/simpsonrule.html
ref: posts
order: 2
---

## Quy tắc Simpson tìm giá trị gần đúng của tích phân.

* **1. Quy tắc Simpson**

 - Quy tắc Simpson là quy tắc dùng để tính xấp xỉ tích phân xác định dựa vào việc thiết lập các phương trình bậc cao.
 - Quy tắc này dựa vào một tính chất, đó là ta có thể thiết lập một phương trình bậc cao dựa vào những điểm cho trước (từ đó giải hệ phương trình đa ẩn).                 
 - Để tính giá trị của ∫f(x)dx trong khoảng từ [a,b], ta sẽ chia [a,b] thành n khoảng bằng nhau (n là số chẵn), mỗi khoảng có chiều dài Δx = (b-a)/n.                   
 * **Quy tắc Simpson 1/3:** 
 - Quy tắc này dựa trên công thức gốc của Quy tắc Simpson. Quy tắc này dễ nhận thấy trong các bài toán về kinh tế, khi chúng ta chưa có hàm f(x) cụ thể để tính xấp xỉ như trong công thức gốc, thay vào đó ta có các bảng số liệu cho sẵn. 
 - Công thức của quy tắc Simpson 1/3 như sau: 
 
 <p align = "center">
  <img src = "https://user-images.githubusercontent.com/51883796/85844625-385cb580-b7cd-11ea-808e-5ee0438ef324.PNG">
 </p>

* **Quy tắc Simpson 3/8:**
- Đây là một biến thể của Simpson 1/3 với độ chính xác cao hơn. Đối với Simpson 1/3 thì dựa trên phép nội suy bậc 2, còn Simpson 3/8 thì dựa trên phép nội suy bậc 3. Chính vì vậy, có một yêu cầu bắt buộc của phương pháp này, đó là n phải là một số chia hết cho 3 (bội số của 3).
- Công thức của quy tắc Simpson 3/8 như sau: 

<p align = "center">
 <img src = "https://user-images.githubusercontent.com/51883796/85950878-9cc47400-b989-11ea-98f0-809806bcb8ff.PNG">
</p>

Hoặc: 

<p align = "center">
 <img src = "https://user-images.githubusercontent.com/51883796/85951796-ad77e880-b98f-11ea-83a6-c2b144779729.PNG">
</p>

Nhìn công thức thì rõ luộm thuộm, thôi thì ta đi vào thẳng ví dụ luôn cho dễ.

* **2. Ví dụ minh họa:**

Anh lấy luôn bài của các em nhé.

Cho bảng số liệu sau: 

<p align = "center">
 <img src = "https://user-images.githubusercontent.com/51883796/85950993-59b6d080-b98a-11ea-8188-5cb4fb2a7d36.PNG">
</p>.

Theo đề của các em là tính xấp xỉ giá trị thặng dư khi q =24 dựa vào bảng số liệu này, sử dùng công thức Simpson. Đối với những gì anh tìm hiểu được thì cái thặng dư đó chính là diện tích phần anh đánh dấu màu đỏ này. 

<p align = "center">
 <img src = "https://user-images.githubusercontent.com/51883796/85951054-c8942980-b98a-11ea-9984-569a9c4d8789.png">
</p>

Vậy ha, okay tính toán thôi. Để cho thống nhất, anh sẽ kí hiệu từ trái qua phải lần lượt là [q1....q7] và [p1...p7] nhé.

Đầu tiên, tìm n. Vì cả Simpson 1/3 lẫn 3/8 đều yêu cầu tìm n nên ta tính chung luôn. Đọc lại lý thuyết, ta thấy trong bảng số liệu này, n = 6, tương ứng với việc ta chia đoạn [0,24] thành 6 khoảng, mỗi khoảng cách nhau 4 đơn vị. Từ đó ta suy ra được Δx = 4 (có thể kí hiệu là h = 4) (mà bản chất Δx chính là khoảng cách giữa 2 giá trị x liên tiếp nhau trong bảng số liệu, các em nhớ để tính cho nhanh).

Chúng ta đã có n = 6, và dễ thấy, 6 chia hết cho 3, vì vậy ta có thể sử dụng cả công thức Simpson 1/3 lẫn 3/8 đều được. 

* a. Sử dụng Simpson 1/3.

Dựa vào công thức ở trên, ta sẽ tính thặng dư khi q = 24 dựa vào Simpson 1/3 như sau: 

sum (consumer's surplus) = (h/3) * (p1 + 4*p2 + 2*p3 + 4*p4 + 2*p5 + 4*p6 +p7) = 4/3 * (49.12 + 4* 42.9 + 2* 31.32 + 4* 19.83 + 2* 13.87 + 4* 10.58 + 7.25) = 586.65

Dễ thấy, ứng với q = 2,4,6,... thì ta nhân 4 rồi cộng lại, với q = 3,5,... thì ta nhân 2 rồi cộng lại, q đầu tiên và q cuối cùng ta không nhân với gì cả, để nguyên thôi. Vậy là xong Simpson 1/3 rồi nhé. 

* b. Sử dụng Simpson 3/8.

Công thức ở trên nhìn rõ kinh khủng, nhưng khi viết ra thì cũng tương tự như Simpson 1/3 thôi nên đừng hoảng loạn =))

sum (consumer's surplus) = (3*h/8) * (p1 + 3*p2 + 3*p3 + 2*p4 + 3*p5 + 3*p6 +p7) = 3/2 * (49.12 + 3* 42.9 + 3* 31.32 + 2* 19.83 + 3* 13.87 + 3* 10.58 + 7.25) = 588.06

Hơi rắc rối tí nhỉ, okay để tóm gọn thì ta sẽ quy định như thế này, 
- Ứng với p2, p5, p8, ... thì ta lấy 3 * (p(i) + p(i+1)). Ví dụ trong bảng trên ta có: p2 = 42.9 => p3 = 31.32 thì ta lấy 3*(p2 + p3), tiếp theo ta có p5 = 13.87 => p6 = 10.58, ta lấy 3*(p5 + p6). Ta tính tất cả các tổng con như vậy rồi sau đó cộng hết lại, ra được 1 tổng lớn. 
- Đối với p4, p7, p10 thì ta chỉ lấy 2 nhân vô cái giá trị đó thôi, không cộng thêm bớt gì hết. Ví dụ trong bảng chỉ có p4 thì ta chỉ cần lấy 2*p4 là xong. 
- Ở đây do p7 là giá trị cuối nên tương tự Simpson 1/3, ta không nhân bất cứ thứ gì hết, để nguyên đó và cộng lại với p1, là xong. Nếu trong bảng có nhiều hơn 7 giá trị thì p7 sẽ được đưa lên ý số 2 nhé. 
Okay xong rồi. 

