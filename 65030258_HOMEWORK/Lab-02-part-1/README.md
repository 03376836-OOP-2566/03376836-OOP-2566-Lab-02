# HOMEWORK 1/4/2024
## แบบฝึกหัด
### เขียนโค้ด plantuml สำหรับ type ชนิดอื่นๆ โดยใช้วิธีเดียวกันกับขั้นตอนที่ 3 เพื่อสร้าง diagram สำหรับ predefined type ทุกชนิด

# SByte
```plantuml   
@startuml
class SByte
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
#Sittha Klaphanich
```
![](./Images/SByte.png)

# Byte
```plantuml
@startuml
class Byte
{
  + MaxValue : byte
  + MinValue : byte

  + Parse(...) : byte
  + TryParse(...) : byte
  + CompareTo(...) : Byte
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
#Sittha Klaphanich
```
![](./Images/Byte.png)

# Short
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
#Sittha Klaphanich
```
![](./Images/Short.png)

# UShort
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
#Sittha Klaphanich
```
![](./Images/UShort.png)

# Int
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
#Sittha Klaphanich
```
![](./Images/Int.png)

# UInt
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
#Sittha Klaphanich
```
![](./Images/UInt.png)

# Long
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
#Sittha Klaphanich
```
![](./Images/Long.png)

# ULong
```plantuml
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
#Sittha Klaphanich
```

![](./Images/ULong.png)


# Float
```plantuml
@startuml
class float
{
  + MaxValue : float
  + MinValue : float
  + Epsilon  : float
  + NegativeInfinity : float
  + PositiveInfinity : float
  + NaN : float


  + Parse(...) : float
  + TryParse(...) : float
  + CompareTo(...) : float
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
#Sittha Klaphanich
```
![](./Images/Float.png)


# Double
```plantuml
@startuml
class double
{
  + MaxValue : double
  + MinValue : double
  + Epsilon  : double
  + NegativeInfinity : double
  + PositiveInfinity : double
  + NaN : double

  + Parse(...) : double
  + TryParse(...) : double
  + CompareTo(...) : double
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
#Sittha Klaphanich
```
![](./Images/double.png)

# Bool
```plantuml
@startuml
class bool
{
  + TrueLiteral : string
  + FalseString : string


  + Parse(...) : string
  + TryParse(...) : bool
  + CompareTo(...) : bool
  + Equals(...) : bool
  + GetHashCode() : int
  + GetTypeCode() : TypeCode
  + ToString(...) : string
}
@enduml
#Sittha Klaphanich
```
![](./Images/Bool.png)

# Char
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
#Sittha Klaphanich
```
![](./Images/Char.png)

# Decimal
```plantuml
@startuml
class decimal
{
  + Currency(...) : decimal
}
@enduml
#Sittha Klaphanich
```
![](./Images/decimal.png)

# Object
```plantuml
@startuml
class object
{
  + Type(...) : GetType
}
@enduml
#Sittha Klaphanich
```
![](./Images/object.png)

# String
```plantuml
@startuml
class string
{
  + Intern(...) : string
  + IsInterned(...) : string 
}
@enduml
#Sittha Klaphanich
```
![](./Images/string.png)
