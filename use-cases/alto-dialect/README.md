#ALTO dialects#
Libraries often need to adapt the ALTO schema. These local formats generally include minor changes to the LoC schema, in order to fulfill specific needs. These differences can be:
 - new attributes 
 - patterns added on attributes 
 - attributes or elements made mandatory 
 - restraints on enumeration  

Objectives : Let an ALTO producer redefining/overriding some parts of the ALTO schema, considering that the “copy and hack schema” solution must be avoided. 

Implementation : W3C XML Schema provides a mechanism for updating a type definition. The updated type derives from itself. This mechanism is based on the xs:redefine element, which first acts as an xs:include element. Then, the included types can be redefined, with two mechanisms:
 - Restriction: adding some constraints on existing types
 - Extension: creating new elements or attributes

