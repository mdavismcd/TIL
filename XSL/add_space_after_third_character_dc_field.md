# Add a Space After the Third Character of a Specific Field in XSL

Some files were deposited into a repository with inconsistent spacing in the dc:title field. Instead of going through each record individually, I, with the help of Robert Chavez, created smiple XSL to run on records in bulk through a normalization rule. This can be done through any xsl convertor, but I used oXygen to check before running in the Alma---Library Services Platform at my work.

```
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:dc="http://purl.org/dc/elements/1.1/"
  exclude-result-prefixes="xs "
  version="3.0">
  
  <xsl:param name="element" select="'dc:title'"/>
  <xsl:template match="*">
    <xsl:copy>
      <xsl:apply-templates/>
    </xsl:copy>
  </xsl:template>  
  <xsl:template match="text()">
    <xsl:choose>
      <xsl:when test="$element!='*'">
        <xsl:choose>
          <xsl:when test="name(..) = $element">
    <xsl:value-of select="replace(.,'(^\w{3})','$0 ')"/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select="."/>
          </xsl:otherwise>
        </xsl:choose>
      </xsl:when>
    </xsl:choose>
  </xsl:template>
  
</xsl:stylesheet>
```