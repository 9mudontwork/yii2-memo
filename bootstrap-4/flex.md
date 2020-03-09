# การใช้ Flex

{% embed url="https://getbootstrap.com/docs/4.4/utilities/flex/" %}



ตัวอย่าง กำหนด flex กระจาย div  ถ้าเต็ม wrap ขึ้นบรรทัดใหม่

```markup
<div class="d-flex justify-content-between flex-wrap">
    <div></div>
    <div></div>
</div>
```

**class ต่อไปนี้อยู่ใน div .d-flex**

กระจาย div item

```text
.justify-content-sm md lg xl

// ซ้ายสุด
.justify-content-start

// ขวาสุด
.justify-content-end

// กลาง จากซ้ายขวา
.justify-content-center

// กระจายชิดขอบ
.justify-content-between

// กระจาย ให้พอดี แต่ไม่ชิดขอบ
.justify-content-around
```

ตำแหน่ง div item

```markup
.align-items-sm md lg xl

// ชิดบน
.align-items-start

// ชิดล่าง
.align-items-end

// กลาง จากบนล่าง
.align-items-center

// ปรับให้เท่ากันกับ อันอื่นๆ
.align-items-baseline

// ยืดให้เต็มบนล่าง
.align-items-stretch


จัดตำแหน่งของตัวมันเอง ใน div item

.align-self-sm md lg xl

.align-self-start
.align-self-end
.align-self-center
.align-self-baseline
.align-self-stretch
```

