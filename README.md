# XML 

| Title | Remark |
|-------|--------|
| [Introduction to XML](https://github.com/potatoscript/xml/wiki/Introduction-to-XML) | Learn the basics of XML, its structure, and common use cases. |
| [XML Syntax](https://github.com/potatoscript/xml/wiki/XML-Syntax) | Understand the fundamental rules and syntax of XML. |
| [XML Elements](https://github.com/potatoscript/xml/wiki/XML-Elements) | Learn how to define and use elements in XML. |
| [XML Attributes](https://github.com/potatoscript/xml/wiki/XML-Attributes) | Explore how attributes add metadata to XML elements. |
| [XML Namespaces](https://github.com/potatoscript/xml/wiki/XML-Namespaces) | Learn how to avoid element name conflicts using namespaces. |
| [XML Comments](https://github.com/potatoscript/xml/wiki/XML-Comments) | Understand how to add comments to XML documents. |
| [XML CDATA Section](https://github.com/potatoscript/xml/wiki/XML-CDATA-Section) | Learn how to use CDATA sections to store unescaped text. |
| [XML Validation](https://github.com/potatoscript/xml/wiki/XML-Validation) | Ensure XML document validity using DTD and XSD. |
| [Document Type Definition (DTD)](https://github.com/potatoscript/xml/wiki/DTD) | Define the structure and rules of XML using DTD. |
| [XML Schema Definition (XSD)](https://github.com/potatoscript/xml/wiki/XML-Schema) | Learn how to validate XML using XSD. |
| [XML Parsers](https://github.com/potatoscript/xml/wiki/XML-Parsers) | Explore DOM and SAX parsers used to process XML data. |
| [XML DOM (Document Object Model)](https://github.com/potatoscript/xml/wiki/XML-DOM) | Learn how DOM represents the structure of an XML document. |
| [XML SAX (Simple API for XML)](https://github.com/potatoscript/xml/wiki/XML-SAX) | Learn about event-driven XML parsing using SAX. |
| [XPath Basics](https://github.com/potatoscript/xml/wiki/XPath-Basics) | Learn how to navigate XML documents using XPath. |
| [Advanced XPath](https://github.com/potatoscript/xml/wiki/Advanced-XPath) | Explore advanced XPath queries and expressions. |
| [XSLT Basics](https://github.com/potatoscript/xml/wiki/XSLT-Basics) | Learn how to transform XML documents using XSLT. |
| [Advanced XSLT](https://github.com/potatoscript/xml/wiki/Advanced-XSLT) | Explore advanced XSLT techniques and transformations. |
| [XML with Java](https://github.com/potatoscript/xml/wiki/XML-with-Java) | Learn how to parse and manipulate XML using Java. |
| [XML with Python](https://github.com/potatoscript/xml/wiki/XML-with-Python) | Explore how to read, modify, and create XML using Python. |
| [XML with C#](https://github.com/potatoscript/xml/wiki/XML-with-CSharp) | Learn XML manipulation using C# and .NET libraries. |
| [XML and AJAX](https://github.com/potatoscript/xml/wiki/XML-and-AJAX) | Use XML with AJAX to update web pages asynchronously. |
| [XML Serialization](https://github.com/potatoscript/xml/wiki/XML-Serialization) | Learn how to convert objects to XML and vice versa. |
| [XML Encryption](https://github.com/potatoscript/xml/wiki/XML-Encryption) | Understand how to secure XML data using encryption. |
| [XML Digital Signatures](https://github.com/potatoscript/xml/wiki/XML-Digital-Signatures) | Learn to sign and verify XML documents digitally. |
| [XML APIs and Tools](https://github.com/potatoscript/xml/wiki/XML-APIs-and-Tools) | Explore popular APIs and tools for working with XML. |
| [Error Handling in XML](https://github.com/potatoscript/xml/wiki/Error-Handling-in-XML) | Learn how to handle and manage errors in XML. |
| [Best Practices for XML](https://github.com/potatoscript/xml/wiki/Best-Practices-for-XML) | Follow best practices for writing clean and efficient XML. |
| [Troubleshooting XML Issues](https://github.com/potatoscript/xml/wiki/Troubleshooting-XML-Issues) | Learn to identify and fix common XML errors. |

---


# home

* [Read XML Document with c#](#Read-XML-Document)

### Read-XML-Documnet
```xml
<?xml version="1.0" encoding="UTF-8"?>
<bookstore "BookId="ABC">
  <book category="fiction">
    <title>The Great Gatsby</title>
    <author>F. Scott Fitzgerald</author>
    <year>1925</year>
    <price>10.99</price>
  </book>
  <book category="fiction">
    <title>To Kill a Mockingbird</title>
    <author>Harper Lee</author>
    <year>1960</year>
    <price>12.99</price>
  </book>
  <book category="non-fiction">
    <title>The Elements of Style</title>
    <author>William Strunk Jr.</author>
    <author>E. B. White</author>
    <year>1918</year>
    <price>9.99</price>
  </book>
</bookstore>

```
```c#
using SYstem.Xml

XmlDocument xmlDoc = new XmlDocument();
xmlDoc.Load("MyXML.xml");
XmlElement root = xmlDoc.DocumentElement;
foreach(XmlNode childNode in root.CHildNodes)
{
   string ProdutId = childNode.Attributes["BookId"].Value;
}

XmlNodeList ndlst = XmlDoc.GetElementsByTagName("book");
foreach(XmlNode ndl in ndlst)
{
   if(ndl.Attributes["category"].Value == 'fiction')
     Console.WriteLine("category :"+ndl.Attributes["category"].Value);
}
```
[home](#home)
