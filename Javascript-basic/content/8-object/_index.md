---
title : "Làm việc với Object"
date :  "`r Sys.Date()`" 
weight : 8 
chapter : false
pre : " <b> 8. </b> "
---


#### Object trong JavaScript

1. Khái niệm:

- Object trong JavaScript là một kiểu dữ liệu được sử dụng để lưu trữ tập hợp các dữ liệu có liên quan với nhau. Nó bao gồm các thuộc tính (property) và phương thức (method).

2. Khai báo và khởi tạo:

- Có nhiều cách để khai báo và khởi tạo object trong JavaScript:
    - Sử dụng **dấu ngoặc vuông**:
        ```
        var obj = {}; // Khai báo object rỗng
        var obj = {name: "Nguyễn Văn A", age: 30}; // Khai báo object với các thuộc tính ban đầu

        ```
    - Sử dụng hàm **Object**:
        ```
        var obj = new Object(); // Khai báo object rỗng
        var obj = new Object({name: "Nguyễn Văn A", age: 30}); // Khai báo object với các thuộc tính ban đầu
        ```
    - Sử dụng **literal object**:
        ```
        var obj = {
        name: "Nguyễn Văn A",
        age: 30,
        sayHello: function() {
            console.log("Hello!"); }
        };

        ```
3. Truy cập thuộc tính:
    - Bạn có thể truy cập thuộc tính của object bằng cách sử dụng tên của nó.
        ```
        var obj = {name: "Nguyễn Văn A", age: 30};
        // Truy cập thuộc tính "name"
        var name = obj.name; // name = "Nguyễn Văn A"   
        // Truy cập thuộc tính "age"
        var age = obj.age; // age = 30

        ```
4. Thêm thuộc tính:
    - Bạn có thể thêm thuộc tính mới vào object bằng cách sử dụng toán tử **.** hoặc **[]**.
        ```
        var obj = {name: "Nguyễn Văn A"};
        // Thêm thuộc tính "age"
        obj.age = 30;
        // Thêm thuộc tính "address"
        obj["address"] = "123 Main Street";

        ```
5. Xóa thuộc tính:
    - Bạn có thể sử dụng toán tử delete để xóa thuộc tính khỏi object.
        ```
        var obj = {name: "Nguyễn Văn A", age: 30};
        // Xóa thuộc tính "age"
        delete obj.age;

        ```
6. Phương thức:
    - Phương thức là hàm được gắn vào object. Bạn có thể gọi phương thức bằng cách sử dụng tên của nó.
        ```
        var obj = {
            name: "Nguyễn Văn A",
            sayHello: function() {
                console.log("Hello!");
            }
        };

        // Gọi phương thức "sayHello"
        obj.sayHello(); // output: Hello!

        ```

7. Date Object
    - Khái niệm
        - **Date object** là một kiểu dữ liệu được sử dụng để biểu diễn ngày, giờ, phút, giây, mili giây và múi giờ trong JavaScript.
        - Nó lưu trữ thông tin ngày tháng theo giờ chuẩn quốc tế (UTC - Coordinated Universal Time).
        - Bạn có thể sử dụng các phương thức của Date object để truy cập, thay đổi, và thao tác với các thành phần ngày giờ.
    - Tạo Date object
        - Sử dụng hàm khởi tạo new Date():
            ```
                var now = new Date(); // Tạo Date object với thời gian hiện tại
            ```
        - Truyền chuỗi ngày tháng:
            ```
                var dateString = "2023-11-19";
                var date = new Date(dateString); // Tạo Date object từ chuỗi ngày tháng
            ```
        -  Truyền các thành phần ngày tháng riêng biệt:
            ```
                var year = 2024;
                var month = 2; // Tháng bắt đầu từ 0 (tháng 2 là 1)
                var day = 5;
                var hour = 10;
                var minute = 30;
                var second = 0;
                var millisecond = 0;
                var date = new Date(year, month, day, hour, minute, second, millisecond);
            ```
    - Các thành phần ngày, giờ:
        |Thuộc tính|Miêu tả|
        |---|---|
        |year|Năm|
        |month|Tháng (0-11)|
        |date|Ngày (1-31)|
        |hours|Giờ (0-23)|
        |minutes|Phút (0-59)|
        |seconds|Giây(0-59)|
        |milliseconds|Mili giây(0-999)|
        |getDay()|Trả về thứ trong tuần (0: chủ nhật;  6: thứ 7)|
        - Ví dụ:
            ```
            var now = new Date();
            var year = now.getFullYear();
            var month = now.getMonth() + 1; // Tháng bắt đầu từ 1
            var day = now.getDate();
            var hour = now.getHours();
            var minute = now.getMinutes();
            var second = now.getSeconds();
            console.log("Ngày: " + day + "/" + month + "/" + year);
            console.log("Giờ: " + hour + ":" + minute + ":" + second);

            ```

    - Thay đổi các thành phần ngày giờ
        |Phương thức| Miêu tả|
        |---|---|
        |setFullYear(year)|Thiết lập năm|
        |setMonth(month)|Thiết lập tháng (0-11)|
        |setDate(day)|Thiết lập ngày trong tháng (1-31)|
        |setHours(hour)|Thiết lập giờ (0-23)|
        |setMinutes(minute)|Thiết lập phút (0-59)|
        |setSeconds(second)|Thiết lập giây (0-59)|
        |setMilliseconds(millisecond)|Thiết lập mili giây (0-999)|
      
         - Ví dụ:
            ```
                var date = new Date(2023, 10, 20); // Tháng 11 (index 10)
                date.setMonth(7); // Tháng 8 (index 7)
                date.setDate(31);
                console.log(date); // "2023-08-31T00:00:00.000Z"

            ```
8. Math object
    - Math Object là một đối tượng cung cấp các hàm toán học và hằng số thường dùng
    - Các hàm thường dùng: 
        |Tên hàm|Miêu tả|Ví dụ|
        |----|---|---|
        |Math.abs(x)|Tìm giá trị tuyệt đối của x|Math.abs(-5) trả về 5|
        |Math.ceil(x)|Làm tròn x lên thành số nguyên lớn nhất không nhỏ hơn x|Math.ceil(2.3) trả về 3|
        |Math.floor(x)|Làm tròn x xuống thành số nguyên nhỏ nhất không lớn hơn x|Math.floor(2.3) trả về 2|
        |Math.round(x)|Làm tròn x đến số nguyên gần nhất|Math.round(2.3) trả về 2, Math.round(2.7) trả về 3|
        |Math.max(x1, x2, ...)|Tìm giá trị lớn nhất trong các số|Math.max(10, 5, 15) trả về 15|
        |Math.min(x1, x2, ...)|Tìm giá trị nhỏ nhất trong các số|Math.min(10, 5, 15) trả về 5|
        |Math.pow(x, y)|Tính x lũy thừa y|Math.pow(2, 3) trả về 8|
        |Math.random()|Tạo số ngẫu nhiên từ 0 đến 1 (không bao gồm 1)|Math.random() trả về giá trị bất kỳ trong khoảng (0, 1)|
        |Math.sqrt(x)|Tính căn bậc hai của x|Math.sqrt(16) trả về 4|
       
    - Ví dụ: tạo hàm getRandomNumber, hàm này nhận 1 tham số là mảng và sẽ trả về ngẫu nhiên 1 phần tử của mảng.
        ```
            function getRandomNumber(array){
                var index = Math.floor(Math.random() * array.length);
                return array[index];
            }
        ```