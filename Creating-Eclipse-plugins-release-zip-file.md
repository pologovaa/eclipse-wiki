Following is an guide how to create distributable release file for
Eclipse for GNU Toolchain for ARC.

1. Create tag for release: `$ git tag arc-2014.12`
2. Clean all past artifacts: `$ git clean -dfx`
3. Start Eclipse
4. Build plugins. That is important, because even when it is not done,
"publishing step" will somehow succeed, but will produce plugins that
are only partially functional.
    1. Make sure that "Project / Build Automatically" is checked
    2. Go to "Project / Clean"
    3. Check "Clean all projects"
    4. Press OK button
5. Open `site.xml` file of "ARC GNU Eclipse Update Site"
6. Press "Build All"
7. Zip contents of "updatesite" folder. Note that contents of this folder
should be zipped, not the folder itself. Files `.gitignore` and `.project`
should be excluded from zip.