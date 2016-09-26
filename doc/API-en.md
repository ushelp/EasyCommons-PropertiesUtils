# EasyCommons-EasyPropertiesUtils

---------------
[EasyCommons](readme-zh.md "EasyCommons")  Properties file manipulation tools under the project. 

`java.util.Properties` not only the existence of problems in the design and function of abnormal primitive, usually in addition to reading and writing not practical in the (original file format and can lead to loss of the comment). When maintenance or write properties file must be self-fulfilling to write programs.

**Use EasyProperties can instead of java.util.Properties.**


## 1. API summary
EasyPropertiesUtils It includes the following components：

1. **EasyProperties**：When the function does not affect or modify the properties used in place of the properties file java.util.Properties class, extends java.util.Properties, provides content merge (merge:: add, delete, change) and modifications (add, change modify) the original format; support `#comment` comment, `#newLine` add newline.

 **Scene** : properties require any scene file read and write operations, without affecting the original file format. 

 ```JAVA
  /**
  * Two ways to modify the properties file (instead of store method):
  * - Merge: The Properties object into the specified file (add, change, delete)
  * - Modify: Modify the Properties object to the specified file (add, change, delete the original file does not include having a parameter)
  *
  *@param PropertiesFile to modify the properties file, support path (string path) and a file (file object) as a parameter
  *@param Charset document character set, optional
  */
  mergeToFile(propertiesFile [, String charset]);
  modifyToFile(propertiesFile [, String charset]);
 ```

2. **EasyPropertiesUtils**： Properties file directly modify the tools to provide the original format write functions, including a comment, support is incorporated (merge: add, delete, change) and modifications (modify: add, change); and suport use regular matches deleted file content; support `#comment` comment, `#newLine` add newline.

 **Scene**: properties files to modify the operation, without prejudice to the original format.
 
 ```JAVA
  /**
  * Map directly modify the data collection and Properties object to specify the properties file two ways to modify the properties file:
  * - Merge: The Properties object into the specified file (add, change, delete)
  * - Modify: Modify the Properties object to the specified file (add, change, delete the original file does not include having a parameter)
  *
  *@param PropertiesFile to modify the properties file, support path (string path) and a file (file object) as a parameter
  *@param Properties support parameter of type Map or Properties
  *@param Charset document character set, optional
  */
  merger(propertiesFile, Map<String, String> properties [, charset]);
  merger(propertiesFile, Properties properties [, charset]);
  modify(propertiesFile, Map<String, String> properties [, charset]);
  modify(propertiesFile, Properties properties [, charset]);

  /**
  * Using regular expressions to remove the lines.
  * @param propertiesFile properties File Object
  * @param propertiesFilePath properties File Path
  * @param regex regular expressions
  * @param charset charset
  * @return whether success
  */
  boolean removeLinesToFile(File propertiesFile|String propertiesFilePath, String regex, [String charset]);
  boolean removeLinesToFile(String propertiesFilePath, String regex, [String charset]);
 
  /**
   * Using regular expressions to remove the contents.
   * 
   * @param propertiesFile properties File Object
   * @param propertiesFilePath properties File Path
   * @param regex regular expressions
   * @param charset charset
   * @return whether success
   */
  boolean removeMatchesToFile(File propertiesFile|String propertiesFilePath, String regex,[String charset]);
  boolean removeMatchesToFile(String propertiesFilePath, String regex,[String charset]);
 ```
  
 **Adding line breaks and comments example:**
 ```
  // Add newLinew by '#newLine'
  map.put("newLine 1", "#newLine");
  map.put("newLine 2", "#newLine");
  
  // Add comments by '#comments'
  map.put("==== this is comments ====","#comments");
 ```

 **Remove content Example:**
 ```
  //Delete line 
  EasyPropertiesUtils.removeLinesToFile(propertiesFile, ".* need to delete.*");
  //Delete content
  EasyPropertiesUtils.removeMatchesToFile(propertiesFile, "("+System.getProperty("line.separator")+"){1,3}#====this is comments.*");
 ```

## 2. Maven
```XML
<!-- EasyPropertiesUtils -->
<dependency>
	<groupId>cn.easyproject</groupId>
	<artifactId>easycommons-properties</artifactId>
	<version>2.0.0-RELEASE</version>
</dependency>
```

## End

[Comments](http://www.easyproject.cn/easycommons/en/index.jsp#about 'Comments')

If you have more comments, suggestions or ideas, please contact me.

Email:<inthinkcolor@gmail.com>

[http://www.easyproject.cn](http://www.easyproject.cn "EasyProject Home")
