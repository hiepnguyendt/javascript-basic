---
title : "Var, Comment, Builtin"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---
1. Khai báo biến ( Var ) 

    - Trong JavaScript, từ khóa **"var"** được sử dụng để khai báo một biến. Khi sử dụng **"var"**, bạn có thể tạo ra một biến và gán giá trị cho nó.

    - Ví dụ: Để khai báo một biến có tên **"fullName"** và gán giá trị là **"First Cloud Journey"**, bạn có thể sử dụng từ khóa **"var"** như sau:

        ```
        var fullName = 'First Cloud Journey'; // khai báo tên

        ```
    - Sau khi khai báo, biến **"First Cloud Journey"** có thể được sử dụng trong phạm vi của khối mã mà nó được khai báo trong, hoặc trong toàn bộ phạm vi chương trình nếu nó được khai báo ở mức độ global.

    - Một biến được khai báo bằng **"var"** có phạm vi chức năng **(function scope)**. Điều này có nghĩa là biến chỉ có thể được truy cập trong cùng một hàm hoặc khối mã nơi nó được khai báo. Nếu bạn cố gắng truy cập biến bên ngoài phạm vi đó, bạn sẽ gặp lỗi.

    - Ví dụ: 

        ```
        function myFunction() {
          var fullName = 'First Cloud Journey'; // Biến fullName chỉ có thể truy cập trong myFunction()
          console.log(fullName); // In ra First Cloud Journey
        }

        console.log(fullName); // Lỗi - biến fullName không tồn tại ở đây
        ```

2. Comments

    - Trong JavaScript, chú thích (comments) được sử dụng để thêm các ghi chú, giải thích mã nguồn hoặc tạm thời vô hiệu hóa một đoạn mã. Chú thích không được thực thi và không ảnh hưởng đến luồng điều khiển của chương trình.

    - Có hai loại chú thích phổ biến trong JavaScript:

        - Chú thích một dòng:  dùng hai dấu gạch chéo **(//)**: Dùng để chú thích một dòng. Mọi nội dung sau dấu **//** trong cùng một dòng được coi là chú thích và không được thực thi.
        - Ví dụ:
          ```
          // Đây là một comment dùng để giải thích code
          var x = 10; // Gán giá trị 10 cho biến x
          ```
        - Chú thích nhiều dòng:  dùng dấu gạch chéo và dấu sao **(/* ... */)** hoặc **(/** */)**: Dùng để chú thích nhiều dòng hoặc một phần của mã. Mọi nội dung nằm trong cặp dấu trên được coi là chú thích và không được thực thi.
        - Ví dụ:  
            ```
            /*
            Đây là một chú thích
            dùng để giải thích mã nguồn
            */
            var y = 20; /* Gán giá trị 20 cho biến y */
            ```
    - Sử dụng phím tắt:
        - Windows: **Ctrl + /**
        - MacOS: **Command + /**
3. Built-in
    - Trong JavaScript, thuật ngữ **"builtin" (hay "built-in")** được sử dụng để chỉ các đối tượng, phương thức, hàm hoặc biến mà đã được cung cấp sẵn bởi ngôn ngữ JavaScript và có thể sử dụng mà không cần phải khai báo hoặc tải thêm thư viện ngoài.

    - Ví dụ về các "builtin" trong JavaScript bao gồm:
      - Các đối tượng toàn cục như ***Math***, ***Date***, ***RegExp***, ***Array***, ***Object***, ***String***,...
        ```
        var currentDate = new Date(); // Sử dụng đối tượng Date
        var text = "Hello, World!"; // Sử dụng đối tượng String
        var numbers = [1, 2, 3, 4, 5]; // Sử dụng đối tượng Array       
        ```

      - Các hàm toàn cục như **alert**, **console**, **confirm**, **promt**, ***parseInt()***, ***parseFloat()***, ***isNaN()***, ***setTimeout()***, ***setInterval()***,...
        ```
        var number = parseInt("10"); // Sử dụng hàm parseInt()
        setTimeout(function() {
          console.log("Thời gian đã hết!");
          alert("Thời gian đã hết!");
        }, 5000); // Sử dụng hàm setTimeout() để chạy hàm trên trong thời gian là 5s
        
        ```

      - Các biến toàn cục như undefined, NaN, Infinity,...

        ```
        console.log(undefined); // In ra giá trị undefined
        console.log(NaN); // In ra giá trị NaN
        console.log(Infinity); // In ra giá trị Infinity
        ```

      Các **"builtin"** trong JavaScript là những thành phần cốt lõi của ngôn ngữ và cung cấp các chức năng phổ biến để thực hiện các tác vụ như xử lý chuỗi, thao tác mảng, làm việc với thời gian, tính toán số học, và nhiều hơn nữa.