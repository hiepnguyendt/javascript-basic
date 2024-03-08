---
title : "Toán tử, Kiểu dữ liệu"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Toán tử
1. Sử dụng để thực hiện các phép tính và thao tác trên các giá trị. Dưới đây là một số toán tử phổ biến trong JavaScript:

    - Toán tử số học:

        - **"+"** : Cộng hai giá trị.

        - **"-"** : Trừ giá trị bên phải từ giá trị bên trái.

        - **"*"** : Nhân hai giá trị.

        - **"/"** : Chia giá trị bên trái cho giá trị bên phải.

        - **"%"** : Lấy phần dư của phép chia giữa hai giá trị.

    - Toán tử gán:
        - **"="** : Gán giá trị bên phải cho biến bên trái.
        - **"+="** : Cộng giá trị bên phải với giá trị củ- a biến bên trái và gán kết quả cho biến đó.
    - Toán tử so sánh:
        - **"=="** : Kiểm tra xem hai giá trị có bằng nhau hay không (không kiểm tra kiểu dữ liệu).
        - **"==="** : Kiểm tra xem hai giá trị có bằng nhau và cùng kiểu dữ liệu hay không.
        - **"!="** : Kiểm tra xem hai giá trị có khác nhau hay không (không kiểm tra kiểu dữ liệu).
        - **"!=="** : Kiểm tra xem hai giá trị có khác nhau hoặc khác kiểu dữ liệu hay không.
        - **">"** : Kiểm tra xem giá trị bên trái có lớn hơn giá trị bên phải hay không.
        - **"<"** : Kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải hay không.
        - **">="** : Kiểm tra xem giá trị bên trái có lớn hơn hoặc bằng giá trị bên phải hay không.
        - **"<="** : Kiểm tra xem giá trị bên trái có nhỏ hơn hoặc bằng giá trị bên phải hay không.
    - Toán tử logic:
        - **"&&"** : Phép AND logic, trả về true nếu cả hai giá trị đều đúng.
        - **"||"** : Phép OR logic, trả về true nếu ít nhất một trong hai giá trị là đúng.
        - **"!"** : Phép NOT logic, đảo ngược giá trị logic.
    - Toán tử chuỗi:
        - **"+"** : Nối chuỗi, kết hợp hai chuỗi lại với nhau.

    Và còn nhiều toán tử khác như toán tử ba ngôi (ternary), toán tử tăng/giảm (++/--), toán tử bit, và toán tử khác. Mỗi toán tử có cú pháp và quy tắc hoạt động riêng, nên cần hiểu kỹ để sử dụng đúng và hiệu quả.

#### Kiểu dữ liệu
1. Sử dụng để lưu trữ và làm việc với các giá trị. Dưới đây là một số kiểu dữ liệu phổ biến trong JavaScript:

    - Kiểu dữ liệu Nguyên thủy (Primitive Data Types):
        - **Number**: Kiểu dữ liệu số, bao gồm cả số nguyên và số thực.
        - **String**: Kiểu dữ liệu chuỗi, được sử dụng để lưu trữ và làm việc với các dãy ký tự.
        - **Boolean**: Kiểu dữ liệu logic, chỉ có hai giá trị là true (đúng) và false (sai).   
        - **null**: Biểu thị giá trị không tồn tại hoặc không hợp lệ.   
        - **undefined**: Biểu thị một biến chưa được gán giá trị.    
        - **Symbol**: Kiểu dữ liệu duy nhất và không thay đổi, được sử dụng để tạo ra     các giá     trị duy nhất.    
    - Kiểu dữ liệu Đối tượng (Object Data Type):
        - **Object**: Kiểu dữ liệu đối tượng, được sử dụng để lưu trữ và làm việc với các thuộc tính và phương thức.
    - Kiểu dữ liệu Đặc biệt:
        - **Array**: Một loại đặc biệt của đối tượng, được sử dụng để lưu trữ và làm việc với một tập hợp các giá trị có thứ tự.
        - **Function**: Một loại đặc biệt của đối tượng, được sử dụng để định nghĩa và thực thi các khối mã.    

    Nhưng đáng lưu ý rằng JavaScript là một ngôn ngữ có kiểu dữ liệu động (dynamically typed), điều này có nghĩa là bạn không cần phải khai báo kiểu dữ liệu cho biến khi tạo ra chúng. Kiểu dữ liệu được xác định tự động dựa trên giá trị mà biến đang giữ. Điều này cho phép bạn gán các kiểu dữ liệu khác nhau cho cùng một biến trong quá trình thực thi.