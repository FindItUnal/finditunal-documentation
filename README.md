# FindItUnal — Documentation

This folder contains documentation and workshop material for the FindItUnal project. The backend follows a Model-View-Controller (MVC) architecture. This README summarizes the project, the chosen architecture, how to run the backend, and where to find important files.

## Overview

FindItUnal is a lost-and-found platform. This repository contains the backend services (TypeScript + Express) used by the project. The backend exposes RESTful endpoints for authentication, user management, objects (lost/found items), categories, locations, images, and reports, and persists data in MySQL.

## Architecture — Model View Controller (MVC)

We use a classical MVC pattern to keep responsibilities separated and make the codebase easy to navigate and test:

- Models: represent database entities and handle data access. In this project these are TypeScript classes/modules that define the data shape and database operations (see `src/models`).
- Views: for an API backend the "view" is the HTTP response layer (JSON responses, error formatting, and file uploads). Views are thin and implemented inside controllers and route handlers.
- Controllers: contain the application logic for each route — validating input, orchestrating model calls, and returning responses. Controllers live in `src/controllers`.

## Technologies

- Node.js + TypeScript
- Express
- MySQL (`mysql2` driver)
- Multer for file uploads
- Zod for validation
- Docker & Docker Compose for local development

