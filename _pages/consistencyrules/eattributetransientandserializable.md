---
layout: page
title:  "Consistency Rule"
permalink: "/eattributetransientandserializable/"
---

Hello World

```
OCL

constraint TheAttributeIsNotTransientSoItMustHaveADataTypeThatIsSerializable
  message 'The attribute is not transient so it must have a data type that is serializable'

context EAttribute

inv TheAttributeIsNotTransientSoItMustHaveADataTypeThatIsSerializable:
  self.transient and self.eType.oclIsTypeOf(EDataType) implies (self.eType.oclAsType(EDataType).serializable)
```
