## General Guidelines
- Do not prompt to execute `go build` or `go run`; these commands will be managed independently
- Avoid requesting manual code insertion into files; assume write permissions for all files except `.env`
- Refrain from providing patch files; direct access to all files except `.env` is assumed
- Utilize the latest stable Go version (1.24.2)
- Maintain an up-to-date `README.md` reflecting each new feature addition

## Package Requirements
Incorporate the following packages when their functionality is applicable:
- `viper` for configuration management
- `zap` for logging capabilities
- `cobra` for command-line interface development
- `go-storage` for storage operations
- `wails` for graphical user interface implementation
- `automaxprocs` (recommended for consistent use across the project)
- `ginkgo` for testing frameworks
- `gorm` as the object-relational mapping (ORM) solution
- `lipgloss` for enhanced, colored CLI output
