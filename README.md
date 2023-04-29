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
