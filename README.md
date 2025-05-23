Below are some useful tools for developing custom assets in the Source engine
## 🗃 [.SMD viewer (calculates a models $bbox)](https://vitaplex.github.io/SourceUtils-Pages/smdviewer.html)
Drag and drop **.smd** files to view them in a **3D viewer**. Automatically calculates and displays the models `$bbox` for use in **.qc** files!
Meshes are also foolhardily editable by hand in the text area, if you're so inclined...
<details>
  <summary><strong>How to use</strong></summary>
    <h3>Basic usage</h3>
    <li>Drag & Drop files from your computer onto the page to view them </li>
    <li>Select multiple files from your computer and drag them all onto the page to open several .smd's at the same time! They will appear as one collective mesh.</li>
    <ul><li>Note that uploading alot of complex mesh data will slow down your browser</li></ul>
    <li>Gaze at your model, edit it or copy the value of <code>$bbox</code> (probably the only useful thing here). <code>$bbox</code> will take into account the size of all your meshes multiple .smd files were opened </li>
    <p>When a .smd is opened, it wil appear as a green, untextured version of your mesh. The yellow wireframe box around it is the models calculated bounding box (<code>$bbox</code>). This will be displayed in the top-right section of your screen</p>
    <h3>3D View Controls</h3>
    <li> <strong>Left-click + drag:</strong> Rotate view</li>
    <li> <strong>Right-click + drag:</strong> Pan view</li>
    <li> <strong>Scroll:</strong> Zoom</li>
    <li> <strong>Mouse3 + Pan up/down:</strong> Zoom in/out fast</li>
    <h3>Gameplay</h3>
    <img src="media/smdviewer.jpg">
</details>
<details>
  <summary><strong>.SMD format</strong></summary>
    <p>The second, third and fourth number in each line is the XYZ position of a single vertex. Modifying these values will manipulate the mesh on the screen</p>
    <a target="_blank" href="https://developer.valvesoftware.com/wiki/SMD#Triangles">SMD format - Valve Developer Community</a>
    <h3>About</h3>
    <pre>0 [PosX] [PosY] [PosZ] [NormX] [NormY] [NormZ] [U] [V] [links] [Bone ID] [Weight] [...</pre>
    <h3>Example</h3>
    <pre>
triangles
  Material
  0     1     1     2     0     1     0     0     0
  0    -1    -1     2     0     0     1     0     0
  0     1    -1     2     0     0     1     0     0
    </pre>
</details>

## 🖼 [Sprite detail viewer and editor](https://vitaplex.github.io/SourceUtils-Pages/spriteboundaryvisualizer.html)
Visualize position of detail sprites on images for detail props   
Drag and Drop an image onto the left pane (Must be a .png or .jpeg, [VTFEdit](https://nemstools.github.io/pages/VTFLib-Download.html) can be used to export Textures)  
In the the right pane, the `sprite`-fields on each sprite part will be used to overlay a grid showing where the textures will be.

<details>
  <summary><strong>Example detail.vbsp snippet</strong></summary>
  <pre>custom_forest_floor_01
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
</pre>

</details>
