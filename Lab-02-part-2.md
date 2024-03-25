# การทดลองสัปดาห์ที่ 5.2 #
## แสดงรายละเอียดของ predefined type ในภาษา C#  ##


### Learning Outcome ###
1. นักศึกษารู้จัก predefined type และบอกได้ว่ามีอะไรบ้าง
2. นักศึกษาสามารถเขียนโปรแกรมเพื่อรายงานค่าเฉพาะตัวของ predefined type ได้

## แบบฝึกหัด ##

แก้ไขโค้ดตัวอย่าง ให้รายงานรายละเอียดของ predefine type ได้ครบถ้วน

Type ใดที่ไม่มี properties ที่กำหนดให้แสดงก็ให้เว้นไว้ หรือใช้การขีด (`-`)
```cs
using System;

sbyte sb = new sbyte();
byte bt = new byte();
short sh = new short();
ushort ush = new ushort();
int ii = new int();
uint ui = new uint();
long lo = new long();
ulong ul = new ulong();
float fl = new float();
double db = new double();
bool bl = new bool();
char ch = new char();
decimal de = new decimal();

object ob = new object();
string st = new string(new char[] { });
dynamic dy = new System.Dynamic.ExpandoObject();

Console.WriteLine($"Declaration\tType name\tType code\tMaximum Value\tMinimum Value");
Console.WriteLine($"----------------------------------------------------------------------------");
Console.WriteLine($"sbyte sb\t{sb.GetType()}\t{Type.GetTypeCode(sb.GetType())}\t\t{sbyte.MaxValue}\t\t{sbyte.MinValue}");
Console.WriteLine($"byte bt\t\t{bt.GetType()}\t{Type.GetTypeCode(bt.GetType())}\t\t{byte.MaxValue}\t\t{byte.MinValue}");
Console.WriteLine($"short sh\t{sh.GetType()}\t{Type.GetTypeCode(sh.GetType())}\t\t{short.MaxValue}\t\t{short.MinValue}");
Console.WriteLine($"ushort ush\t{ush.GetType()}\t{Type.GetTypeCode(ush.GetType())}\t\t{ushort.MaxValue}\t\t{ushort.MinValue}");
Console.WriteLine($"int ii\t\t{ii.GetType()}\t{Type.GetTypeCode(ii.GetType())}\t\t{int.MaxValue}\t\t{int.MinValue}");
Console.WriteLine($"uint ui\t\t{ui.GetType()}\t{Type.GetTypeCode(ui.GetType())}\t\t{uint.MaxValue}\t\t{uint.MinValue}");
Console.WriteLine($"long lo\t\t{lo.GetType()}\t{Type.GetTypeCode(lo.GetType())}\t\t{long.MaxValue}\t\t{long.MinValue}");
Console.WriteLine($"ulong ul\t{ul.GetType()}\t{Type.GetTypeCode(ul.GetType())}\t\t{ulong.MaxValue}\t\t{ulong.MinValue}");
Console.WriteLine($"float fl\t{fl.GetType()}\t{Type.GetTypeCode(fl.GetType())}\t\t{float.MaxValue}\t\t{float.MinValue}");
Console.WriteLine($"double db\t{db.GetType()}\t{Type.GetTypeCode(db.GetType())}\t\t{double.MaxValue}\t\t{double.MinValue}");
Console.WriteLine($"bool bl\t\t{bl.GetType()}\t{Type.GetTypeCode(bl.GetType())}\t\t{bool.TrueString}\t\t{bool.FalseString}");
Console.WriteLine($"char ch\t\t{ch.GetType()}\t{Type.GetTypeCode(ch.GetType())}\t\t{(int)char.MaxValue}\t\t{(int)char.MinValue}");
Console.WriteLine($"decimal de\t{de.GetType()}\t{Type.GetTypeCode(de.GetType())}\t\t{decimal.MaxValue}\t\t{decimal.MinValue}");

Console.WriteLine($"object ob\t{ob.GetType()}\t- \t\t{decimal.MaxValue}\t{decimal.MinValue}");
Console.WriteLine($"string st\t{st.GetType()}\t{Type.GetTypeCode(st.GetType())}\t- \t- ");
Console.WriteLine($"dynamic dy\t{dy.GetType()}\t- \t- \t- ");
Console.WriteLine("============================================================================");

```

![](./Pictures/Lab5_2_Pic1.png)
