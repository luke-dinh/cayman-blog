---
layout: page
title: Posts
tagline: 
permalink: /posts/DeepLearning.html
ref: posts
order: 1
---

## Những kiến thức cơ bản về Deep Learning - Phần 1

* **Lời nói đầu**: Bản thân mình mong muốn được chia sẻ những gì mình biết về AI - ML - DL đến cho mọi người như là một cách để ôn lại kiến thức, nên mình viết blog bằng tiếng Việt để lưu giữ lại kiến thức mình học được. Okay bắt đầu nào.

* **1. Nơ ron (neural): Cảm hứng của tất cả**

<p align= "center">
  <img src = "https://user-images.githubusercontent.com/51883796/81307449-e17b0f80-90aa-11ea-935f-727253705a11.png">
</p>

Nơ ron (neural) có lẽ là một khái niệm quen thuộc đối với tất cả mọi người. Trong môn Sinh học lớp 8 thì cũng đã đề cập đến nó. Đây là đơn vị cấu tạo cơ bản của hệ thống thần kinh và là phần quan trọng của não bộ. Não chúng ta gồm khoảng 10 triệu nơ-ron và mỗi nơ-ron liên kết với 10.000 nơ-ron khác. Ở mỗi nơ-ron có phần thân (soma) chứa nhân, các tín hiệu đầu vào qua sợi nhánh (dendrites) và các tín hiệu đầu ra qua sợi trục (axon) kết nối với các nơ-ron khác. Hiểu đơn giản mỗi nơ-ron nhận dữ liệu đầu vào qua sợi nhánh và truyền dữ liệu đầu ra qua sợi trục, đến các sợi nhánh của các nơ-ron khác. Mỗi nơ-ron nhận xung điện từ các nơ-ron khác qua sợi nhánh. Nếu các xung điện này đủ lớn để kích hoạt nơ-ron, thì tín hiệu này đi qua sợi trục đến các sợi nhánh của các nơ-ron khác. => Ở mỗi nơ-ron cần quyết định có kích hoạt nơ-ron đấy hay không.

* **2. Mạng Nơ ron nhân tạo (Artificial Neural Network - ANN)**

Đây chính là lí thuyết tiền đề cho kỹ thuật Deep Learning

<p align= "center">
  <img src = "https://user-images.githubusercontent.com/51883796/81303503-f7d29c80-90a5-11ea-811b-adc39c8902db.png">
</p>

Hình trên mô tả tổng quát một ANN. Đây được gọi là Fully Connected Network - FCN

Lớp đầu tiên được gọi là Input layer, các lớp ở giữa được gọi là Hidden Layer(s), lớp cuối cùng được gọi là Output layer. Một mạng nơ ron bắt buộc phải có Input layer và Output Layer, tuy nhiên có thể có hoặc không có Hidden Layer(s). (Trong trường hợp không có lớp ẩn nào, mạng nơ ron lúc này sẽ được gọi là Perceptron). 

Các hình tròn trong hình được gọi là các node hoặc là neural. Các node trong hidden layer và output layer:

- Liên kết với tất cả các node ở layer trước đó với các hệ số w riêng.

- Mỗi node có một hệ số bias b riêng.

- Diễn ra hai quá trình: tính tổng linear và đi qua hàm activation (hàm kích hoạt) trước khi qua layer tiếp theo.

Ở đây ta thấy có thắc mắc: Hệ số bias dùng để làm gì? Như đã đề cập ở trên, các node sẽ phải trải qua quá trình tính tổng linear. Nếu không thêm hệ số bias thì tổng linear sẽ có dạng y = a*x luôn đi qua gốc tọa độ và không tổng quát hóa được phương trình đường thẳng và có thể không tìm được phương trình mong muốn. Vì vậy hệ số bias rất quan trọng.

* **3. Các bước để làm bài toán Deep Learning là gì?**

1. Xử lý data: chia dữ liệu thành các tập train, validation, test (thông thường thì tỉ lệ sẽ là 60-20-20).

2. Thiết lập model, networks.

3. Tính toán hàm mất mát (loss function).

4. Tìm tham số bằng cách tối ưu hàm loss function, trong đó cố gắng chọn learning rate phù hợp.

5. Dự đoán dữ liệu test bằng model vừa train xong.

* **4. Hàm mất mát (loss function) là gì?**

Loss function hay còn gọi là hàm mất mát, thể hiện một mối quan hệ giữa y* (thông thường trong các sách người ta gọi là y hat, là chữ y có dấu mũ ^ ngay trên đầu, là kết quả dự đoán của model) và y (là giá trị thực tế). Ví dụ ta có hàm loss như sau: f(y) = (y* - y)^2. Khi đó người ta đưa vào hàm loss function này mục đích là để tối ưu model của mình sao cho tốt nhất, hay cũng dùng để đánh giá độ tốt của model , y* (là kết quả dự đoán của model) càng gần y (là giá trị thực tế) thì càng tốt. Tức là dựa vào loss function, khi đó chúng ta có thể tính ra gradient descent để tối ưu loss function càng về gần 0 càng tốt.

* **5. Activation function (Hàm kích hoạt)**

Hàm kích hoạt là những hàm phi tuyến, được đặt tại ngõ ra của neural trong các lớp ẩn của mô hình mạng, có nhiệm vụ chuẩn hóa output của neural để từ đó sử dụng làm input của lớp ẩn tiếp theo. Hàm kích hoạt mô phỏng tỉ lệ truyền xung qua axon của một neural thần kinh.

<p align= "center">
  <img src = "https://user-images.githubusercontent.com/51883796/81408541-9bd04c80-9167-11ea-86ac-36ebba940b8a.png">
</p>

Hình trên mô phỏng cấu trúc bên trong một neural trong mạng ANN. Ta có thể thấy sau khi tính tổng linear thì sẽ qua hàm kích hoạt trước khi trở thành input cho lớp ẩn tiếp theo.

Giống như trong mô hình sinh học, các xung thần kinh được truyền qua axon với một tỷ lệ nào đó. Ở mô hình học máy mô phỏng chúng ta xây dựng, các hàm kích hoạt sẽ điều chỉnh tỷ lệ truyền này. Các hàm này thường là các hàm phi tuyến.

Tại sao phải có hàm kích hoạt? Và tại sao các hàm kích hoạt là hàm phi tuyến?

1. Nếu không có hàm kích hoạt, thì output của lớp ẩn này, khi trở thành input của lớp ẩn kế tiếp thì việc này không khác gì chúng ta thêm một tầng ẩn nữa vì phép biến đổi cũng chỉ đơn thuần là nhân đầu ra với các weights. Với chỉ những phép tính đơn thuần như vậy, trên thực tế mạng neural sẽ không thể phát hiện ra những quan hệ phức tạp của dữ liệu. Vì vậy sự kết hợp của các activation functions giữa các tầng ẩn là để giúp mô hình học được các quan hệ phi tuyến phức tạp tiềm ẩn trong dữ liệu.

2. Hàm kích hoạt là một hàm phi tuyến vì nếu không, một lớp ẩn hay nhiều lớp ẩn cũng sẽ giống như nhau. Ví dụ ta có hình sau:

<p align= "center">
  <img src = "https://user-images.githubusercontent.com/51883796/81410216-91638200-916a-11ea-9665-09c9e3a88253.png">
</p>

Nếu activation function là một hàm linear (giả sử hàm f(s) = s) thì cả hai layer có thể được thay bằng một layer với ma trận hệ số W = W1*W2 (tạm bỏ qua hệ số bias)

* **6. Gradient Descent**

1. Đạo hàm: là sự biến đổi của của hàm số hay còn gọi là độ dốc của đồ thị. Ví dụ : f(x) = x^2 +1 . Khi đó f'(x) = 2x. Ở đây, với x =1 thì f'(x) = 2, với x =2 thì f'(x)=4. Ta thấy x càng tăng thì f'(x) càng tăng, hay giá trị của hàm số sẽ càng tăng. Một cách hiểu khác là hàm số f(x) sẽ càng tăng lên khi x tăng từ 1 lên.

2. Đạo hàm riêng: Khi mà hàm số có nhiều biến hơn 1. Ví dụ như f(x,y) = 2x+3y thì khi đó khái niệm đạo hàm riêng sẽ ra đời. Ở đây sẽ phân ra 2 khái niệm là đạo hàm riêng trên x, và đạo hàm riêng trên y. Đạo hàm riêng trên x, sẽ muốn xem x nó ảnh hưởng thế nào đến f(x,y). Đạo hàm riêng trên y, sẽ muốn xem y ảnh hưởng thế nào đến f(x,y).

3. Gradient Descent: Về bản chất thì nó là một thuật toán giúp việc tìm giá trị nhỏ nhất của hàm số, ví dụ f(x) dựa trên đạo hàm, hoặc f(x,y,...) dựa trên đạo hàm riêng của từng biến. Ví dụ : với f(x) = x^2 +1 => f'(x) = 2x. Ta sẽ thực hiện các bước như sau để tìm giá trị nhỏ nhất của f(x):

- Khởi tạo giá trị x = x0 tùy ý

- Gán x = x0 - (learning rate)*f'(x) (learning rate là một hẳng số không âm, có thể hiểu đây là "khoảng cách" giữa hai lần "học" (gradient descent) liên tiếp nhau)

- Tính lại f(x): Nếu f(x) đủ nhỏ thì dừng lại, ngược lại tiếp tục bước 2

Việc chọn learning rate rất quan trọng, vì: 
- Nếu learning_rate nhỏ: mỗi lần hàm số giảm rất ít nên cần rất nhiều lần thực hiện bước 2 để hàm số đạt giá trị nhỏ nhất.

- Nếu learning_rate hợp lý: sau một số lần lặp bước 2 vừa phải thì hàm sẽ đạt giá trị đủ nhỏ.

- Nếu learning_rate quá lớn: sẽ gây hiện tượng overshoot (như trong hình dưới bên phải) và không bao giờ đạt được giá trị nhỏ nhất của hàm.

<p align="center">
  <img src = "https://user-images.githubusercontent.com/51883796/81411870-2d8e8880-916d-11ea-992e-943bc0647f13.png">
</p>

* **7. Phân biệt Scalar, Vector, Matrix, Tensor**

Scalar là đại lượng chỉ độ lớn của cái gì đó, hay biểu diễn giá trị nào đó, mà không có hướng.

Vector : Khi dữ liệu biểu diễn dạng 1 chiều, người ta gọi là vector.

Matrix: Khi dữ liệu dạng 2 chiều, người ta gọi là ma trận, kích thước là số hàng * số cột

Tensor: Khi dữ liệu nhiều hơn 2 nhiều thì sẽ được gọi là tensor, ví dụ như dữ liệu có 3 chiều.

Tài liệu tham khảo: 

[1] Sách Deep Learning Cơ Bản của Nguyễn Thanh Tuấn. Website : https://nttuan8.com/ 

[2] https://viblo.asia/p/mot-so-ham-kich-hoat-trong-cac-mo-hinh-deep-learning-tai-sao-chung-lai-quan-trong-den-vay-part-1-ham-sigmoid-bWrZn4Rv5xw

[3] Machine Learning Cơ Bản https://machinelearningcoban.com/

[4] https://viblo.asia/p/nhung-cau-hoi-trong-phong-van-deep-learning-p1-YWOZrbPpZQ0

[Go to the Home Page]({{ '/' | absolute_url }})
  
