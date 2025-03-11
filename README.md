# SBOM
# SBOM Finder for Software Applications and Apps

## Overview
SBOM Finder is a powerful tool designed to generate, analyze, and validate **Software Bill of Materials (SBOMs)** for software applications and mobile apps. It simplifies dependency management, enhances security vulnerability detection, and ensures compliance with industry standards, benefiting software developers, security professionals, and organizations. 

Supported SBOM formats include **CycloneDX** and **SPDX**.

## Features
- **SBOM Generation**: Automatically creates SBOMs from source code or existing artifacts.
- **Vulnerability Detection**: Identifies known vulnerabilities within your software dependencies.
- **Format Compatibility**: Supports industry-standard SBOM formats (CycloneDX, SPDX).
- **License Compliance**: Helps maintain compliance by identifying license conflicts and risks.
- **REST API**: Offers easy integration for automation and third-party tools.
- **Intuitive UI**: Provides an intuitive user interface suitable for both technical and non-technical users.
- **Automated Reports**: Offers comprehensive reporting for compliance audits and security assessments.

## Getting Started

### Requirements
- Python 3.8 or higher
- PostgreSQL
- Docker (optional for deployment)

### Installation
Clone the repository:
```bash
git clone https://github.com/your-username/sbom-finder.git
cd sbom-finder
```

Install dependencies:
```bash
pip install -r requirements.txt
```

### Running the Application
To start the application:
```bash
python main.py
```

### Docker Deployment
```bash
docker build -t sbom-finder .
docker run -p 8000:8000 sbom-finder
```

## Usage

### Generate SBOM
Run the following command to generate an SBOM in CycloneDX format:
```bash
python sbom_finder.py --input path/to/project --format cyclonedx
```

### Vulnerability Check
Scan an existing SBOM for vulnerabilities:
```bash
python sbom_finder.py --scan sbom.json
```

### REST API
Start the REST API server:
```bash
uvicorn app:main --host 0.0.0.0 --port 8000
```

Use the API endpoint to upload and analyze SBOMs:
```bash
curl -X POST -F "file=@sbom.json" http://localhost:8000/api/upload
```

## Configuration
Create or update a `.env` file with the following environment variables:
```bash
DB_HOST=localhost
DB_USER=admin
DB_PASS=password
API_KEY=your-api-key
```

## Contributing
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/my-feature`).
3. Commit your changes (`git commit -m 'Add my feature'`).
4. Push to the branch (`git push origin feature/my-feature`).
5. Open a pull request.

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contact
For questions or support, please contact [your-email@example.com](mailto:your-email@example.com) or open an issue on GitHub.
