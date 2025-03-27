# Tony's Render Demo Reel

I am Tony, a student studying Computer Graphics and Game Technology at the University of Pennsylvania. I am very interested in computer graphics rendering. Here are some render demos of the projects I have recently done.

Monte Carlo Path Tracer
-----

The Monte Carlo Path Tracer is implemented using C++ and GLSL. It utilizes Monte Carlo estimation of the Light Transportation Equation to repeatedly sample light rays and produce a path traced image. Rendering in this path tracer takes time to converge to a final image as displayed below. The path tracer is able to load cubemap format environment maps and json format scene files. A json scene file consists of light source, object, and texture information. The path tracer supports loading .obj 3D models and their corresponding texture and normal maps.

**Cornell Box** <br>
The cornell box is a commonly used rendering scene in computer graphics. In this scene we have an area light on the ceiling, while all other objects are perfectly diffuse materials. Notice how the path tracer renders the diffuse reflection of wall colors to the center cubic objects.
![1743033022356](image/README/1743033022356.png)

**Cornell Box Mirror** <br>
Cornell box with a perfectly specular mirror as the back wall.
![1743033122823](image/README/1743033122823.png)

**Infite Mirror Scene** <br>
A scene with six surrounding mirrors as walls. The objects are reflected repeatedly in the mirrors. Increasing the maximum ray-object testing iteration passes can increase the number of reflections in the scene.
![1743033571527](image/README/1743033571527.png)

**Cornell Box Glass Ball** <br>
The path tracer is able to handle reflections and internal reflections of dielectric materials like glass. Notice how the imaging inside the glassball is distorted.
![1743033887468](image/README/1743033887468.png)

**Cornell Box Microfacet Material** <br>
The path tracer is able to handle microfacet materials that are between perfectly diffuse and perfectly specular. The surface can be uniform in roughness or have a roughness map applied to it.
![1743034122047](image/README/1743034122047.png)
![1743034328034](image/README/1743034328034.png)

**Glass Ball with Environment Map** <br>
Various scenes with different environment maps applied. The environment maps are treated as light sources as we compute the light transport equation. Different brightness spots in the map contribute differently to the light energy. Notice the image of the environment map projected in the diffuse surface below the ball.
![1743034469153](image/README/1743034469153.png)
![1743034667544](image/README/1743034667544.png)

Real Time Physically Based Ray Tracing Shader
---

I have also implemented a Physically Based Rendering (PBR) shader that can perform ray tracing of a scene in a real-time frame rate of above 60fps. The PBR shader can tune an object's color (albedo), metallicness and roughness to investigate different material properties. It can also load predefined albedo map, normal map, metalicness map, and roughness map to produce a ray-traced render in real-time.

**White Ball with 50\% metallic and 50\% roughness**
![1743036248852](image/README/1743036248852.png)

**White Ball with 100\% metallic and 0\% roughness (Chrome)**
![1743036304209](image/README/1743036304209.png)

**White Ball with 0\% metallic and 0\% roughness (Plastic)**
![1743036360302](image/README/1743036360302.png)

**Custom Cerberus model with albedo, metallic, roughness, and normal maps**
![1743036422841](image/README/1743036422841.png)
![1743036484241](image/README/1743036484241.png)

**Custom Atomizer model with only albedo map**<br>
Metal-like texture
![1743036577989](image/README/1743036577989.png)
Plastic-like texture
![1743036723378](image/README/1743036723378.png)

