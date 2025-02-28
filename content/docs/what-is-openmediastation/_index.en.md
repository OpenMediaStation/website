+++
title = 'What is OpenMediaStation (OMS)'
draft = false
weight = 1
description = "Explanation about what the OpenMediaStation (OMS) software aims to be."
type = "docs"
+++

OpenMediaStation (OMS) is designed to be a central hub for hosting all the media files you own.  

Our goal is to give the control back to the user which has been lost due to various streaming services and the misleading concept of "buying" a license to access media rather than truly owning it. With this project, we aim to restore that control. Users who purchase media from sources that allow file downloads can use OMS to manage and view their collection in one place.  

OMS supports various media types, including movies, TV shows, audiobooks, books and more. (Currently, movies and TV shows are fully supported, with additional media types planned for future releases.)  

While similar projects exist, none fully met our needs. We strongly believe in open-source software and the only real alternative that supports multiple media types is Jellyfin. However, Jellyfin’s support for books and audiobooks is lacking. Our goal is to offer robust support for these media types, making them a core focus of our development.  

Additionally, we prioritize user privacy. We do not collect unnecessary data or make it easy for third parties to do so. However, privacy also requires strong security. Unlike Jellyfin, which lacks proper security when exposed to the internet, OMS was created with security in mind. (I will cover this topic in more detail in a future blog post.) To enhance security, OMS allows users to integrate a third-party identity provider via OAuth, significantly improving authentication compared to Jellyfin. 
