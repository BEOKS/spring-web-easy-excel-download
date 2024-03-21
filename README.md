# spring-web-easy-excel-download

In services run on the Spring web framework, sometimes data must be offered in Excel instead of JSON. This library simplifies the process, allowing the conversion of JSON data to Excel files for download with just one annotation, bypassing the complexity of using tools like Apache POI
# Usage
You need only append `@ExcelDownload` annotation to Controller Method.
```java
@RestController
@RequestMapping("/pet")
public class PetController {
    @GetMapping("/excel/aop")
    @ExcelDownload(fileName = "test.xlsx")
    List<Pet> getExcelAop(HttpServletResponse response){
        return Pet.getDummy();
    }
}
```