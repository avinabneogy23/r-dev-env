#### 1. Example Contribution Workflow using the R Dev Container

- To start working in R we will click on `R:(not attach)` which is in the bottom
  right of the VSCode window. This will open an R terminal for us.

  This is what you will see when you open the R terminal:

  ```console
    R version 4.3.2 (2023-10-31) -- "Eye Holes"
    Copyright (C) 2023 The R Foundation for Statistical Computing
    Platform: x86_64-pc-linux-gnu (64-bit)

    R is free software and comes with ABSOLUTELY NO WARRANTY.
    You are welcome to redistribute it under certain conditions.
    Type 'license()' or 'licence()' for distribution details.

    Natural language support but running in an English locale

    R is a collaborative project with many contributors.
    Type 'contributors()' for more information and
    'citation()' on how to cite R or R packages in publications.

    Type 'demo()' for some demos, 'help()' for on-line help, or
    'help.start()' for an HTML browser interface to help.
    Type 'q()' to quit R.

    .vsc.attach()
    > .vsc.attach()
  ```

  ![alt text](../assets/rdev11.png)

  ![alt text](../assets/rdev12.png)

- We can now run R commands. We will use the `utils::askYesNo()` function as an
  example

    ![alt text](../assets/rdev19.png)

```R
    > askYesNo("Is this a good example?")
    Is this a good example? (Yes/no/cancel) Yes
    [1] TRUE
```

#### 2. Editing Source Code

- Edit the source code of `utils::askYesNo()` to change the default options. The
  source code can be found in `$TOP_SRCDIR/src/library/utils/R/askYesNo.R`.
- You can redirect to that file using

```bash
code $TOP_SRCDIR/src/library/utils/R/askYesNo.R
```

**> Before edit:** ![alt text](../assets/rdev20.png)

```R title="askYesNo.R" linenums="20"
    prompts = getOption("askYesNo", gettext(c("Yes", "No", "Cancel"))),
```

**> With edit (for example - change to whatever you like!):**

![alt text](../assets/rdev21.png)

```R title="askYesNo.R" linenums="20"
    prompts = getOption("askYesNo", gettext(c("Oh yeah!", "Don't think so", "Cancel"))),
```

#### 3. Rebuild R

- We can re-build R with our changes. Since we have only modified the utils
  package, rebuilding R will only re-build the utils package.
- First we need to be inside $BUILDDIR.
- Quit R with `q()` or by closing the R terminal.
- In the bash terminal, change to the build directory:

```bash
cd $BUILDDIR
```

- Now run the `make` command to rebuild R with the changes you made in
  step 2. This will be much faster than the full build!

```bash
make
```

![alt text](../assets/rdev22.png)

- Optionally run `make check` to run R's test suite with your local changes. You
  may skip this step while you are iterating on a bug fix or other development,
  until you are ready to [create a patch](./patch_update.md).

- To use the re-built R, simply open a new R terminal.

#### 4. Cross check and Re-running Code

- Check the edit has worked as expected by re-running the example code: ![alt
text](../assets/rdev23.png)

```R
    > askYesNo("Is this a good example?")
    Is this a good example? (Oh yeah!/don't think so/cancel) Oh yeah!
    [1] TRUE
```
