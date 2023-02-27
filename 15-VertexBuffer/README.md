DirectX Raytracing Tutorials
============
This repository contain tutorials demonstrating how to use DirectX Raytracing.

Requirements:
- A GPU that supports DXR (Such as NVIDIA's Volta or Turing hardware)
- Windows 10 RS5 (version 1809) or newer
- [Windows 10 SDK version 1809 (10.0.17763.0)](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive)
- Visual Studio 2022

# DXR Tutorial 15

## 15.0 Vertex Buffer

## Overview
There will be times that you need the Vertex and Indice information in the shaders for DXR and RTX for things like vertex positions, texture uvs, normals, binormals, tangents, and even colors.  We do this with a shader Structured Buffer.

## Structured Buffer
If you have been following along then you may already have some ideas about how to do this.  Should be easy right?
1.  Create the SRV in the hit root signature for the structured buffer.
2.  Add the root signature for each shader that needs access
3.  Pass the address of the buffer to the GPU for each shader that needs access
4.  Create the structured buffer in the shader file
5.  Make sure the structured buffer and vertex buffers match

## 15.1 Root Signatures
