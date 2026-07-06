## **<u>Manual Testing</u>**

<b>There are three manual testing surface categories:</b>

### **Modern third-party**

In web hacking, this testing should not be done at the functionality level, but analysing how it is implemented and if that leads to vulns;
Jquery itself may have no vulnerabities that could be found, but unsanitized output could mean XSS.

Some practices:

- Check if the library/api is out of scope; Zero-day vulnerabilities/supply chain attacks are more overlooked by another group of researchers.
- Source code, raw requests and in general raw content is where the related finds are.

*Overall*, developer team logic errors cause frictions between system and third-party assets.

### **Outdated third-party**

This is the part that is best automated; Either passive or active scanning with shodan API, retireJS or as preffered by me OWASP zap can compare 
version through metadata or requests with known CVEs; From there you can implement payloads that are known to work, *and it's not fraud because you
being at the right time right place earns your own find :)*
A key takeaway, **If it has been done before, it can be automated**

### **Developer-built functionality**

For this category, methods from both previous categories can be validly implemented.

Some exclusive vulnerability types *that have also earned high spots in the latest [OWASP top 10](https://owasp.org/Top10/2025/)*:
- IDOR
- Acess Control
- Insecure Design
- Business Logic

<iframe src = "https://owasp.org/Top10/2025" width = "555" height = "200">
