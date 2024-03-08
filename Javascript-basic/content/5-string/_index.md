---
title : "Làm việc với Chuỗi"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

Trong JavaScript, một "string" là một chuỗi các ký tự được đặt trong dấu nháy đơn ('') hoặc dấu nháy kép (""). Dưới đây là một số ví dụ về cách khai báo và sử dụng string trong JavaScript:

1. Kiểu dữ liệu

    - Chuỗi là một kiểu dữ liệu nguyên thủy trong JavaScript. Nó được biểu diễn bằng đối tượng **String**.

2. Tạo chuỗi
    - Có nhiều cách để tạo chuỗi trong JavaScript:
        - Sử dụng dấu nháy đơn hoặc dấu nháy kép:
            ```
            var str1 = "First Cloud Journey";
            var str2 = 'First Cloud Journey';
            ```
        - Sử dụng hàm String:

            ```
            var str3 = new String("First Cloud Journey");
            ```
        - Sử dụng toán tử nối (+):
            ```
            var str4 = "First" + " " + "Cloud" + " " + "Journey";
            ```
3. Thao tác với chuỗi
    - JavaScript cung cấp nhiều phương thức để thao tác với chuỗi, bao gồm:
        - Lấy độ dài chuỗi:
            ```
            var str = "First Cloud Journey";
            var length = str.length; // length = 18
            ```
        - Tìm kiếm ký tự:
            ```
            var str = "First Cloud Journey";
            var index = str.indexOf("i"); // index = 1
            ```
        - Cắt chuỗi:
            ```
            var str = "First Cloud Journey";
            var sliceStr = str.slice(0, 5); // slice = "First"
            ```
        - Cắt 1 chuỗi thành 1 array
            ```
            var str = 'First, Cloud , Journey';
            var splitStr = str.split(', '); // tìm để điểm chung của chuỗi để cắt
            ```
        - Chuyển đổi chuỗi:
            ```
            var str = "First Cloud Journey";
            var uppercase = str.toUpperCase(); // uppercase = "FIRST CLOUD JOURNEY"
            ```
        - Thay thế chuỗi
            - Thay thế một chuỗi con cụ thể
            ```
            var str = "Hello, world!Welcome to the First Cloud Journey.";
            var replaceStr = str.replace("world","everyone"); 
            console.log(replacedString1); // Output: Hello, everyone*! Welcome to First Cloud Journey.
            ```
            - Thay thế tất cả các kết quả khớp với một chuỗi con
            ```
            var str = "Hello, world!Welcome to the First Cloud Journey.";
            var replaceStr1 = str.replace(/world/g,"everyone"); 
            console.log(replacedString1); // Output: Hello, everyone! Welcome to the First Cloud Journey.
            ```
            - Thay thế bằng sử dụng biểu thức chính quy
            ```
            var str = "Hello, world!Welcome to the First Cloud Journey.";
            var replaceStr2 = str.replace(/o/gi,"*"); 
            console.log(replacedString2); // Output: Hell*, every*e! Welc*me t* the First Cl*ud J*urney.
            ```
            - Loại bỏ khoảng trắng thừa
            ```
            var str = "Hello, world!Welcome to the First Cloud Journey.";
            var trimStr= str.trim();
            ```
        - Template String
            ```
                var firstName = 'First Cloud';
                var lastName = 'Journey'
                console.log(`Welcome to ${firstName} ${lastName}`);
            ```