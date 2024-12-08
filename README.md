# SPRING_SECURITY

## 1. Concepts de base  

### Qu’est-ce que Spring Security et pourquoi l’utilise-t-on ?  
Spring Security est un framework dédié à la sécurité des applications Java. Il fournit des fonctionnalités comme l'authentification, l'autorisation, la protection 
contre les attaques (CSRF, XSS), et la gestion des utilisateurs et rôles. On l’utilise pour sécuriser les applications Web et REST, en réduisant la complexité liée à l’implémentation manuelle de la sécurité.  


### Quelles sont les principales fonctionnalités fournies par Spring Security ?  

- Authentification (avec formulaires, Basic Auth, OAuth2, JWT, etc.).  
- Autorisation (gestion des rôles et permissions).  
- Protection contre les attaques CSRF (Cross-Site Request Forgery).  
- Protection contre les attaques XSS (Cross-Site Scripting).  
- Intégration avec des bases de données pour la gestion des utilisateurs.   
- Sécurisation des APIs REST.  
- Support des protocoles OAuth2 et OpenID Connect.  

### Qu’est-ce que le SecurityContext dans Spring Security ?    
Le SecurityContext stocke les informations de sécurité de l'utilisateur actuel, comme son identifiant et ses rôles. Par défaut, il est stocké dans un thread local et est accessible globalement via SecurityContextHolder. 
C’est essentiel pour vérifier si un utilisateur est authentifié et quels sont ses privilèges.

### Quelle est la différence entre Authentication et Authorization ?   

- Authentication : Vérifie l’identité de l’utilisateur (par exemple, via un login/mot de passe).  
- Authorization : Contrôle l'accès à des ressources ou actions en fonction des permissions ou rôles attribués à l'utilisateur.  

### Quels sont les différents types de grants dans un système de sécurité ?  

- Role-based access control (RBAC) : Les utilisateurs se voient attribuer des rôles (ex. : ADMIN, USER), et les rôles définissent les permissions.  
- Permission-based access control : Les permissions sont attribuées directement aux utilisateurs (ex. : READ_PRIVILEGE, WRITE_PRIVILEGE).  
- Attribute-based access control (ABAC) : Les décisions d’accès sont basées sur des attributs contextuels (ex. : l'heure, la localisation).  

### Quelles sont les étapes principales du traitement d’une requête dans Spring Security ?  

- Filtrage de la requête : Les filtres (comme UsernamePasswordAuthenticationFilter) interceptent la requête.  
- Authentication : Spring Security vérifie l'identité de l'utilisateur via un gestionnaire d'authentification (AuthenticationManager).  
- Authorization : Une fois authentifié, Spring vérifie si l'utilisateur a le droit d'accéder à la ressource.  
- Réponse : La requête est autorisée ou rejetée.

  
