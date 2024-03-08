---
title : "Làm việc với Số"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---

1. Khái niệm
   - Kiểu dữ liệu số trong JavaScript được sử dụng để biểu diễn các giá trị số.     
   - Bao gồm hai loại chính:
      - Số nguyên: Ví dụ: 1, 2, 3, 4, 5
      - Số thực: Ví dụ: 1.2, 3.14, 100.5
2. Biểu diễn
   - Số trong JavaScript được biểu diễn dưới dạng số thực dấu phẩy động theo chuẩn IEEE-754 với độ chính xác kép.
3. Thao tác
   - JavaScript cung cấp nhiều toán tử và hàm để thao tác với số, bao gồm:
      - Toán tử số học: +, -, *, /, %, ++, --
      - Hàm toán học: Math.sqrt(), toString, toFixed , Math.round()

      ```
      var a = 10;
      var b = 20;

      // Cộng hai số
      var a = a + b; // a = 30

      // Trừ hai số
      var b = b - a; // b = 10

      // Nhân hai số
      var c = a * b; // c = 200

      // Chia hai số
      var d = b / a; // d = 2

      // Lấy căn bậc hai
      var e = Math.sqrt(a); // e = 3.162277660168379

      // Làm tròn xuống
      var Pi = 3.14
      var g = Pi.toFixed(); //g = 3

      // Làm tròn lên
      var Pi = 3.5
      var h = Pi.toFixed(); //h = 4

      // Làm tròn số thập phân
      var Pi = 3.1412434
      var f = Pi.toFixed(2) // f = 3.14

      // Convert từ số sang chuỗi

      var myString = a.toString(); // myString = '20'
      console.log(a, b, c, d, e, f, g, h);
      ```