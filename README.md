#  deployable-writerside-documentation
It can be a pain to configure the github actions CI for writerside, as it is not as foolproof at it seems. 
This template is for those having issues.

## Setting this up for your situation.
To make sure the deployment.yml works for you, you might need to change some things around, because the current id is 'hi'.

Do the following:
 1. Replace all occurrences of the (lowercase!!) id, denoted here as 'hi'.
    1. Think of, for example, 'hi.tree' -> '<your-id>.tree' (use ctrl + shift + f or your OS' equivalent.)
 2. Go to .github/workflows/deployment.yml and replace 
    1. `INSTANCE: 'Writerside/hi'` with INSTANCE: `'Writerside/<your lowercase id here>'` (if not already)
    2. `ARTIFACT: 'webHelpHI2-all.zip'` with `ARTIFACT: 'webHelp<YOUR ID IN UPPERCASE HERE>2-all.zip'`
 
It is important to note that you MUST have a 'Writerside' folder, wherein the c.list, <your lowercase id here>.tree, etc. lives.
This is required by JetBrains as well, as far as I know.
