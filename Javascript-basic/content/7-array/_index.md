---
title : "Làm việc với Mảng"
date :  "`r Sys.Date()`" 
weight : 7 
chapter : false
pre : " <b> 7. </b> "
---

#### Mảng (Array) trong JavaScript
1. Khái niệm:
    - Mảng trong JavaScript là một kiểu dữ liệu được sử dụng để lưu trữ tập hợp các giá trị có thứ tự. Nó có thể chứa bất kỳ kiểu dữ liệu nào, bao gồm số, chuỗi, đối tượng, v.v.

2. Khai báo và khởi tạo:

    - Có hai cách phổ biến để khai báo và khởi tạo mảng trong JavaScript:
        - Sử dụng dấu ngoặc vuông:
            ```
            var arr = []; // Khai báo mảng rỗng
            var arr = [1, 2, 3, "a", "b"]; // Khai báo mảng với các giá trị ban đầu

            ```
        - Sử dụng hàm **Array**
            ```
            var arr = new Array(); // Khai báo mảng rỗng
            var arr = new Array(1, 2, 3, "a", "b"); // Khai báo mảng với các giá trị ban đầu

            ```
3. Truy cập phần tử:
    - Bạn có thể truy cập phần tử trong mảng bằng cách sử dụng chỉ mục. Chỉ mục bắt đầu từ 0, và tương ứng với vị trí của phần tử trong mảng.

        ```
        var arr = [1, 2, 3, "a", "b"];

        // Truy cập phần tử đầu tiên
        var firstElement = arr[0]; // firstElement = 1

        // Truy cập phần tử cuối cùng
        var lastElement = arr[arr.length - 1]; // lastElement = "b"

        ```

4. Thay đổi phần tử:
    - Bạn có thể thay đổi giá trị của phần tử trong mảng bằng cách gán giá trị mới cho nó.

        ```
        var arr = [1, 2, 3, "a", "b"];

        // Thay đổi giá trị của phần tử đầu tiên
        arr[0] = 10;

        // Thay đổi giá trị của phần tử cuối cùng
        arr[arr.length - 1] = "c";
        ```
5. Thêm phần tử:   
    - Có nhiều phương thức để thêm phần tử vào mảng:
        - Sử dụng phương thức **push**:
            ```
            var arr = [1, 2, 3];
            // Thêm phần tử vào cuối mảng
            arr.push(4); // arr = [1, 2, 3, 4]

            ```
        - Sử dụng phương thức **unshift**:

            ```
            var arr = [1, 2, 3];
            // Thêm phần tử vào đầu mảng
            arr.unshift(0); // arr = [0, 1, 2, 3]

            ```
6. Xóa phần tử:
    - Có nhiều phương thức để xóa phần tử khỏi mảng:
        - Sử dụng phương thức **pop**:
            ```
            var arr = [1, 2, 3];
            // Xóa phần tử cuối cùng khỏi mảng
            arr.pop(); // arr = [1, 2]

            ```
        - Sử dụng phương thức **shift**:
            ```
            var arr = [1, 2, 3];
            // Xóa phần tử đầu tiên khỏi mảng
            arr.shift(); // arr = [2, 3]
        - Sử dụng phương thức **splice** để xóa phần tử bất kì trong array
            ```
            var arr = [1, 2, 3];
            // Xóa phần tử thứ hai khỏi mảng
            arr.splice(1,1); // arr = [1, 3]
            ```
7. Tìm kiếm phần tử:
    - Bạn có thể sử dụng các phương thức sau để tìm kiếm phần tử trong mảng:
        - Phương thức **indexOf**:
            ```
            var arr = [1, 2, 3, "a", "b"];
            // Tìm vị trí xuất hiện đầu tiên của "a"
            var index = arr.indexOf("a"); // index = 3

            ```
        
        - Phương thức **lastIndexOf**:
            ```
            var arr = [1, 2, 3, "a", "b", "a"]; 
            // Tìm vị trí xuất hiện cuối cùng của "a"
            var index = arr.lastIndexOf("a"); // index = 5

            ```
8. Sắp xếp phần tử:
    - Sử dụng phương thức sort để sắp xếp phần tử trong mảng:
        ```
        var arr = [3, 2, 1, "a", "b"];
        // Sắp xếp phần tử theo thứ tự tăng dần
        arr.sort(); // arr = [1, 2, 3, "a", "b"]

        ```
9. Chuyển kiểu dữ liệu từ Object của Array sang String
    - Sử dụng phương thức **toString**
        ```
            var courses = [ 'Java', 'PHP', 'HTML'];
            console.log(courses.toString());
        ```
10. Nối 2 mảng lại với nhau
    - Sử dụng phương thức **concat**
        ```
        var arr1=['a', 'b', 'c'];
        var arr2=['e', 'f'];
        // Nối 2 mảng arr1 và arr2
        var arr3 = arr1.concat(arr2); // arr3= ['a', 'b', 'c', 'd', 'e', 'f']
        ```
11. Cắt phần tử của mảng
    - Sử dụng phương thức **slice**
        ```
         var arr = ['a', 'b', 'c'];
         // Cắt phần tử đầu tiên và phần tử cuối cùng
         var arr1 = arr.slice(1, 2); // arr1 = ['b']
        ```
#### Thực hành
1. Cho trước hàm **joinWithCharacter** có 2 tham số là array và charactor, hãy hoàn thành phần nội dung hàm sao cho hàm trả về 1 chuỗi là kết quả của việc nối từng phần tử của mảng với charactor.
    ```
       // Viết hàm tại đây
        // Ví dụ khi sử dụng
        var cars = ['BMW', 'Vinfast', 'Mercedes'];

        var result = joinWithCharacter(cars, ' - ');

        console.log(result); // Expected: "BMW - Vinfast - Mercedes"
    ```

    {{%expand "Kết quả" %}}
        function joinWithCharacter(array, charactor) {
            
            return(array.join(charactor));
        }
            // Ví dụ khi sử dụng
        var cars = ['BMW', 'Vinfast', 'Mercedes'];
        var result = joinWithCharacter(cars, ' - ');
        console.log(result); // Expected: "BMW - Vinfast - Mercedes"
    {{% /expand%}}

2. hãy tạo hàm **getLastElement** có 1 tham số (đối số là 1 array), hàm này sẽ trả về phần tử cuối cùng trong mảng.
    ```
    // Viết hàm tại đây


    // Ví dụ sử dụng
    var animals = ['Monkey', 'Tiger', 'Elephant'];
    var result = getLastElement(animals);

    console.log(result); // Expected: "Elephant"
    console.log(animals); // Expected: ['Monkey', 'Tiger', 'Elephant']
    ```

    {{%expand "Kết quả" %}}

        function getLastElement(arr){
            return(arr.slice(-1));
        }

        // Ví dụ sử dụng
        var animals = ['Monkey', 'Tiger', 'Elephant'];
        var result = getLastElement(animals);

        console.log(result); // Expected: "Elephant"
        console.log(animals); // Expected: ['Monkey', 'Tiger', 'Elephant']

    {{% /expand%}}
