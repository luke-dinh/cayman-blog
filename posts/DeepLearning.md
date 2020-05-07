---
layout: page
title: Posts
tagline: 
permalink: /posts/DeepLearning.html
ref: posts
order: 1
---

## Những kiến thức cơ bản về Deep Learning

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
