# การทดลองสัปดาห์ที่ 5.2 #
## แสดงรายละเอียดของ predefined type ในภาษา C#  ##


### Learning Outcome ###
1. นักศึกษารู้จัก predefined type และบอกได้ว่ามีอะไรบ้าง
2. นักศึกษาสามารถเขียนโปรแกรมเพื่อรายงานค่าเฉพาะตัวของ predefined type ได้

## แบบฝึกหัด ##

แก้ไขโค้ดตัวอย่าง ให้รายงานรายละเอียดของ predefine type ได้ครบถ้วน

Type ใดที่ไม่มี properties ที่กำหนดให้แสดงก็ให้เว้นไว้ หรือใช้การขีด (`-`)
```cs
sbyte sb = new sbyte();  // create new object
byte bt = new byte();
short sh;                 
ushort ush;
int ii = new int();
uint ui;
long lo;
ulong ul;
float fl;
double db;
bool bl;
char ch;
decimal de;

object ob = new object();
string st = new string("");
dynamic dy;


Console.WriteLine($"Declaration\tType name\tType code\tMaximum Value\tMinimum Value");
Console.WriteLine($"----------------------------------------------------------------------------");
Console.WriteLine($"sbyte sb\t{sb.GetType()}\t{sb.GetTypeCode()}\t\t{sbyte.MaxValue}\t\t{sbyte.MinValue}");
Console.WriteLine($"byte bt\t\t{sb.GetType()}\t{bt.GetTypeCode()}\t\t{byte.MaxValue}\t\t{byte.MinValue}");
Console.WriteLine($"short sh");
Console.WriteLine($"ushort ush");
Console.WriteLine($"int ii\t\t{ii.GetType()}\t{ii.GetTypeCode()}\t\t{int.MaxValue}\t{int.MinValue} ");

Console.WriteLine($"object ob\t{ob.GetType()}");
Console.WriteLine($"string st\t{st.GetType()}\t{st.GetTypeCode()} ");

Console.WriteLine("============================================================================");

```

![](./Pictures/Lab5_2_Pic1.png)


### แก้ไขโค้ดตัวอย่าง ให้รายงานรายละเอียดของ predefine type ได้ครบถ้วน
#### ส่งงาน นางสาว อัญชิสา เพชรน้อย 65030289
![ภาพ](https://github.com/03376836-OOP-2566/03376836-OOP-2566-Lab-02/assets/144197034/3fcfbb25-7b56-44b9-a485-f5ffa0aa814e)
![ภาพ](https://github.com/03376836-OOP-2566/03376836-OOP-2566-Lab-02/assets/144197034/8223240c-36af-423b-97e4-1f2ebcdbedb6)
![ภาพ](https://github.com/03376836-OOP-2566/03376836-OOP-2566-Lab-02/assets/144197034/1da666eb-965c-4fc1-89d7-1212dd2e16d8)
![ภาพ](https://github.com/03376836-OOP-2566/03376836-OOP-2566-Lab-02/assets/144197034/e62783c4-c246-4ba9-bd27-1788b51126c5)

![ภาพ](https://github.com/03376836-OOP-2566/03376836-OOP-2566-Lab-02/assets/144197034/622603f4-aaa8-48a3-b425-8b6ac56283f1)









