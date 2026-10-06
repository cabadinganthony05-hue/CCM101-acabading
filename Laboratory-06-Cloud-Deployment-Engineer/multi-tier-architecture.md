# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture is a system design where an application is divided into two main parts: the application or web tier and the database tier. Each tier performs a different responsibility while working together to provide the complete service.

## Web/Application Tier

The web or application tier is responsible for handling the application's interface and processing requests from users. In this laboratory, Nextcloud serves as the application that users access through a web browser. It processes user requests and communicates with the database when information needs to be stored or retrieved.

## Database Tier

The database tier is responsible for storing and managing persistent information. In this project, MariaDB serves as the database for Nextcloud. It stores important application data such as user accounts, configuration information, and other records required by the application.

## Why Separate the Tiers?

Separating the web application and database into different containers makes the infrastructure easier to manage and maintain. Each service can be configured, updated, restarted, or scaled independently. It also provides better organization because each container has a specific responsibility instead of placing all components into one container.
