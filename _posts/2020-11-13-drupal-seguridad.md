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

The Drupal community has developed a completely different, centralised model. It mostly consists of free add-ons, available directly from the drupal.org website, additionally covered by an internal security programme. Such an approach somewhat complicates the creation of modules and skins, but at the same time – makes it difficult to smuggle malicious code. The centralised model also reveals its advantages in the case of discovering security flaws in Drupal itself. It was perfectly demonstrated by the recent SA-CORE-2019-003 security update, which covered not only the core, but also the popular modules.

2. Security Team
You can often hear about critical errors in Drupal. In 2018 and 2019 we had to deal with some highly critical updates, some of them were even named "Drupalgeddon". However, this is not a result of poor-quality code. It's a result of the titanic work being carried out by the community, especially its part dealing with security.

Drupal's Security Team currently consists of over 30 people from various companies and organisations from around the world. It has earned a well-deserved reputation – through efficiency and downright paranoid concentration on security issues. It is supported by volunteers – also working as part of paid "bug bounty" programmes.

3. Organisations' support
Based on the example of WordPress – security does not go hand in hand with reach. Though the way which a given CMS is being used is very important. Drupal is a system often chosen by large corporations and government agencies (some of them can be found on this list https://groups.drupal.org/government-sites). Even such giants as Tesla, Nokia, Harvard University, London and Los Angeles, as well as NASA have trusted him. Each of these organisations takes good care of the security measures on their websites and conducts innumerable internal audits. The vulnerabilities found are usually passed to the previously mentioned Drupal Security Team.

The support of big players is very important and necessary – thanks to this, an open-source project becomes a common good, the development of which will benefit everyone interested. As a curiosity, I would like to mention that at the beginning of 2019 the European Commission announced the EU FOSSA 2 (The European Commission Free and Open Source Software Audit) programme – the second largest beneficiary of which is actually Drupal. As part of the programme, the people tracking errors will receive a monetary reward, the amount of which depends on the significance of the reported vulnerability. There's € 89 000 in the pot.

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