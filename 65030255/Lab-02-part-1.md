## เขียนโค้ด plantuml สำหรับ type ชนิดอื่นๆ โดยใช้วิธีเดียวกันกับขั้นตอนที่ 3 เพื่อสร้าง diagram สำหรับ predefined type ทุกชนิด

# sByte
```plantuml   
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

# byte
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

# ushort
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

# ulong
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
```

# float
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

# Double
```plantuml
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

# bool
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

# char
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

# decimal
```plantuml
@startuml
class decimal
{
  + Currency(...) : decimal
  + decimal(Currency value) : decimal
}
@enduml
```

# object
```plantuml
@startuml
class object
{
  + Type(...) : GetType
}
@enduml
```

# string
```plantuml
@startuml
class string
{
  + Intern(...) : string
  + IsInterned(...) : string 
}
@enduml
```

# dynamic
### dynamic ใน C# ไม่ได้มีการกำหนดประเภทข้อมูลแบบมีโครงสร้าง (structure) และมีการติดต่อกับทุกประเภทข้อมูลใน runtime โดยไม่มีการตรวจสอบประเภทใน compile time จึงไม่มีข้อมูลที่แน่นอน
