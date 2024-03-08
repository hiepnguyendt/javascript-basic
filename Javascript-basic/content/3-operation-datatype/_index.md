---
title : "Toán tử, Kiểu dữ liệu"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Toán tử
1. Sử dụng để thực hiện các phép tính và thao tác trên các giá trị. Dưới đây là một số toán tử phổ biến trong JavaScript:

    - Toán tử số học (Arithmetic):

        - **"+"** : Cộng hai giá trị.

        - **"-"** : Trừ giá trị bên phải từ giá trị bên trái.

        - **"*"** : Nhân hai giá trị.

        - **"/"** : Chia giá trị bên trái cho giá trị bên phải.

        - **"%"** : Lấy phần dư của phép chia giữa hai giá trị.
        - **"++"**: Tăng 1 giá trị số 
        - **"--"** : Giảm 1 giá trị số
        - **"**"** : Lũy thừa
        - Ví dụ: 
            - x++ tăng giá trị biến lên 1 và trả về giá trị trước khi tăng
            - ++x tăng giá trị biến lên 1 và trả về giá trị sau khi tăng
            - x-- giảm giá trị biến xuống 1 và trả về giá trị trước khi giảm
            - --x giảm giá trị biến xuống 1 và trả về giá trị sau khi giảmm


    - Toán tử gán (Assigment):
        - **"="** : a = b => a = b
        - **"+="** : a + = b => a = a + b
        - **"-="** : a - = b => a = a - b
        - **"*="** : a * = b => a = a * b
        - **"/="** : a / = b => a = a / b
        - **"%="** : a & = b => a = a % b
        - **"+="** : a ** = b => a = a ** b
    - Toán tử so sánh (Comparison):
        - **"=="** : Kiểm tra xem hai giá trị có bằng nhau hay không (không kiểm tra kiểu dữ liệu).
        - **"==="** : Kiểm tra xem hai giá trị có bằng nhau và cùng kiểu dữ liệu hay không.
        - **"!="** : Kiểm tra xem hai giá trị có khác nhau hay không (không kiểm tra kiểu dữ liệu).
        - **"!=="** : Kiểm tra xem hai giá trị có khác nhau hoặc khác kiểu dữ liệu hay không.
        - **">"** : Kiểm tra xem giá trị bên trái có lớn hơn giá trị bên phải hay không.
        - **"<"** : Kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải hay không.
        - **">="** : Kiểm tra xem giá trị bên trái có lớn hơn hoặc bằng giá trị bên phải hay không.
        - **"<="** : Kiểm tra xem giá trị bên trái có nhỏ hơn hoặc bằng giá trị bên phải hay không.
    - Toán tử logic (Logical):
        - **"&&"** : Phép AND logic, trả về true nếu cả hai giá trị đều đúng.
        - **"||"** : Phép OR logic, trả về true nếu ít nhất một trong hai giá trị là đúng.
        - **"!"** : Phép NOT logic, đảo ngược giá trị logic.
    -  Toán tử nổi chuỗi:
        - "**+**" : Nối chuỗi, kết hợp hai chuỗi lại với nhau.
        - Ví dụ:
            ```
            var firstName = 'First Cloud';
            var lastName = 'Journey';
            var fullName = firstName + ' ' + lastName; 
            console.log(fullName); // First Cloud Journey
            ```
    Và còn nhiều toán tử khác như toán tử ba ngôi (ternary), toán tử tăng/giảm (++/--), toán tử bit, và toán tử khác. Mỗi toán tử có cú pháp và quy tắc hoạt động riêng, nên cần hiểu kỹ để sử dụng đúng và hiệu quả.

#### Kiểu dữ liệu
1. Sử dụng để lưu trữ và làm việc với các giá trị. Dưới đây là một số kiểu dữ liệu phổ biến trong JavaScript:

    - Kiểu dữ liệu Nguyên thủy (Primitive Data Types):
        - **Number**: Kiểu dữ liệu số, bao gồm cả số nguyên và số thực.
            ```
                var a = 1;
                var b = 2;
            ```
        - **String**: Kiểu dữ liệu chuỗi, được sử dụng để lưu trữ và làm việc với các dãy ký tự.
            ```
                var fullName = "First Cloud Journey"
            ```
        - **Boolean**: Kiểu dữ liệu logic, chỉ có hai giá trị là true (đúng) và false (sai).   
            ```
                var isSuccess = true; 
            ```
        - **null**: Biểu thị giá trị không tồn tại hoặc không hợp lệ.   
            ```
                var isNull = null; // không có gì
            ```
        - **undefined**: Biểu thị một biến chưa được gán giá trị.    
            ```
                var age;
            ```
        - **Symbol**: Kiểu dữ liệu duy nhất và không thay đổi, được sử dụng để tạo ra     các giá     trị duy nhất.    
            ```
                var id = Symbol('id') // tính duy nhất
            ```
    - Kiểu dữ liệu Đối tượng (Object Data Type):
        - **Object**: Kiểu dữ liệu đối tượng, được sử dụng để lưu trữ và làm việc với các thuộc tính và phương thức.
            ```
                var myObject = {
                    name: 'First Cloud Journey',
                    age: 10,
                    address: 'Ho CHi Minh'
                }
            ```
    - Kiểu dữ liệu Đặc biệt:
        - **Array**: Một loại đặc biệt của đối tượng, được sử dụng để lưu trữ và làm việc với một tập hợp các giá trị có thứ tự.
            ```
                var myArray = [
                    'SAA',
                    'DVA',
                    'SAP'
                ];
            ```
        - **Function**: Một loại đặc biệt của đối tượng, được sử dụng để định nghĩa và thực thi các khối mã.    
            ```
                var myFunction = function (){
                    alert('Welcome to the First Cloud Journey');
                }
            ```
2. Kiểm tra kiểu dữ liệu
    - Sử dụng typeof để kiểm tra kiểu dữ liệu
    - Ví dụ:
        ```
            var a = '1';
            var b = 2;
            var c = typeof a;
            var d = typeof b;
            var e = typeof d;
            console.log(c, d, e) // Output: c: string,  d: number, e: string

        ```
    - Chú ý: Kết quả trả về của typeof sẽ luôn là 1 chuỗi, vậy nên typeof của d sẽ là 'string'.
    
    Nhưng đáng lưu ý rằng JavaScript là một ngôn ngữ có kiểu dữ liệu động (dynamically typed), điều này có nghĩa là bạn không cần phải khai báo kiểu dữ liệu cho biến khi tạo ra chúng. Kiểu dữ liệu được xác định tự động dựa trên giá trị mà biến đang giữ. Điều này cho phép bạn gán các kiểu dữ liệu khác nhau cho cùng một biến trong quá trình thực thi.