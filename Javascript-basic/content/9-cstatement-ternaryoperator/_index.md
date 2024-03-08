---
title : "Câu lệnh điều kiện - Toán tử ba ngôi"
date :  "`r Sys.Date()`" 
weight : 9 
chapter : false
pre : " <b> 9. </b> "
---

#### Lệnh rẽ nhánh If else
1. Khái niệm
    - Câu lệnh diều kiện if..else là 1 trong những cấu trúc điều kiện cơ bản. Nó cho phép bạn thực thi 1 khối mã nhật dịnh chỉ khi một điều kiện nào đó được thỏa mãn.
    - Cú pháp:
        ```
            if(điều kiện){
                // code sẽ được thực thi nếu thỏa điều kiện
            } else {
                // code sẽ được thực thi nếu thỏa điều kiện
            }
        ```
    - Ví dụ: 
        ```
        var a = 1;
        var b = 2;
        if ( a < b){
            console.log("So sánh đúng!");
        } else {
            console.log("So sánh sai!");
        }
        ```

#### Câu lệnh rẽ nhánh - Switch
1. Khái niệm
    -  Câu lệnh điều kiện switch...case là một lựa chọn khác để thực hiện logic rẽ nhánh trong JavaScript. Nó hữu ích khi bạn muốn kiểm tra một biến với nhiều giá trị khác nhau và thực thi các khối lệnh tương ứng.
    - Cú pháp:
        ```
          switch (expression) {
            case value1:
                // Khối lệnh được thực thi nếu expression có giá trị bằng value1
                break;
            case value2:
                // Khối lệnh được thực thi nếu expression có giá trị bằng value2
                break;
            // ... Thêm các case khác nếu cần
            default:
                // Khối lệnh mặc định được thực thi nếu expression không khớp với bất kỳ case nào (tùy chọn)
            }  
        ```
    - Ví dụ: 
        ```
            var day = 3;

            switch (day) {
            case 1:
                console.log("Thứ Hai");
                break;
            case 2:
                console.log("Thứ Ba");
                break;
            case 3:
                console.log("Thứ Tư");
                break;
            default:
                console.log("Không phải ngày trong tuần (1-3)");
            }
        ```
3. Toán tử 3 ngôi (Ternary operator)
    - Khái niệm: Toán tử 3 ngôi, hay còn gọi là toán tử điều kiện, là một toán tử trong JavaScript cho phép bạn rút gọn cú pháp của một phép gán hoặc một câu lệnh điều kiện if/else.
    - Cú pháp:
        ```
            điều kiện ? giâ trị 1 : giá trị 2

        ```
    - Ví dụ:
        ```
            var num = 10;
            var result = num > 0 ? "Số dương" : "Số không dương";
            console.log(result); // "Số dương"

        ```
    - Thực hành: 
        - Tạo hàm **getCanVoteMessage**, hàm này có 1 tham số là **age**. Trong trường hợp từ 18 tuổi trở lên hàm sẽ trả về Bạn có thể bỏ phiếu, ngược lại hàm trả về Bạn chưa được bỏ phiếu.

        {{%expand "Kết quả" %}}
            // Làm bài
            function getCanVoteMessage(age){
            var     canVote = age >= 18 ? "Bạn có thể bỏ phiếu" : "Bạn chưa được bỏ phiếu";
            return canVote;
            }
            // Kỳ vọng
            console.log(getCanVoteMessage(18)) // 'Bạn có thể bỏ phiếu'
            console.log(getCanVoteMessage(15)) // 'Bạn chưa được bỏ phiếu'
        {{% /expand%}}
