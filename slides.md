---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss
hideInToc: true
---

# Xây dựng website
# đọc truyện tranh

Nguyễn Thế Sinh - 18810340136

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---
---


<Toc />


<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
layout: image-left
image: /images/slide_3_001.png
---

# Giới thiệu đề tài


### Lý do chọn đề tài:
  - Các website đọc truyện hiện nay đều quá cũ hoặc có quá nhiều quảng cáo
  - Mong muốn tạo ra 1 nền tảng để mọi người có thể chia sẻ sở thích đọc truyện

<br />

### Mục đích tạo ra website:
  - Tối giản về giao diện
  - Có tốc độ tải nhanh
  - Giúp người đọc chia sẻ truyện với nhau


---
layout: intro
---

# Các nội dung thực hiện

---
layout: image-right
image: /images/slide_5_001.png
---
## Khảo sát thực trạng

<br />

### Khảo sát 2 website đọc truyện lớn:
-	blogtruyen.vn
-	cuutruyen.net

<br />
<br />

### Khảo sát với 2 tiêu chí
-	Giao diện trang
-	Các tính năng tiêu biểu của trang


---
class: px-20
hideInToc: true
layout: center
---

## Kết quả khảo sát

<br />
<br />

|   |blogtruyen.vn   |cuutruyen.net   |
|---|---|---|
|Giao diện   | <ul><li>Cũ và lỗi thời</li> <li>Quảng cáo xuất hiện nhiều và dày đặc hơn</li></ul>|  <ul><li>Hiện đại, tối giản,  bắt mắt</li> <li>Quảng cáo xuất hiện ít, được bố trí hợp lý</li></ul>|
|Tính năng   | <ul><li>Cho phép người dùng tự upload và quản lý truyện</li><li>Tìm kiếm với bộ lọc phức tạp</li></ul> | <ul><li>Không có tính năng đăng tải </li><li>Chỉ có tìm kiếm theo tên</li></ul>|

---
preload: false
---

## Bài toán đặt ra

<p>Xây dựng được một website truyện tranh nơi mà người truy cập có thể tìm kiếm và đọc truyện, người dùng có thể đăng nhập (hoặc đăng ký) để theo dõi, đánh giá truyện mình đọc. Đồng thời, người dùng có tài khoản sẽ có khả năng đăng tải và quản lý truyện của chính họ.</p>

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0 rounded-36"
      src="/images/sabe_think.png"
    />
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

---
layout: statement
---

## Phân tích và thiết kế hệ thống

---
layout: center
hideInToc: true
---


### Use case tổng quát

<div class='w-md mt-5'>
  <img src='/images/use-case.jpg' alt='general use case' >
</div>

---
layout: center
hideInToc: true
---
### Biểu đồ thực thể liên kết

<div class='w-xl mt-5'>
  <img src='/images/er.png' alt='general use case' >
</div>


---
layout: statement
hideInToc: true
---


## Xây dựng hệ thống


---
layout: two-cols
---
### Front-end

<div class='flex flex-col gap-5 mt-5'>
  <img alt='nextjs' src='/images/nextjs.png' width='400'>
  <img alt='vercel' src='/images/vercel.png' width='400'>
</div>

::right::

### Back-end
<div class='flex flex-col gap-5 mt-5'>
  <img alt='pocket-base' src='/images/pocket-base.png' width='400'>
  <img alt='dgoc' src='/images/dgoc.png' width='400'>
</div>

---
layout: fact
---

<img src='/images/explain_nextjs.png'>

---
layout: statement
---
# Kết quả thực hiện

---
layout: image-left
image: /images/google_light_house.png
hideInToc: true
---

### Các tính năng đã đạt được:

- Tìm kiếm truyện với bộ lọc
- Đăng tải và quản lý truyện
- Xem thông tin truyện
- Đọc các chương truyện
- Ghi nhớ lịch sử đọc truyện
- Theo dõi và bình luận truyện
- Nhận thông báo khi có chương mới của truyện
- Quản lý tài khoản cá nhân

---
layout: fact
---

Thank you for listening.