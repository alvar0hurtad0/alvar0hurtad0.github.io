---
layout: post
title:  "Por qué drupal es el CMS más seguro que conozco"
author: alvaro
categories: [ Tecnología ]
image: assets/images/wales-golf-madrid.jpg
image_credits: https://www.marca.com/futbol/real-madrid/2019/11/21/5dd6eecaca47411c6f8b45b0.html
description: "Drupal el CMS más seguro que conozco, a continuación explico por qué"
featured: false
hidden: false
---

En Internet se pueden encontrar muchas comparaciones entre los sistems de gestión de contenido más populares. Cada vez que se menciona a Drupal, se describe con palabras como como: seguro, abierto, frecuentemente actualizado... Hoy voy a explicar por qué no es solo una opinión (ojo: que no es solo porque me dedique a desarrollar en drupal). Voy a presentar también pruebas de que el nivel de seguridad del que presumimos en la comunidad de drupal va mucho más allá de las palabras.

Hay fundamentalmente cinco razones detrás de la segurida de Drupal:

1. Modelo de código abierto
Posiblemente digas "Bueno, la mayoría de gestores de contenido se distribuyen bajo el modelo de código abierto ¿Por qué va a ser esto una ventaja para drupal?". Vamos a mirar un poco más allá en el ecosistema el gestor de contenidos. La mayoría se distribuyen como cógio abierto, pero sus módulos, complementos y temas se están sujetos a un sistema puramente comercial. En el caso, por ejemplo, de WordPress, la vent de complementos es muy popular y hace que su modelo de código abierto se vea limitado.

La comunidad de drupal ha desarrollado un modelo completamente diferente y centralizado. Fundamentalmente consiste en que los módulos gratuitos que se encuentran dispobles desde drupal.org, tienen una cobertura adicional gracias al programa interno de seguridad. A pesar de que está manera de hacer las cosas complica de alguna manera la creacin y publicacin de nuevos módulos y temas, también hace mucho más difícil que llegue a estos módulos y temas algún tipo de código malicioso. Este modelo centralizado también tiene ventajas cuando se descubren problemas de seguridad en el mismo drupal. Esto quedó perfectamente demostrado en la actualizacin de seguridad SA-CORE-2019-003, que cubría tanto el core de drupal como algunos módulos muy utilizados.

2. El equipo de seguridad
Se puede oir hablar sobre errores críticos de drupal a menudo. En 2018 y 2019 tuvimos que lidiar con algunos errores calificados como altamente críticos, dos de los cuales fueron bautizados como "Drupalgeddon". A pesar de esto, es importante tener en cuenta que no es el resultado de un código de poca calidad. Es el resultado de un esfuerzo titánico por parte de la comunidad, especialmente en la parte correspondiente a cuidar de la seguridad.

El equipo de seguridad, actualmente consiste en más de 30 personas de varias empresas y organizaciones de diferentes partes del mundo. Se ha ganado una merecida reputación (gracias a hacer su labor de una manera eficiente y calificada por algunos como paranoica) en cuestiones de seguridad, además cuenta con el apoyo de voluntarios y con "caza-recompensas" del programa "Bug Bounty"

3. Soporte de las organizaciones
Aunque la forma en que se utiliza un determinado CMS es muy importante. Drupal es el gestor de contenidos que eligen muchas grandes corporaciones y agencias gubernamentales (algunos de ellos se pueden encontrar en esta lista https://groups.drupal.org/government-sites). Incluso gigantes como Tesla, Nokia, la Universidad de Harvard, Londres y Los Ángeles, así como la NASA han confiado en él. Cada una de estas organizaciones cuida bien las medidas de seguridad de sus sitios web y realiza innumerables auditorías internas. Las vulnerabilidades encontradas suelen pasar al ya mencionado Equipo de Seguridad de Drupal.

El apoyo de estas grandes organizaciones es muy importante y necesario, gracias a ello, un proyecto de código abierto se convierte en un bien común, cuyo desarrollo beneficiará a todos los interesados. Como curiosidad, me gustaría mencionar que a principios de 2019 la Comisión Europea anunció el programa EU FOSSA 2 (The European Commission Free and Open Source Software Audit), cuyo segundo mayor beneficiario es fue Drupal. Como parte del programa, las personas que reportaran errores errores de seguridad recibirán una recompensa monetaria, cuyo monto dependería de lo grave que fuera

4. Composer and the components of Symfony
Since version 8, Drupal is integrated with Symfony components. It's a huge leap forward, towards code standardisation. The use of proven modules, such as EventDispatcher, HttpFoundation/HttpKernel and Routing, relieves developers of the need to maintain their own solutions. At the same time, the Symfony community is gaining new developers and new sponsors. Thanks to this, the level of security is constantly rising, because the basic libraries are getting more and more "tight".

Symfony is not only a collection of libraries, it is also equipped with Composer – an excellent package manager created based on the npm model. It was already possible to use it with Drupal 7, but in version 8 it became a downright obligatory addition, without which it is hard to even imagine the ongoing maintenance of pages. It can deal with complex dependencies, downloading libraries other than PHP, patching and running installation scripts. Today, when the Composer's operation is very well-developed, it's safe to say that it's a milestone in updating the Drupal code.

5. Security mechanisms
I've already written about many organisational, money and design factors. I didn't, however, specifically mention what mechanisms protect a webmaster from an attack on his site. Here are some of them:

Users' passwords are stored in a hashed form, using salt and multiplicative hash function. This makes brute force attacks more difficult to carry out.
The site configuration can be saved to .yml files and compared to its previous version. What's more, you can save it in the code repository using the Features module. It's an excellent solution that greatly limits the possibility of unnoticed database infection.
Advanced permission management allows you to define user roles and assign them activities that they can perform on the site. The creators of Drupal put a lot of emphasis on this issue, and today it results in a high degree of security.
The error reporting system records every security breach, including missing .htaccess files in sensitive directories.
The update system allows for downloading and installing the latest versions of modules from the admin panel. It's very convenient on shared hostings, that do not always have the ability to use Composer.
The Twig language used to create templates has advanced mechanisms used to defend against XSS and CSRF attacks.
The extensive cache allows you to effectively defend against DoS attacks.
It is possible to fully encrypt the database.
It is worth adding that Drupal complies with the OWASP (Open Web Application Security Project) standard, defining the basic security principles that a modern web project must meet.

Con el permiso de Droptica <a href="https://www.droptica.com/blog/why-drupal-more-secure-any-other-cms/">drupal agency</a>.
