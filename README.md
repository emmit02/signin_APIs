# Signin_APIs


To authenticate a login page through GitHub and Google in a Spring Boot application, you can use OAuth 2.0, which is a widely used standard for authentication and authorization. Spring Boot provides support for OAuth 2.0 through Spring Security. Below are the general steps to implement authentication using GitHub and Google in a Spring Boot application:



1. Create OAuth Apps:
    For GitHub: Go to your GitHub account settings, navigate to "Developer settings" > "OAuth Apps," and create a new OAuth App. Obtain the Client ID and Client Secret.
    For Google: Go to the Google Cloud Console, create a new project, enable the "Google+ API," and create OAuth 2.0 credentials. Obtain the Client ID and Client Secret.

2. Add Dependencies:
    Add the necessary dependencies in your pom.xml file for Spring Security, OAuth, and Spring Web.

3. Configure OAuth Properties:
    Configure OAuth properties in your application.properties

    # GitHub Login
      spring.security.oauth2.client.registration.github.client-id=#generate your client-id from github acc   
      spring.security.oauth2.client.registration.github.client-secret=#generate your client-secret from github acc
    # Google Login
      spring.security.oauth2.client.registration.google.client-id=#generate your client-id from google acc
      spring.security.oauth2.client.registration.google.client-secret=#generate your client-secret from google acc

4. Enable OAuth in Security Configuration:
    Create a configuration class that extends WebSecurityConfigurerAdapter and enable OAuth 2.O

5. Run your Spring Boot Application:
    Run your Spring Boot application, and when you navigate to the login page, Spring Security should redirect you to GitHub or Google for authentication.
