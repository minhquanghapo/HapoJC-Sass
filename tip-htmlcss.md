# Tip for Html/Css

```sh
Làm thế nào để code html/css ngắn và tinh gọn hơn?
```
## Body
Nên đặt font chữ, font-size....vv chung nhất vào phần body cũng như các thành phần khác của trang ví dụ:
```
body {
	font: 16px Lato, sans-serif;
}

button {
	font: 14px lato-regular;
	color: white;
}
```

## Shorthand 
Nên sử dụng dạng [shorthand](https://www.sitepoint.com/introduction-css-shorthand/) để code ngắn gọn hơn.
```
padding: $top $right $bottom $left;
margin: $top $right $bottom $left;
border-width: $top $right $bottom $left;
border-radius: $top $right $bottom $left;
background: $color $url(image) $repeat $position;
font: $style $variant $weight $size $family; 
```
## Dàn đều các div theo hàng ngang
Sử dụng thuộc tính [justify-content](https://www.w3schools.com/cssref/css3_pr_justify-content.asp):
```
justify-content: space around;
```
hoặc 
```
justify-content: space-betweeen.
```
## Đặt phần tử vào giữa một khung
Sử dụng thuộc tính [transform](https://www.w3schools.com/cssref/css3_pr_transform.asp):

+Chiều ngang
```
left: 50%;
transform: translate(-50%,0);
```
+Chiều dọc
```
top: 50%;
transform: translate(0,-50%);
```
+Chính giữa
```
top: 50%;
left: 50%;
transform: translate(-50%,-50%);
```

## Button
**Nên:**
		- *Không xét ~~width~~ và ~~height~~ cho button.*
		- *Dùng button đúng chỗ*
		- *Xét padding cho button*
```
padding: 12px 18px;
```

## CSS cho các lớp có cùng thành phần tên
Khi ta muốn CSS cho các class có cùng thành phần tên đầu có dạng như:
```
.col-cl-1 {}.col-cl-2 {}
......
```
có thể dùng
```
div[class^="col-cl"] {

}
```
Các class có cùng thành phần trong tên có dạng như:
```
.cl-col-1{},.sml-col-2{}.....vv
```
có thể dùng
```
div[class*=" col"{

}
```