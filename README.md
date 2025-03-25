# SourceDetailSpriteViewer
Source Engine; Visualize position of detail sprites on images for detail props   
Drag and Drop an image onto the left pane (Must be a .png or .jpeg, use [VTFEdit](https://nemstools.github.io/pages/VTFLib-Download.html) to export Textures)  
In the the right pane, the `sprite`-fields on each sprite part will be used to overlay a grid showing where the textures will be.

# Installation
Download the file. The file is a single, self-contained .html file. Run it in any browser. Simple as that!

## Example detail.vbsp snippet
```
custom_forest_floor_01
{
    density 1600
    GrassTex
    {
        alpha 0
        RoseFlower
        {
            sprite "0 0 83 128 512"
            spritesize "0.5 0.05 7 13"
        }
        FernShrub
        {
            sprite "120 0 136 256 512"
            spritesize "0.5 0.05 17 28"
        }
        GrassTuft
        {
            sprite "0 199 120 57 512"
            spritesize "0.5 0 20 10"
        }
        PinkFlower
        {
            sprite "83 0 38 128 512"
            spritesize "0.5 0 6 18"
        }
        LushShrub
        {
            sprite "256 128 172 128 512"
            spritesize "0.5 0 32 21"
        }
    }
}
```
