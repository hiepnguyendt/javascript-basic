---
title : "Làm việc với Hàm"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

**Hàm** là một khối mã được đặt tên và có thể được gọi để thực hiện một tác vụ cụ thể. Hàm giúp tổ chức mã thành các đơn vị nhỏ hơn, tái sử dụng mã và tạo ra các chức năng độc lập. Dưới đây là cách khai báo và sử dụng hàm trong JavaScript:

1. Khai báo hàm:
   - Hàm có thể được khai báo bằng cách sử dụng từ khóa function, theo sau là tên của hàm và danh sách các tham số trong dấu ngoặc đơn (). Thân hàm, chứa các câu lệnh để thực thi, được đặt trong cặp ngoặc nhọn {}.

      ```
      function myFunction(thamso1, thamso2) {
      // Khối mã của hàm
      return giaTriTrave;
      }
      ```
   
2. Tham số:
   - Định nghĩa: Tham số là giá trị được truyền vào function khi nó được gọi. Nó cho phép function nhận dữ liệu từ bên ngoài và sử dụng dữ liệu đó để thực hiện các thao tác.
   - Kiểu dữ liệu: không giới hạn kiểu dữ liệu
   - Truyền tham số:   
      - 1 tham số
      - Nhiều tham số
      - Ví dụ:

         ```
            function message(mess1, mess2) {
               console.log(mess1);
               console.log(mess2)
            }
            message('Hi', 'Hello');
         ```   
   
3. Gọi hàm:
   - Hàm có thể được gọi bằng cách sử dụng tên hàm, theo sau là danh sách các đối số trong dấu ngoặc đơn ().
      ```
      
         ```
            function message(mess1, mess2) {
               console.log(mess1);
               console.log(mess2)
            }
            message('Hi', 'Hello'); // gọi hàm message với 2 tham số Hi và Hello
         ```   
      ```
   
4. Giá trị trả về:
   - Hàm có thể trả về một giá trị bằng cách sử dụng từ khóa return. Khi gặp phần tử return, hàm sẽ kết thúc và trả về giá trị đã được xác định.
      ```
      function tinhTong(a, b) {
            return a + b;
         }
         var tong = tinhTong(2, 3); // tong = 5 // Gọi hàm và lưu giá trị trả về vào biến result
      console.log(result); // In ra 8

      ```

5. Hàm nặc danh (Anonymous function):
   - Hàm có thể được khai báo mà không cần tên, gọi là hàm nặc danh. Hàm nặc danh thường được sử dụng như một đối số của các hàm khác hoặc để tạo ra các khối mã độc lập.
      
      ```
            var myFunction = function() {
               // Thân hàm nặc danh
               // Các câu lệnh được thực thi ở đây
            };
      ```

6. Hàm mũi tên (Arrow function):
   - Arrow function là một cú pháp ngắn gọn để khai báo hàm trong JavaScript. Nó có thể giúp viết mã ngắn gọn hơn và giữ nguyên ngữ cảnh this của hàm gốc.

      ```
      var addNumbers = (a, b) => a + b;
      var result = addNumbers(5, 3);
      console.log(result); // In ra 8
      ```  

Hàm trong JavaScript rất mạnh mẽ và linh hoạt, cho phép bạn thực hiện các tác vụ phức tạp và tái sử dụng mã một cách dễ dàng.

7. Thực hành tạo hàm sum 
   - Hãy tạo 1 hàm có tên là sum có 2 tham số:
      - Tham số thứ 1 là a
      - Tham số thứ 2 là b

   {{%expand "Kết quả" %}}
   ```
   function sum(a,b){

   }      
   ```  
   {{% /expand%}}
