---
title : "Vòng lặp"
date :  "`r Sys.Date()`" 
weight : 10 
chapter : false
pre : " <b> 10. </b> "
---

#### Vòng lặp For
1. Khái niệm
    - Vòng lặp **for** là vòng lặp dùng để thực thi một hành động lặp đi lặp lại.
    - Cú pháp 1:
        ```
            for ( var i = 0; i < 10; i++){
                console.log(i);
            }
        ```
        - **var i = 0**: Khởi tạo biến cho vòng lặp
        -  **i < 10**: điểu kiện để vòng lặp thực hiện
        -  **i++**: tằng giá trị chạy lên 1 mỗi khi thực hiện xong hành động
    - Cú pháp 2:  Bạn có thể bỏ trống ***giá trị ban đầu*** trong cú pháp của vòng lặp for nếu trước đó đã gán giá trị của biến chạy
        ```
            var i = 0;
            for (; i < 10; i++){
                console.log(i);
            }
        ```
    - Cú pháp 3: Bạn cũng có thể bỏ trống ***giá trị thứ hai*** trong cú pháp của vòng lắp for. Lúc này, nếu giá trị thứ hai trả về giá trị ***true*** thì vòng lặp tiếp tục thực thi, nếu là ***false*** thì vòng lặp sẽ dừng lại.

        ```
            for( var i = 0; ; i++){
                console.log(i);
                if(i == 5) break;
                //Nếu bỏ trống giá trị thứ hai thì bắt buộc trong vòng lặp phải có lệnh break, nếu không thì vòng lặp sẽ chạy mãi không dừng lại.
            }
        ```
    - Tuy nhiên, việc bỏ trống các giá trị trong cú pháp của vòng lặp for là không nên. Dù ngắn gọn nhưng nếu dùng không đúng lúc sẽ khiến code của chúng ta khó đọc lại.

2. Thực hành
    - Hãy tạo hàm **getRandNumbers** có 3 tham số là min, max, length. Hàm này sẽ trả về một mảng gồm length phần tử, các giá trị trong mảng là số ngẫu nhiên, giá trị trong khoảng từ min tới max. Gợi ý: ***Math.random() * (max - min) + min*** là cách tạo ra 1 số ngẫu nhiên trong khoảng min - max.

        {{%expand "Kết quả" %}}
            function getRandNumbers (min, max, length){
                var arr=[];
                for(var i=0; i < length; i++){
                arr.push((Math.random() * (max - min) + min));
                }
                return arr;
            }
            // Hãy lưu ý: Vòng lặp phải luôn có điểm dừng nếu không sẽ dẫn đến treo trình duyệt
        {{% /expand%}}


    - Cho trước mảng numbers, hãy viết hàm getTotal trả về tổng giá trị các phần tử của mảng.

        {{%expand "Kết quả" %}}
            function getRandNumbers (min, max, length){
                var arr=[];
                for(var i=0; i < length; i++){
                arr.push((Math.random() * (max - min) + min));
                }
                return arr;
            }
            // Hãy lưu ý: Vòng lặp phải luôn có điểm dừng nếu không sẽ dẫn đến treo trình duyệt
        {{% /expand%}}


    - Cho trước mảng orders là danh sách chứa các khóa học, các mặt hàng này được thể hiện dưới dạng object và đều có 1 key là price để thể hiện giá trị của mặt hàng đó. Bạn hãy hoàn thành hàm getTotal để tính được tổng giá trị của đơn hàng.
    {{%expand "Kết quả" %}}
  
            var orders = [
                {
                    name: 'Khóa học HTML - CSS Pro',
                    price: 3000000
                },
                {
                    name: 'Khóa học Javascript Pro',
                    price: 2500000
                },
                {
                    name: 'Khóa học React Pro',
                    price: 3200000
                }
            ]

            var orders = [
                {
                    name: 'Khóa học HTML - CSS Pro',
                    price: 3000000
                },
                {
                    name: 'Khóa học Javascript Pro',
                    price: 2500000
                },
                {
                    name: 'Khóa học React Pro',
                    price: 3200000
                }
            ]

            function getTotal(order){
                var total=0;
                for(var i=0; i<order.length;i++)
                {
                    total=order[i].price+total;
                }
                return total;
            }
            console.log(getTotal(orders));


            // Expected results:
            getTotal(orders) // Output: 8700000

        {{% /expand%}}


#### Vòng lặp for...in
1. Khái niệm
    - Vòng lặp này thường được sử dụng với mục đích là lặp trong một object chứ không phải trong array hay string giống như hai vòng lặp trên. Số lượng lặp tương ứng với số thuộc tính của object mà ta duyệt.

    - Cú pháp: 
        ```
            for (var key in obj){
                //đoạn code mà bạn muốn thực thi
            }
        ```
        - var key: khai báo biến chạy
        - obj: đố tượng duyệt
    - Ví dụ:
        ```
            // Khai báo mảng
            var myInfo = {
                name: FCJ,
                address: HCM,
                age:10
            }
            // In ra các value trong array myInfo
            for(var key in myInfo){
                console.log(myInfo(key)); 
            }
            // Kết quả: FCJ HCM 10
        ```
2. Thực hành
    - Hoàn thành đoạn code sau để được output như mong muốn
        ```
            // Expected results:
            console.log(run({ name: 'First Cloud Journey', addrees: 'Ho Chi Minh' }));
            // Output:
            // [
            //     "Thuộc tính name có giá trị First Cloud Journey",
            //     "Thuộc tính address có giá trị Ho Chi Minh"
            // ]
        ```
        {{%expand "Kết quả" %}}
            
                function run(info) {
                    var result = [];
                    for (var key in info) {
                        result.push("Thuộc tính " + [key] + " có giá trị " + object[key]);
                    }
                    return result;
                }
        {{% /expand%}}

#### Vòng lặp for...of
1. Khái niệm
    - Vòng lặp for...of cho phép bạn lặp qua các phần tử của một đối tượng iterable trong JavaScript.
    - Cú pháp:
       ```
            for (var value of iterable){
                // đoạn code mà bạn muốn thực thi
            }
       ```     
    - Ví dụ

        ```
            var myCerts = [
                'AWS Certified Solutions Architect - Professional',
                'AWS Certified DevOps Engineer - Professional',
                'AWS Certified SysOps Administrator - Associate'
            ];
            for (var value of myCerts){
                console.log(value)
            }
        ```

#### Vòng lặp While
1. Khái niệm 
    - Vòng lặp while dùng để lặp lại việc thực thi một đoạn code nếu điều kiện mà ta đưa ra vẫn còn đúng.
    - Cú pháp:
        ```
            while(điều kiện){
            // đoạn code mà bạn muốn thực thi
            }
        ```
    - Ví dụ: Dùng vòng lặp while để hiển thị dãy số tăng dần từ 1 đến 9

        ```
            var i = 1; // khai báo biến i
            while(i<10){
                console.log(`Kết quả: ${i}`) // in ra màn hình
                i++; // Câu lệnh này giúp cho điều kiện dần trở thành bị SAI
            }
        ```

#### Vòng lặp do...while
1. Khái niệm
    - Tương tự như vòng lặp while, vòng lặp do while dùng để lặp lại việc thực thi một đoạn mã nếu điều kiện mà ta đưa ra vẫn còn đúng.
    - Tuy nhiên, đối với vòng lặp do while thì ở lần đầu tiên đoạn mã sẽ được thực thi luôn mà không cần phải kiểm tra điều kiện (đó chính là điểm khác nhau giữa vòng lặp while và do while)
    - Cú pháp: 
        ```
        do{
            // Đoạn code mà bạn muốn thực thi
        }while(điều kiện)
        ```
    - Ví dụ: Dùng vòng lặp while để hiển thị dãy số giảm dần từ 9 xuống 1
        ```
        var i = 0;
        do{
            i++;
            console.log(`Kết quả: ${i}`);
        }while(i<9)
        ```
2. Thực hành
    - Viết một đoạn code mô tả số lần nhập mật khẩu ( không quá 3 lần nhập). Nếu nhập quá 3 lần sẽ in ra thông báo **kiểm tra lại mật khẩu**
    - Output:
        ```
        Nhập lần mật khẩu: 1
        Nhập lần mật khẩu: 2
        Nhập lần mật khẩu: 3
        Kiểm tra lại mật khẩu
        ```

        {{%expand "Kết quả" %}}
            var i = 0;
            var isSucess = false;
            do {
                i++;
                if(i == 4) {
                console.log("Kiểm tra lại mật khẩu"); 
                break;
                };
                console.log(`Nhập mật khẩu lần: ${i}`);
            }while(!isSucess && i < 3 )
                        
        {{% /expand%}}

#### Break và Continue trong vòng lặp
1. Break
    - Dùng để thoát khỏi vòng lặp ngay lập tức
    - Khi gặp Break, vòng lặp sẽ dừng thực thi và chuyển sang phần code sau vòng lặp.
    - Ví dụ:
        ```
            for (var i = 0; i < 10; i++) {
                console.log(i);
                if (i === 5) {
                    break;
                }
            }
        ```
2. Continue
    - Dùng để bỏ qua phần còn lại của vòng lặp hiện tại và chuyển sang lần lặp tiếp theo.
    - Khi gặp continue, vòng lặp sẽ tiếp tục thực thi từ đầu với lần lặp tiếp theo
    - Ví dụ: 
        ```
            for (var i = 0; i < 10; i++) {
                if (i % 2 === 0) {
                    continue;
                }
            console.log(i);
            }

        ```
#### Vòng lặp lồng nhau - Nested loop
1. Khái niệm
    - Vòng lặp lồng nhau là khi một vòng lặp được đặt bên trong một vòng lặp khác. Ví dụ, một vòng lặp for có thể được đặt bên trong một vòng lặp while.
    - Cú pháp:
        ```
            for (var i = 0; i < 10; i++) {
                for (var j = 0; j < 5; j++) {
                    // Khối mã được thực thi lặp lại cho mỗi giá trị của i và j
                }
            }
        ```

        - Vòng lặp ngoài (vòng lặp for) sẽ lặp lại 10 lần.
        - Vòng lặp trong (vòng lặp for) sẽ lặp lại 5 lần cho mỗi lần lặp của vòng lặp ngoài.

    - Ví dụ:
        ```
            var arr = [
                [1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]
            ];

            for (var i = 0; i < arr.length; i++) {
                for (var j = 0; j < arr[i].length; j++) {
                    console.log(arr[i][j]);
                 }
            }
        ```
    