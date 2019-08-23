### general:
  - parameter --go leave the button [exit to menu] in interface though it leads to exit to os instead
  - mouse grabbing not released  when switch app under x11 and lose focus
    
  - client side lua api is either confused or non working.
most likely problem is here https://github.com/minetest/minetest/blob/master/src/client/renderingengine.cpp#L325

### port specific:

Using irrlicht 1.9.x GLES (tested on : OpenGL ES-CM 1.1 Mesa 18.0.5)

   - when building against GLES + x11 there's a small final linking problem since link.txt will miss a -lGL with the -lEGL
