# Grand Tour (Bally 1964)

This is a test table using my VPX Grand Tour (Bally 1964). It uses **HDRP 12.1** and **Unity 2021.3.0f1**.

Note: Anything above Unity 2021.3.0 currently doesn't work. In order to install 2021.3.0, open the Unity hub, choose *Installs*, click *Install Editor*, *Archive*, and on the *download archive* link. Then, under *Unity 2021.x*, click the *Unity Hub* button under *Unity 2021.3.0f1 (12 Apr, 2022)*. This should get to you back into the hub, where you can install 2021.3.0.

## Usage

We've referenced the VPE packages locally since it makes things easier for the dev team. In the future, you will just need to open this project in Unity without any further actions.

1. Open a console and go to the folder where you would like to clone the VPE repositories. If you haven't already, you'll probably need to install [.NET Core](https://dotnet.microsoft.com/en-us/download/dotnet/3.1) to compile.

```bash
git clone https://github.com/Scottacus64/GrandTourVPE.git
git clone https://github.com/VisualPinball/VisualPinball.Unity.Hdrp.git
git clone https://github.com/VisualPinball/VisualPinball.Unity.AssetLibrary.git
git clone https://github.com/VisualPinball/VisualPinball.Engine.PinMAME.git
git clone https://github.com/VisualPinball/VisualPinball.Unity.VisualScripting.git
git clone https://github.com/freezy/VisualPinball.Engine.git
```

Then, compile the test project which copies the native dependencies to the Unity folder, as well as the PinMAME project.

<details open>
  <summary>Windows x64</summary>
  
```bash
dotnet build VisualPinball.Engine/VisualPinball.Engine.Test/VisualPinball.Engine.Test.csproj -c Release -r win-x64
dotnet build VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME.csproj -c Release -r win-x64
```
</details>

<details>
  <summary>MacOS - Intel</summary>
  
```bash
dotnet build VisualPinball.Engine/VisualPinball.Engine.Test/VisualPinball.Engine.Test.csproj -c Release -r osx-x64
dotnet build VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME.csproj -c Release -r osx-x64
  ```
</details>

<details>
  <summary>MacOS - Apple Silicon</summary>
  
```bash
dotnet build VisualPinball.Engine/VisualPinball.Engine.Test/VisualPinball.Engine.Test.csproj -c Release -r osx-arm64
dotnet build VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME.csproj -c Release -r osx-arm64
  ```
</details>

<details>
  <summary>Linux x64</summary>
  
```bash
dotnet build VisualPinball.Engine/VisualPinball.Engine.Test/VisualPinball.Engine.Test.csproj -c Release -r linux-x64
dotnet build VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME/VisualPinball.Engine.PinMAME.csproj -c Release -r linux-x64
  ```
</details>

2. Open the project at `GrandTourVPE` in Unity.

3. Open the GT table by clicking on *File -> Open Scene* and choosing `Assets/GrandTourVPE.unity`.
