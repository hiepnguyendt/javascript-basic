---
title : "Number"
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
      - Hàm toán học: Math.sqrt(), Math.floor(), Math.ceil(), Math.round()

      ```
      var x = 10;
      var y = 20;

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
      var f = Math.floor(a.5); // f = 1

      // Làm tròn lên
      var g = Math.ceil(a.5); // g = 2

      // Làm tròn
      var h = Math.round(a.5); // h = 2

      console.log(a, b, c, d, e, f, g, h);
      ```