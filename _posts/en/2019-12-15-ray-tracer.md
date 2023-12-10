---
layout: post
title: C++ Ray Tracer
subtitle: "A ray tracer written from scratch based on Phong shading and extended to support reflectiveness and transparency"
date: 2019-12-15
categories: rendering
author: Yuxuan Huang
cover: /assets/img/posts/raytracer/raytracer-cover.jpg
tags: 
- C++
- Rendering
lang: en
---

## Chapter 1

> A C++ ray tracer written from scratch based on Phong shading and extended to support reflectiveness and transparency. The current version is used for grading in CSCI 5607 Fundamentals of Computer Graphics at UMN, thus the source code is not made public.

### Phong Shading

![Basic Phong Shading](/assets/img/posts/raytracer/phongshading.jpg)

Spheres rendered with high ambient value (upper), high diffuse value (lower-left), and high specular value (lower-right).

### Soft Shadow, Spotlight and Attenuation

![Lighting and Shadow](/assets/img/posts/raytracer/spotlight_softshadow.jpg)

Light sources in the scene cast soft shadows on the spheres. Spotlights with soft shadow boundaries were implemented (illuminated area with circular shape). Light attenuation effect was also included (light sources closer to the surface create brighter illumination).

### Texture Mapping
![Sphere Texture Mapping](/assets/img/posts/raytracer/texturemap1.jpg)
A basic textured sphere.

![Triangle Texture Mapping](/assets/img/posts/raytracer/texturemap2.jpg)
A textured scene with more geometric primitives.

![Normal Mapping](/assets/img/posts/raytracer/normalmap.jpg)
Normal maps are also supported.

### Reflection, Refraction & Fresnel Effect

![Polished Metal Sphere (reflection only)](/assets/img/posts/raytracer/raytracer-metalsphere.jpg)

The surface acts like a perfect mirror.

![Glass Sphere (reflection + refraction)](/assets/img/posts/raytracer/raytracer-glasssphere.jpg)

Light rays pass through the crystal ball. Note that Fresnel effect is implemented, so that the sphere is more transparent in the center, and more reflective towards the boundary.

![Hollow Glass Sphere](/assets/img/posts/raytracer/raytracer-glassspherehollow.jpg)

Note that the scene is upright after the rays entering and exiting the glass surfaces twice (flipped twice). Also the boundary of the sphere appears like a dark ring due to total internal reflection.