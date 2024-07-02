<p align="center" width="100%">
  # Snap-in Development Challenge Documentation
</p>

#### [output snaps](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/blob/main/snaps.pdf)

## Step-1: Installation
- [Install DevRev CLI](https://developer.devrev.ai/snapin-development/references/cli-install)
- [Install jq](https://jqlang.github.io/jq/)
## Step-2: Log in to DevRev for authentication
To authenticate, run the following command:
```
devrev profiles authenticate -o sathyakumar -u sathyakumar.webdev@gmail.com
```
### Output
![authenticate](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/46dd19d8-a33e-40a0-aa3d-dc4ca894da91)

## Step-3: Creating a snap-in package
To create a snap-in package, run the following command:
```
devrev snap_in_package create-one --slug  HelloWorld | jq .
```
### Output
![snap_in_package](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/b0108e5d-8fc4-42b5-8665-27f5e17fe7a9)

## Step-4: Creating a snap-in version
To create a snap-in version, run the following command:
```
devrev snap_in_version create-one --manifest manifest.yaml --archive build.tar.gz | jq .
```
### Output
![Snap_in_version](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/238df6a1-5e7e-457f-8945-a17732c61888)

## Step-5: Installing a snap-in from a snap-in version
To create a snap-in from a snap-in version, run the following command:
```
devrev snap_in draft
```
### Output
![Snap_in_draft](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/5ec6335d-c614-4ebe-b87b-0ac3d024dbac)

## Step-6: Configuring the snap-in
The snap-in is installed in draft state. It may require some configuration before it can be deployed.
You can access snap-in configuration by using the URL generated by the draft command, or by navigating to the snap-ins page in the DevRev app.

Open your org website > goto settigns>Integrations>Snap-ins
Your snap-in will be available
### Output
![Snap_in](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/b1513b24-1a24-448f-9627-ed28c55029b2)

## Step-7: Deploying the snap-in
Once you have provided the required configuration, the Deploy snap-in button is enabled on the UI. Click on it to deploy the snap-in. That’s it, the snap-in should now be active and ready to use.

### Implemented output
![image](https://github.com/Febiecode/DevRev-Hello-World-Snap-in/assets/93641901/59a6254a-6f3f-4e92-9c11-f1f7e2f9001e)
