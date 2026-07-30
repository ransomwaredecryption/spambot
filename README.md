# Spambot




> [!WARNING]
> real spambot and should be used on your own rish




## Operational Workflow

The tool environment relies on a master builder script to compile and structure customized deployment configurations. Users must deploy the entire repository folder structure locally.

### 1. Download & Environment Setup
1. Click the green **Code** button at the top right of this repository.
2. Select **Download ZIP** from the dropdown menu to capture all core resources.
3. Extract the contents of the downloaded ZIP archive into a dedicated directory on your local Windows system.

### 2. Configuration & Executable Generation
1. Launch **`Builder.exe`** from the extracted directory.
2. Within the graphical configuration control panel, specify your target infrastructure properties:
   - **Version / Timeout (sec)**: Establish tracking attributes and system timeout intervals (e.g., `0777`).
   - **Config Server 1 & 2**: Input the target listener IP addresses or fallback destination networks.
   - **Routing Endpoints**: Configure active paths for validation and execution endpoints (`Alive page`, `Report page`, `Update path`, `Config script`, `Post logs page`).
3. Click the **Build** button at the bottom left of the panel interface.
4. Upon successful validation, the environment will update **`config.xml`** and output your custom-tailored **`out.exe`** worker binary directly into the root folder.

### 3. Execution
1. Open an elevated console instance (Command Prompt or PowerShell) inside your local directory.
2. Initiate the generated worker binary to begin processing workloads:
   ```powershell
   .\out.exe
   ```

## Repository Architecture

*   **`Builder.exe`**: The standalone Delphi graphical management panel and binary compiler interface.
*   **`config.xml`**: The structured XML data container populated dynamically by the builder interface.
*   **`out.exe`**: The custom deployment binary output generated upon a successful compilation sequence.
*   **`.gitignore`**: Formatted specifically for the Delphi developer pipeline; excludes temporary binary data (`.dcu`, `.identcache`, `.stat`) to maintain source cleanliness.

## Technical Specifications

*   **Target Platform**: Windows 10, Windows 11, or Windows Server environments.
*   **Dependencies**: Standalone native binary execution. No external runtime frameworks required.
