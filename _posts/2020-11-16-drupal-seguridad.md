---
layout: post
title:  "Por qué drupal es el CMS más seguro que conozco"
author: alvaro
categories: [ Tecnología, drupal ]
image: assets/images/drupal-security.jpg
image_credits: https://unsplash.com/@thejmoore
description: "Drupal el CMS más seguro que conozco, a continuación explico por qué"
featured: false
hidden: false
---

  
En Internet se pueden encontrar muchas comparaciones entre los sistems de gestión de contenido más populares. Cada vez que se menciona a Drupal, se describe con palabras como como: seguro, abierto, frecuentemente actualizado... Hoy voy a explicar por qué no es solo una opinión (ojo: que no es solo porque me dedique a desarrollar en drupal). Voy a presentar también pruebas de que el nivel de seguridad del que presumimos en la comunidad de drupal va mucho más allá de las palabras.

Hay fundamentalmente cinco razones detrás de la segurida de Drupal:

## 1. Modelo de código abierto
    
Posiblemente digas “Bueno, la mayoría de gestores de contenido se distribuyen bajo el modelo de código abierto ¿Por qué va a ser esto una ventaja para drupal?”. Vamos a mirar un poco más allá en el ecosistema el gestor de contenidos. La mayoría se distribuyen como código abierto, pero sus módulos, complementos y temas se están sujetos a un sistema puramente comercial. En el caso de WordPress, por ejemplo, la venta de complementos es muy popular y hace que su modelo de código abierto se vea limitado. La comunidad de drupal ha desarrollado un modelo completamente diferente y centralizado.

Fundamentalmente consiste en que los módulos gratuitos que se encuentran dispobles desde [drupal.org](http://drupal.org), tienen una cobertura adicional gracias al programa interno de seguridad. A pesar de que está manera de hacer las cosas complica de alguna manera la creación y publicación de nuevos módulos y temas, también hace mucho más difícil que llegue a estos módulos y temas algún tipo de código malicioso. Este modelo centralizado también tiene ventajas cuando se descubren problemas de seguridad en el mismo drupal. Esto quedó perfectamente demostrado en la actualización de seguridad SA-CORE-2019-003, que cubría tanto el core de drupal como algunos módulos muy utilizados.

## 2. El equipo de seguridad

Se puede oir hablar sobre errores críticos de drupal a menudo. En 2018 y 2019 tuvimos que lidiar con algunos errores calificados como altamente críticos, dos de los cuales fueron bautizados como "Drupalgeddon". A pesar de esto, es importante tener en cuenta que no es el resultado de un código de poca calidad. Es el resultado de un esfuerzo titánico por parte de la comunidad, especialmente en la parte correspondiente a cuidar de la seguridad.


El equipo de seguridad, actualmente consiste en más de 30 personas de varias empresas y organizaciones de diferentes partes del mundo. Se ha ganado una merecida reputación (gracias a hacer su labor de una manera eficiente y calificada por algunos como paranoica) en cuestiones de seguridad, además cuenta con el apoyo de voluntarios y con "caza-recompensas" del programa "Bug Bounty"


## 3. Soporte de las organizaciones

Aunque la forma en que se utiliza un determinado CMS es muy importante. Drupal es el gestor de contenidos que eligen muchas grandes corporaciones y agencias gubernamentales (algunos de ellos se pueden encontrar en esta lista https://groups.drupal.org/government-sites). Incluso gigantes como Tesla, Nokia, la Universidad de Harvard, Londres y Los Ángeles, así como la NASA han confiado en él. Cada una de estas organizaciones cuida bien las medidas de seguridad de sus sitios web y realiza innumerables auditorías internas. Las vulnerabilidades encontradas suelen pasar al ya mencionado Equipo de Seguridad de Drupal.

  
El apoyo de estas grandes organizaciones es muy importante y necesario, gracias a ello, un proyecto de código abierto se convierte en un bien común, cuyo desarrollo beneficiará a todos los interesados. Como curiosidad, me gustaría mencionar que a principios de 2019 la Comisión Europea anunció el programa EU FOSSA 2 (The European Commission Free and Open Source Software Audit), cuyo segundo mayor beneficiario es fue Drupal. Como parte del programa, las personas que reportaran errores errores de seguridad recibirán una recompensa monetaria.
  
## 4. Composer y los componentes de Symfony

Desde la versión 8, Drupal está integrado con componentes Symfony. Es un gran salto adelante, hacia la estandarización del código. El uso de módulos probados, como EventDispatcher, HttpFoundation/HttpKernel y Routing, reduce la carga de trabajo en mantenimiento y seguridad puesto que se colabora con el desarrollo de esos módulos. Al mismo tiempo, la comunidad Symfony está ganando nuevos desarrolladores y nuevos patrocinadores. Gracias a esto, el nivel de seguridad está aumentando constantemente, porque las bibliotecas en las que se basa todo están cada vez más controladas.


Symfony no sólo es una colección de bibliotecas, sino que también está equipado con Composer - un excelente administrador de paquetes creado en base al modelo npm. Ya era posible usarlo con Drupal 7, pero en la versión 8 se convirtió en la manera estándar de añadir módulos y bibliotecas, sin la cual es difícil incluso imaginar el mantenimiento continuo de las páginas. Puede solucionar dependencias complejas, descargando librerías diferentes a PHP, parcheando y ejecutando scripts de instalación. Hoy en día Composer funciona muy bien, por lo que la estandarización de su uso se considera un paso muy importante en el avance del desarrollo de drupal.


## 5. Mecanismos de seguridad

Ya se ha hablado sobre muchos factores de organización, dinero y diseño. Sin embargo, puede quedar alguna duda sobre que mecanismos protegen a un webmaster de un ataque a su sitio. Aquí están algunos de ellos:


* Las contraseñas de los usuarios se almacenan en forma de hash, usando sal y función multiplicativa de hash. Esto hace que los ataques de fuerza bruta sean más difíciles de llevar a cabo.


* La configuración del sitio puede ser guardada en archivos .yml y comparada con su versión anterior. Además, suele exportarse en código en el repositorio. Esta es una excelente solución que limita en gran medida la posibilidad de una infección inadvertida de la base de datos.


* La gestión avanzada de permisos permite definir los roles de los usuarios y asignarles actividades que pueden realizar en el sitio. Los creadores de Drupal pusieron mucho énfasis en este tema, y hoy en día resulta en un alto grado de seguridad.


* El sistema de reporte de errores registra cada posible problem de seguridad, incluyendo los archivos .htaccess perdidos en directorios sensibles.


* El sistema de actualización permite descargar e instalar las últimas versiones de los módulos desde el panel de administración. Es muy conveniente en los hostings compartidos, que no siempre tienen la capacidad de usar Composer.


* El lenguaje Twig utilizado para crear plantillas tiene mecanismos avanzados para defenderse de los ataques XSS y CSRF.


* El sistema de caché permite aguantar ataques DoS.


* Es posible encriptar completamente la base de datos.


* Vale la pena añadir que Drupal cumple con el estándar OWASP (Open Web Application Security Project), que define los principios básicos de seguridad que debe cumplir un proyecto web moderno.
  

Basado en un post de Droptica <a  href="https://www.droptica.com/blog/why-drupal-more-secure-any-other-cms/">drupal agency</a> y por supuesto con su permiso.