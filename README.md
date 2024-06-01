# Entrepriza.com
<beans xmlns="https://jakarta.ee/xml/ns/jakartaee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="https://jakarta.ee/xml/ns/jakartaee https://jakarta.ee/xml/ns/jakartaee/beans_4_0.xsd" bean-discovery-mode="all" version="4.0"> </beans>
<web-app xmlns="https://jakarta.ee/xml/ns/jakartaee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="6.0" xsi:schemaLocation="https://jakarta.ee/xml/ns/jakartaee https://jakarta.ee/xml/ns/jakartaee/web-app_6_0.xsd">

<welcome-file-list>

<welcome-file>index.html</welcome-file>

</welcome-file-list>

<security-constraint>

<display-name>Secured pages</display-name>

<web-resource-collection>

<web-resource-name>secured</web-resource-name>

<url-pattern>/secured/*</url-pattern>

</web-resource-collection>

<auth-constraint>

<role-name>admin</role-name>

<role-name>user</role-name>

</auth-constraint>

</security-constraint>

<security-constraint>

<display-name>Secured admin pages</display-name>

<web-resource-collection>

<web-resource-name>admin</web-resource-name>

<url-pattern>/admin/*</url-pattern>

</web-resource-collection>

<auth-constraint>

<role-name>admin</role-name>

</auth-constraint>

</security-constraint>

</web-app>

