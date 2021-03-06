# Setting up Jupyter Notebooks and Jupyter Lab to launch directly from Win10 Start Menu

1. Install Anaconda distribution with recommended settings
2. Manually update PATH to make Python and Jupyter available to all programs outside Anaconda

> `C:\ProgramData\Anaconda3; `
> `C:\ProgramData\Anaconda3\Scripts; `
> `C:\ProgramData\Anaconda3\Library\bin; `

3. Update the default working folder for Jupyter
  - enter this in Anaconda prompt
  
      `jupyter notebook --generate-config`
    
  - this generates a new file `C:\Users\username\\.jupyter\jupyter_notebook_config.py`
  - edit this file and uncomment and update the line below (use your preferred location here, remember to use double backslashes for path)
  
      `c.NotebookApp.notebook_dir = 'D:\\dev\\code'`

4. Place these two batch files in a local folder -  `Launch Jupyter Lab.bat` & `Launch Jupyter Notebook.bat` - along with the icon files (available in the repo)
5. Right-click them and "Send to > Desktop (create shortcut)"
6. Move these shortcut files to the Start Menu folder
> `C:\ProgramData\Microsoft\Windows\Start Menu\Programs`
7. Right-click the shortcut files and select Properties > Advanced and select the checkbox 'Run as administrator'

![Properties](properties-screenshot.gif)

8. Also select Properties > Change Icon > Browse > select the corresponding ico file
9. Optionally right-click these items in Start menu and select 'Pin to Start"

![ScreenShot](startmenu-screenshot.gif)
