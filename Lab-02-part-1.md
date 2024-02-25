# การทดลองสัปดาห์ที่ 5.1 #
## ศึกษา data structure  และ methods ของ predefined type ในภาษา C#  ##


### Learning Outcome ###
1. นักศึกษารู้จัก predefined type และบอกได้ว่ามีอะไรบ้าง
2. นักศึกษารู้จักองค์ประกอบของ predefined type แต่ละชนิดและสามารถสร้างแผนภาพอธิบาย type เหล่านั้นได้

### ความรู้เบื้องต้น ###
#### 1.  Predefined type ในภาษา C# ####

Predefined type ในภาษา C# มีอยู่ด้วยกัน 16 ชนิด (สำหรับคนที่ update เป็น C# version 9 แล้ว จะมี 18 ชนิด) ดังรูปที่ 1


![](./Pictures/PredefinedType.png)


<p align = "center"> <b>รูปที่ 1</b>  predefined type ในภาษา C# </p>

#### 2. การเข้าถึง predefined type โดยใช้ Visual Studio IDE ####
เราสามารถอาศัยเครื่องมือใน text editor ของ Visual Studio เข้าถึงนิยามของ predefined type ได้โดยการกดปุ่ม F12 หรือ กดปุ่ม Ctrl บนคีย์บอร์ดแล้วใช้เมาส์คลิกที่ขื่อของ Type นั้นๆ

##### ลำดับขั้นการทดลอง #####

1. สร้าง console project ใน Visual studio สมมติว่าตั้งชื่อ project เป็น `Week05_Lab1`



2. แก้ไขไฟล์ `program.cs` มีเนื้อหาดังต่อไปนี้


```cs
class Program
{
    sbyte sb;
    byte bt;
    short sh;
    ushort ush;
    int ii;
    uint ui;
    long lo;
    ulong ul;
    float fl;
    double db;
    bool bl;
    char ch;
    decimal de;

    object ob;
    string st;
    dynamic dy;

    static void Main(string[] args)
    {

    }
}
```

<p align = "center"> <b>รูปที่ 2 </b> Source code  ของ program.cs</p>


3. กดปุ่ม Ctrl แล้วใช้เมาส์คลิกที่ `sbyte` โปรแกรม Visual Studio จะเปิดไฟล์ใหม่ขึ้นมา ซื่งมือเนื้อหาของ `System.Sbyte`

![รูปที่ 2](./Pictures/Lab5_1_Pic2.png)


จะสังเกตได้ว่าในบรรทัดที่ 12 มีการสร้าง type ของข้อมูลเป็น `struct` ซึ่งมีการ สืบทอดมาจาก `Interface` หลายชนิด (จะได้เรียนเรื่อง `interface` ในภายหลัง)

ในบรรทัดที่ 18 และ 22 มีตัวแปรแบบ `public const SByte` จำนวนสองตัว ซึ่งทำหน้าที่บอกค่าสูงสุด (`MaxValue`) และค่าต่ำสุด  (`MinValue`) ที่สามารถเก็บในตัวแปรชนิดนี้ 

จากค่า `MaxValue`  และ   `MinValue` ทำให้เรารู้ได้ว่าตัวแปรที่สร้างจาก type นี้มีขนาด 8 บิตแบบคิดเครื่องหมาย นั่นคือต้องใช้บิดซ้ายสุดจำนวน 1 บิตเป็นตัวเก็บเครื่องหมาย (ถ้าบิตนี้มีค่า 0 คือจำนวนเต็มบวก ถ้าเป็น 1 จะเป็นจำนวนเต็มลบ) ดังนั้นจึงสามารถมีข้อมูลได้ 7 บิต (แทนค่าเป็นเลขฐานสิบได้ 0-127)

`1 0000000` ถึง `1 1111111` เป็นค่าลบ

`0 0000000` ถึง `0 1111111` เป็นค่าบวก


บรรทัดที่ 27 ถึง 338 จะเป็น methods ของชนิดข้อมูลนี้ ทำให้เรารู้ว่าสามารถทำอะไรกับชนิดข้อมูลนี้ได้บ้าง  

ถ้าลองคลิ่ folding โดยการคลิกที่เครื่องหมาย [+] เราจะเห็นข้อความอธิบายอยู่ใน comment ดังรูปที่ 3

![รูปที่ 3](./Pictures/Lab5_1_Pic3.png)

<p align = "center"> <b>รูปที่ 3</b> คำอธิบาย method ของ SByte </p>

4. วาดไดอะแกรมของ type นี้ด้วย plantuml

``` puml
@startuml
class SByte
{
  + Maxvalue : SByte
  + Minvalue : SByte

  + Parse(...) : SByte 
  + TryParse(...) : SByte
  + CompareTo(...) : SByte
  + Equals(...) : bool
  + GatHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```

เมื่อ render ด้วยโปรแกรม plantuml แล้วจะได้คลาสไดอะแกรมดังนี้

![รูปที่ 3](./Pictures/SByte_uml.png)

<p align = "center"> <b>รูปที่ 4</b> diagram สำหรับ SByte </p>


----------
__หมายเหตุ__ 

รูปแบบของการเขียนรายละเอียดของตัวแปรและ function ใน class diagram คือ
```
< +|-|# > name [ : < return-type > ]
```
เมื่อ
```
+ คือการเข้าถึงแบบ public
- คือการเข้าถึงแบบ private
# คือการเข้าถึงแบบ protected

< > หมายถึงเป็นส่วนที่ต้องมี (required)
[ ] หมายถึงเป็นส่วนที่ไม่ต้องก็ได้ (optional)

เช่น 
 + Maxvalue : SByte     //  ในกรณีที่ต้องการระบุให้ชัดเจนเนื่องจากรู้ชนิดล่วงหน้าแล้ว
 หรือ 
 + Maxvalue             // ในกรณีที่ยังไม่รู้ชนิดล่วงหน้า 

```
ในกรณีที่ชื่อฟังก์ชันเหมือนกันแต่มี parameter ต่างกันให้เขียน parameter  เป็น (...) แล้วใช้ฟังก์ชันเดียวเท่านั้น

----------

## แบบฝึกหัด ##

เขียนโค้ด plantuml สำหรับ type ชนิดอื่นๆ โดยใช้วิธีเดียวกันกับขั้นตอนที่ 3  เพื่อสร้าง diagram สำหรับ predefined type ทุกชนิด
# sByte
```plantuml   
@startuml
class sbyte
{
  + MaxValue : sbyte
  + MinValue : sbyte

  + Parse(...) : sbyte
  + TryParse(...) : sbyte
  + CompareTo(...) : sbyte
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/0451fef4-fb0e-45ee-9718-6a7a847f6b11)

#  byte
```plantuml  
@startuml
class byte
{
  + MaxValue : byte
  + MinValue : byte

  + Parse(...) : byte
  + TryParse(...) : byte
  + CompareTo(...) : byte
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/89648f64-dffe-40ee-91ab-c4e08da85092)

# short
```plantuml  
@startuml
class short
{
  + MaxValue : short
  + MinValue : short

  + Parse(...) : short
  + TryParse(...) : short
  + CompareTo(...) : short
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/33223bc1-b1cf-48c2-9ca1-145d2a30141d)

#  ushort
```plantuml
@startuml
class ushort
{
  + MaxValue : ushort
  + MinValue : ushort

  + Parse(...) : ushort
  + TryParse(...) : ushort
  + CompareTo(...) : ushort
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/956fc969-9086-4e93-acb0-52496b59354d)

# int
```plantuml
@startuml
class int
{
  + MaxValue : int
  + MinValue : int

  + Parse(...) : int
  + TryParse(...) : int
  + CompareTo(...) : int
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/0db6d1cb-cdf7-422d-a27e-94353478ffce)

# uint
```plantuml
@startuml
class uint
{
  + MaxValue : uint
  + MinValue : uint

  + Parse(...) : uint
  + TryParse(...) : uint
  + CompareTo(...) : uint
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml


```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/a05be4de-997b-4a65-94e4-adc47af0b271)

# long
```plantuml
@startuml
class long
{
  + MaxValue : long
  + MinValue : long

  + Parse(...) : long
  + TryParse(...) : long
  + CompareTo(...) : long
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml

```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/38031847-cc72-43da-a899-53eb09e7000a)

# ulong
```plantuml
# ulong
@startuml
class ulong
{
  + MaxValue : ulong
  + MinValue : ulong

  + Parse(...) : ulong
  + TryParse(...) : ulong
  + CompareTo(...) : ulong
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml

```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/a6678e78-4680-4e04-9337-624d8d47a4dd)

#  float
```plantuml
@startuml
class float
{
  + MaxValue : float
  + MinValue : float
  + PositiveInfinity : float
  + NegativeInfinity : float
  + NaN : float

  + Parse(...) : float
  + TryParse(...) : float
  + CompareTo(...) : int
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/eac93290-79c9-4744-af53-880c7b253c2d)

#  double
```plantuml
@startuml
class double
{
  + MaxValue : double
  + MinValue : double
  + PositiveInfinity : double
  + NegativeInfinity : double
  + NaN : double

  + Parse(...) : double
  + TryParse(...) : double
  + CompareTo(...) : int
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml

```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/ed1cd3be-d40e-4c2c-be16-fc535791983d)

#  bool
```plantuml
@startuml
class bool
{
  + TrueString : string
  + FalseString : string

  + Parse(...) : bool
  + TryParse(...) : bool
  + CompareTo(...) : bool
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml

```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/085065a0-27ee-4779-ac37-e8d90c30bb2e)

 #  char
```plantuml
@startuml
class char
{
  + MaxValue : char
  + MinValue : char

  + Parse(...) : char
  + TryParse(...) : char
  + CompareTo(...) : char
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/c76b0eb4-e385-48e6-8ccb-f4a42061b0f5)

  #  decimal
```plantuml
@startuml
class decimal
{
  + Currency(...) : decimal

  + decimal(Currency value) : decimal
}
@enduml

```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/4bdf7b7b-38bf-41df-a43f-2fee971b0d10)

#     object 
```plantuml
@startuml
class object
{
  + Type(...) : GetType
}
@enduml




```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/63842a38-a340-4655-8159-de7d783c8dc7)


  #   string

```plantuml
@startuml
class string
{
  + Intern(...) : string
  + IsInterned(...) : string
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/4f03ab92-05d1-4365-b729-24d088ced7ea)

 #  dynamic
```plantuml
@startuml
class dynamic
{
  # Dynamic type in C#
}
@enduml
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-02/assets/144197034/20c81f31-c3b9-4907-b788-2bdb7824eaa6)

<br>
ใน UML diagram ที่แสดง class dynamic นั้น 
บ่งบอกว่ามันเป็น dynamic type ซึ่งไม่ระบุประเภทข้อมูลในลักษณะเดียวกับที่เกิดขึ้นใน C# ซึ่งมีความยืดหยุ่นในการใช้งานประเภทข้อมูลขณะ runtime
<br>       
