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


# UInt
```plantuml
@startuml
class int
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

# ULong
```plantuml
@startuml
class long
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

# Float
```plantuml
@startuml
class long
{
  + MaxValue : float
  + MinValue : float

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

# Double
```plantuml
@startuml
class double
{
  + MaxValue : double
  + MinValue : double

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


# Bool
```plantuml
@startuml
class bool
{
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
