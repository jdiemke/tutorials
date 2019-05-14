# 3D Computer Graphics

## Content

1. Introduction
2. Transformations
3. Clipping
4. Texture Mapping
   1. Affine Texture Mapping
   2. Perspective Texture Mapping
5. References

## 1. Introduction

## 2. Transformations

## 3. Clipping

## 4. Texture Mapping

### 4.1. Affine Texture Mapping

### 4.2. Perspective Texture Mapping

Perspective texture mapping is a little bit more tricky.
The problem with perspective texture mapping is that texture coordinates `[u,v]` as well as the `z` value can not be interpolated linearly in screen space since linear interpolation does not take perspective into account. Interestingly, though, it can be proofen that `1/z`, `u/z` and `v/z` are linear in screen space, and therefore can be interpolated linearly [1].

## 5. References

1. M. Kalms, Perspective Texturemapping, 1997
   http://www.lysator.liu.se/~mikaelk/doc/perspectivetexture/
