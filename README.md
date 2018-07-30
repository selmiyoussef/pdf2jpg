
## Building jar file from source.

To build the package maven is used, by default pdfbox does not include converted for certain jpg images.
To add support include the jar file provided in data/dependency path of project in your classpath and then maven compile.

Below is the entry in pom.xml for this jar file.
<p>
`
	<dependency> 
	    <groupId>org.apache.pdfbox</groupId>
	    <artifactId>jbig2-imageio</artifactId>
	    <version>3.0.0-SNAPSHOT</version>
	    <type>jar</type> <!-- Meaning it is picking this artifact from a jar file, add this jar to classpath-->
	</dependency>
`	
</p>

## Usage 

To use the jar just type below commands which will work

To convert single pdf page to image [Eg, below converting 3rd page]
`java -jar data/pdf2jpg.jar -i path_to_pdf -o output_directory -p 2`

To convert Multiple pdf pages to image 
`java -jar data/pdf2jpg.jar -i path_to_pdf -o output_directory -p 0,1,2,3`

To convert ALL pdf pages to image
`java -jar data/pdf2jpg.jar -i path_to_pdf -o output_directory -p ALL `



<b>OLD Jar usage - data/pdf2jpg_noargs.jar</b>

To convert single pdf page to image
`java -jar data/pdf2jpg.jar path_to_pdf output_directory SINGLE 1`

To convert Multiple pdf pages to image
`java -jar data/pdf2jpg.jar path_to_pdf output_directory MULTI 1,2,4`

To convert ALL pdf pages to image
`java -jar data/pdf2jpg.jar path_to_pdf output_directory ALL`