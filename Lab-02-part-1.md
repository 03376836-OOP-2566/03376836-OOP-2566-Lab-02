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
### sByte ###
```
@startuml
class sbyte
{
  + Maxvalue : sbyte
  + Minvalue : sbyte
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/54ae0647-c126-4503-82cf-4488a749eacd)

### byte ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/208e17f3-81a0-446b-9c29-1bc273d46a92)
### short ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/e654be0d-2a8e-456a-93d2-9dbb53ca0da1)

### ushort ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/61406dcc-5efc-431c-ab7b-d43c0cc57b2d)

### int ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/39436d1a-832c-445d-a052-880f8fb7dc1d)
### uint ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/b68bfa2b-efa1-474f-8f0f-822e9e8f88a7)

### long ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/79340ce2-a766-448b-8885-5284a9d3dd59)

### ulong ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/15535b10-3b3a-41db-942c-c2d1ca9d3501)

### float ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/dd440b9c-e772-4360-ac03-86d213df5940)

### double ###
```
@startuml
class Double
{
  + MaxValue : Double
  + MinValue : Double
  + PositiveInfinity : Double
  + NegativeInfinity : Double
  + NaN : Double
  + Parse(...) : Double 
  + TryParse(...) : Double
  + CompareTo(...) : Double
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
```
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/c874debc-26b7-4cad-9d42-d403d4aad799)

### bool ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/12959402-6a8e-4362-b4d9-fdfd42c2024b)

### char ###
```
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
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/a7464062-7813-4a0e-b3bb-ef19d9cc9799)

### decimal ###
```
@startuml
class decimal
{
  + Currency(...) : decimal
  + decimal(Currency value) : decimal
}
@enduml
```
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/86492725-d454-478e-ba53-5bd92006a6dc)

### object ###
```
@startuml
class object
{
  + Type(...) : GetType
}
@enduml
```
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/b926ded1-7f37-4b1a-b7e8-448749d22d2a)

### string ###
```
@startuml
class string
{
  + Intern(...) : string
  + IsInterned(...) : string 
}
@enduml
```
![image](https://github.com/kanoksiriboonkam/03376836-OOP-2566-Lab-02/assets/144196048/c43c77fc-ee86-4d53-9c5c-bebb0ef29e11)

### dynamic ###
dynamic ใน C# ไม่ได้มีการกำหนดประเภทข้อมูลแบบมีโครงสร้าง (structure) และมีการติดต่อกับทุกประเภทข้อมูลใน runtime โดยไม่มีการตรวจสอบประเภทใน compile time จึงไม่มีข้อมูลที่แน่นอน
