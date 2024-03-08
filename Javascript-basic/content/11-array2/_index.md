---
title : "Làm việc với Mảng 2"
date :  "`r Sys.Date()`" 
weight : 11 
chapter : false
pre : " <b> 11. </b> "
---

#### forEach() 
1. Khái niệm
    - Dùng để duyệt qua từng phần tử của mảng. Nó cho phép bạn thực thi một hàm cho mỗi phần tử trong mảng.
    - Cú pháp:
        ```
            array.forEach(function(elment, index, array){
                // Đoạn code mà bạn muốn thực thi

            })
        ```
        - array: Mảng mà bạn muốn duyệt qua
        - function: Hàm thực thi
        - element: Biến đại diện cho từng phần tử của mảng
        - index: Ví trị hiện tại của phần tử trong mảng
        - array: Tham chiếu đến mảng ban đầu
    - Ví dụ: 
        ```
            var arr = ["a", "b", "c"];
            arr.forEach(function(element) {
            console.log(element);
            });

        ```
2. Thực hành
    - Tính tổng các phần tử của mảng
        
        {{%expand "Kết quả" %}}
            var arr = [1, 2, 3, 4, 5];
            var sum = 0;
            arr.forEach(function(element) {
            sum += element;
            });
            console.log(sum); //sum = 15
        {{% /expand%}}

#### every()
1. Khái niệm
    - Kiếm tra tất cả các phần tử trong mảng thỏa mãn điều kiện gì đó. Nếu 1 phần tử không thỏa mãn điều kiện, vòng lặp sẽ dừng lại.
    - Cú pháp:
        ```
            arr.every(function(element, index, array){
                // kiểm tra điều kiện
                return condition;
            });
        ```
        - arr: Mảng mà bạn muốn kiểm tra
        - function: Hàm thực thi
        - element: Biến đại diện cho từng phần tử của mảng
        - index: Ví trị hiện tại của phần tử trong mảng
        - arr: Tham chiếu đến mảng ban đầu
        - return: Giá trị **true** hoặc **false** được trả về, biểu thị phần tử đó có thỏa mãn điểu kiện hay không.
    - Ví dụ: 
        ```
            // Kiểm tra xem tất cả các phần tử đều là số chẵn
            var arr = [2, 4, 6, 8];
            var allEven = arr.every(function(element) {
            return element % 2 === 0;
            });
            console.log(allEven); // true

            // Kiểm tra xem tất cả các phần tử đều lớn hơn 5
            var arr = [6, 8, 10, 12];
            var allGreaterThanFive = arr.every(function(element) {
            return element > 5;
            });
            console.log(allGreaterThanFive); // true
        ```
2. Thực hành.
    - Kiểm tra xem tất các các khóa học có được miễn phí hay không. 
        ```
            myCourse = [
                {
                    id: 1,
                    name: 'SAA',
                    price: 0
                },
                {
                    d: 1,
                    name: 'SAP',
                    price: 0
                },
                {
                    d: 1,
                    name: 'DVA',
                    price: 0
                }
            ];
        ```
        {{%expand "Kết quả" %}}
            myCourse = [
                {
                    id: 1,
                    name: 'SAA',
                    price: 0
                },
                {
                    d: 1,
                    name: 'SAP',
                    price: 0
                },
                {
                    d: 1,
                    name: 'DVA',
                    price: 0
                }
            ];
            var iCheck = myCourse.every(function(course){
                return course.price === 0;

            });
            console.log(iCheck) // true: Tất cả các khóa học đều miễn phí, // false: Có khóa học tính phí
        {{% /expand%}}

#### some()
1. Khải niệm
    - Kiểm tra xem ít nhất một phần tử của một mảng đáp ứng một điều kiện nhất định. Nó trả về **true** ngay khi gặp một phần tử thỏa mãn điều kiện, và trả về **false** nếu không có phần tử nào thỏa mãn
    - Cú pháp:
        ```
            arr.some(function(element, index, array){
                // Kiểm tra điều kiện
                return condition;
            })
        ```
    - Ví dụ: Kiểm tra xem **ít nhất một** phần tử là số lẻ
        ```
            var arr = [2, 4, 6, 8];
            var hasOddNumber = arr.some(function(element) {
            return element % 2 !== 0;
            });
            console.log(hasOddNumber); // false
        ```

2. Thực hành
    - Kiểm tra xem có phần tử nào bằng 0 trong mảng sau hay không:
        ```
            var arr = [-1, 2, 3, 0];
        ```
    {{%expand "Kết quả" %}}
        var arr = [-1, 2, 3, 0];
        var isZero = arr.some(function(element) {
        return element === 0;
        });
        console.log(isZero); // true
    {{% /expand%}}

#### find()
1. Khái niệm
    - Tìm phần tử đầu tiên trong mảng thỏa mãn điều kiện đưa ra. Sau đó trả về giá trị đó ngay lập tức nếu thỏa mãm điều kiện, hoặc trả về undefines nếu không tìm thấy phần tử nào thỏa mãn điều kiện và dừng lặp
    - Cú pháp
        ```
            array.find(function(element, index, array) {
            // Hàm kiểm tra
            return condition;
            });
        ```
    - Ví dụ: Tìm số chẵn đầu tiên trong mảng
        ```
        const numbers = [1,2,4,0,9];
        const firstEvenNumber = numbers.find(function(number){
            return number % 2 === 0
        })
        console.log(firstEvenNumber); // Xuất: 2;
        ```
#### filter()
1. Khái niệm
    - Tìm tất cả các phần tử trong mảng thỏa mãn điều kiện đưa ra. Sau đó trả về giá trị phần tử đó nếu thỏa mãn điểu kiện hoặc trả mảng rỗng nếu không tìm thấy phần tử nào thỏa mãn điều kiện.
    - Cú pháp:  
         ```
            array.filer(function(element, index, array) {
            // Hàm kiểm tra
            return condition;
            });
        ```
    - Ví dụ: Tìm các phần tử chia hết cho 3
        ```
            var listNumber = [1,3,5,7,9,12];
            var result = listNumber.filter(function(number){
                return number % 3 === 0;
            })
            console.log(result) // [3,9,12]
        ```

2. Thực hành.
    - Tìm tất cả các khóa học về AWS SAA.
        ```
            myCourse = [
                    {
                        id: 1,
                        name: 'SAA',
                        price: 0
                    },
                    {
                        id: 2,
                        name: 'SAP',
                        price: 0
                    },
                    {
                        id: 3,
                        name: 'DVA',
                        price: 0
                    },
                    {
                        id: 4,
                        name: 'SAA',
                        price: 10
                    },
                ];
        ```

        {{%expand "Kết quả" %}}
            myCourse = [
                    {
                        id: 1,
                        name: 'SAA',
                        price: 0
                    },
                    {
                        id: 2,
                        name: 'SAP',
                        price: 0
                    },
                    {
                        id: 3,
                        name: 'DVA',
                        price: 0
                    },
                    {
                        id: 4,
                        name: 'SAA',
                        price: 10
                    },
                ];
            var iCheck = myCourse.filter(function(course){
                return course.name === 'SAA';
            })
            console.log (iCheck);
        {{% /expand%}}

#### map()
1. Khái niệm
    - Là một phương thức được sử dụng để chuyển đổi các phần tử trong một mảng JavaScript thành một mảng mới. Nó lặp qua mảng ban đầu và áp dụng một hàm cho mỗi phần tử. Hàm này có thể được sử dụng để thay đổi giá trị, sắp xếp lại thứ tự, hoặc trích xuất dữ liệu từ các phần tử.
    - Cú pháp
        ```
            array.map(function(element, index, array) {
            // Hàm biến đổi
            return transformedElement;
            }); 
        ```
    - Ví dụ: Nhân đôi mỗi phần tử trong mảng
        ```
            var numbers = [0, 1, 2, 3, 4, 5]
            function doubleNumber (numbers){
              return numbers *2;
            }
            var resultNumbers= numbers.map(doubleNumber);
            console.log(resultNumbers);
        ```
2. Thực hành
    - Thêm từ phần tử với key: address, value: 'Ho Chi Minh' vào trong tất cả các object trong mảng sau
        ```
            var course = [
                {
                    id: 1,
                    course: 'SAA',
                    price:10
                },
                {
                    id: 1,
                    course: 'DVA',
                    price:5
                },
                {
                    id: 1,
                    course: 'SAP',
                    price:20
                }
            ]
        ```
    
        {{%expand "Kết quả" %}}
            var course = [{
                    id: 1,
                    course: 'SAA',
                    price:10
                },
                {
                    id: 1,
                    course: 'DVA',
                    price:5
                },
                {
                    id: 1,
                    course: 'SAP',
                    price:20
                }
                ];
            function changeInfo(course){
            return {
                id:1,
                 course: 'SAA', 
                 price:10, 
                 address:'HCM'
                }
            }
            var changeInfo= course.map(changeInfo);
            console.log(changeInfo)
        {{% /expand%}}

#### reduce()
1. Khái niệm
    - Là một phương thức được sử dụng để thực thi một hàm lên các phần tử của mảng ( từ trái sang phải ) với một biến tích lũy để thu về một giá trị duy nhất. Là một phương thức quan trong hay sử dụng trong lập trình hàm.
    - Cú pháp:
        ```
            array.reduce(function(accumulator, currentValue, index, array) {
            // Hàm tích lũy
            return accumulatedValue;
            }, initialValue);

        ```
        - function: Ham callback được áp dụng cho từng phần tử. Hàm này có 4 tham số:
            - accumlator: Biến lưu trữ giá trị tích lũy sau mỗi lần lặp
            - currentValue: Phần tử hiện tại của mảng đang được xử lý
            - index (optional): Chỉ số của phần tử trong mảng đang được xử lý
            - array(optional): mảng hiện tại gọi hàm reduce()
        - initiaValue: là giá trị cho tham số thứ nhất (accumulator) của hàm callback trong lần gọi hàm đầu tiên. Nếu giá trị này không được cung cấp thì giá trị phần tử đầu tiên của mảng sẽ được sử dụng.
    - Ví dụ: TÍnh tổng các phần tử trong mảng
        ```
            var arr = [1,2,3,4,5,6]
            var sumArr = arr.reduce(function(total,number){
                return total + number;
            },0)
            console.log(sumArr)
        ```
2. Thực hành
    - Giả sử rằng chúng ta có một mảng đại diện cho danh sách thông tin các khóa học. Chúng ta hãy dùng hàm reduce() để tính tổng chi phi các khóa học đó.
        ```
            var course = [
                {
                    id: 1,
                    course: 'SAA',
                    price:10
                },
                {
                    id: 1,
                    course: 'DVA',
                    price:5
                },
                {
                    id: 1,
                    course: 'SAP',
                    price:20
                }
            ]
            var sumPrice = course.reduce(function(total, cost){
                return total + cost.price;  
            },0)
            console.log(sumPrice);
        ```