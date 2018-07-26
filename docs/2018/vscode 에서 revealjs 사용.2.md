## yuml

![](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuIhEpimhI2nAp5N8pS_BJyueoizDLIWfAatbSifFKj2rKt3CoKnELR1Io4ZDoSbFIU5oICrB0Me40000)

note:

- http://www.plantuml.com/plantuml/uml/
  @startuml
  skinparam monochrome reverse
  User -> Server : 1
  Server -> Google : 2
  Google -> Server : 3
  @enduml

--

## 노트 작성

**showNotes** 속성 을 정의합니다.

```
showNotes: "true";
```

노트 안보이게, 기본값은 **false**

```
showNotes: "false";
```

note:

- 노트에 작성을 하면 발표자만 확인할 수 있습니다.
- 옵션을 작성하여 모두 보이게도 할 수 있습니다.
- 안보이게 하는 경우, 기본값은 **false** 이므로 작성하지 않아도 됩니다.

---
