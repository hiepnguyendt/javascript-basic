---
title : "Quản lý session logs"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---


Với Session Manager chúng ta có thể xem được lịch sử các kết nối tới cá---
title : "Hàm"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

**Hàm** là một khối mã được đặt tên và có thể được gọi để thực hiện một tác vụ cụ thể. Hàm giúp tổ chức mã thành các đơn vị nhỏ hơn, tái sử dụng mã và tạo ra các chức năng độc lập. Dưới đây là cách khai báo và sử dụng hàm trong JavaScript:

1. Khai báo hàm:
   - Hàm có thể được khai báo bằng cách sử dụng từ khóa function, theo sau là tên của hàm và danh sách các tham số trong dấu ngoặc đơn (). Thân hàm, chứa các câu lệnh để thực thi, được đặt trong cặp ngoặc nhọn {}.

      ```
      function myFunction(param1, param2) {
      // Thân hàm
      // Các câu lệnh được thực thi ở đây
      }
      ```

2. Gọi hàm:
   - Hàm có thể được gọi bằng cách sử dụng tên hàm, theo sau là danh sách các đối số trong dấu ngoặc đơn ().
      ```
      myFunction(arg1, arg2); // Gọi hàm myFunction với các đối số arg1 và arg2
      ```
   
3. Giá trị trả về:
   - Hàm có thể trả về một giá trị bằng cách sử dụng từ khóa return. Khi gặp phần tử return, hàm sẽ kết thúc và trả về giá trị đã được xác định.
      ```
      function addNumbers(a, b) {
      return a + b;
      }

      var result = addNumbers(5, 3); // Gọi hàm và lưu giá trị trả về vào biến result
      console.log(result); // In ra 8

      ```

4. Hàm nặc danh (Anonymous function):
   - Hàm có thể được khai báo mà không cần tên, gọi là hàm nặc danh. Hàm nặc danh thường được sử dụng như một đối số của các hàm khác hoặc để tạo ra các khối mã độc lập.
      
      ```
            var myFunction = function() {
               // Thân hàm nặc danh
               // Các câu lệnh được thực thi ở đây
            };
      ```

5. Hàm mũi tên (Arrow function):
   - Arrow function là một cú pháp ngắn gọn để khai báo hàm trong JavaScript. Nó có thể giúp viết mã ngắn gọn hơn và giữ nguyên ngữ cảnh this của hàm gốc.

      ```
      var addNumbers = (a, b) => a + b;
      var result = addNumbers(5, 3);
      console.log(result); // In ra 8
      ```


Hàm trong JavaScript rất mạnh mẽ và linh hoạt, cho phép bạn thực hiện các tác vụ phức tạp và tái sử dụng mã một cách dễ dàng.c instance thông qua **Session history**. Tuy nhiên chúng ta chưa xem được chi tiết các câu lệnh được sử dụng.

![S3](/images/4.s3/001-s3.png)

Trong phần này chúng ta sẽ tiến hành tạo S3 bucket và thực hiện cấu hình lưu trữ các session logs để xem được chi tiết các câu lệnh được sử dụng trong session.

![port-fwd](/images/arc-log.png) 

### Nội dung:

  - [Cập nhật IAM Role](./4.1-updateiamrole/)
  - [Tạo **S3 Bucket**](./4.2-creates3bucket/)
  - [Tạo S3 Gateway endpoint](./4.3-creategwes3)
  - [Cấu hình **Session logs**](./4.4-configsessionlogs/)
