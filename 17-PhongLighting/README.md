DirectX Raytracing Tutorials
============
This repository contain tutorials demonstrating how to use DirectX Raytracing.

Requirements:
- A GPU that supports DXR (Such as NVIDIA's Volta or Turing hardware)
- Windows 10 RS5 (version 1809) or newer
- [Windows 10 SDK version 1809 (10.0.17763.0)](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive)
- Visual Studio 2022

# DXR Tutorial 17

## 17 Phong Lighting
![image](https://user-images.githubusercontent.com/17934438/222796299-56c50142-0f30-468a-8226-4bf19cef8e52.png)

## Overview

## 17.0
Add structs for creating a sphere
```c++
// 17.0.a
namespace Structs
{
    struct VertexPositionNormalTangentTexture
    {
        glm::vec3 position;
        glm::vec3 normal;
        glm::vec3 tangent;
        glm::vec2 texCoord;

        VertexPositionNormalTangentTexture(const glm::vec3 pos, const glm::vec3 norm,
            const glm::vec3 tan, const glm::vec2 texCor)
        {
            position = pos;
            normal = norm;
            tangent = tan;
            texCoord = texCor;
        }

        VertexPositionNormalTangentTexture() = default;
    };
}
```
```c++
// 17.0.b
struct Shape
{
    std::vector<Structs::VertexPositionNormalTangentTexture> vertexData;
    std::vector<unsigned short> indexData;
};
```
