Here's a sample README documentation for your Node.js project. This documentation will guide users on how to set up, run, and test the API endpoints.

---

# Node.js File System API

This project is a simple Node.js API that allows users to create text files with the current timestamp and retrieve all text files from a specified folder. The API is built using Express and the Node.js File System (fs) module.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Starting the Server](#starting-the-server)
  - [API Endpoints](#api-endpoints)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js**: Ensure that Node.js and npm (Node Package Manager) are installed on your machine.
- **Git**: Make sure Git is installed for version control.

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/nodejs-filesystem.git
   cd nodejs-filesystem
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

   This command will install all necessary packages listed in the `package.json` file, including Express.

## Usage

### Starting the Server

To start the server, run the following command:

```bash
node index.js
```

The server will start on `http://localhost:3000`. You should see the following message in your terminal:

```
Server running on http://localhost:3000
```

### API Endpoints

The API provides the following endpoints:

#### 1. Create a Text File with the Current Timestamp

- **URL**: `/create-file`
- **Method**: `POST`
- **Description**: Creates a text file in the `files` directory with the current timestamp as the filename and content.
- **Response**: A success message with the filename.

**Example Request**:
```bash
POST http://localhost:3000/create-file
```

**Example Response**:
```json
{
  "message": "File 2024-09-03T10-20-30.123Z.txt created successfully"
}
```

#### 2. Retrieve All Text Files

- **URL**: `/files`
- **Method**: `GET`
- **Description**: Retrieves a list of all `.txt` files in the `files` directory.
- **Response**: A JSON array of filenames.

**Example Request**:
```bash
GET http://localhost:3000/files
```

**Example Response**:
```json
[
  "2024-09-03T10-20-30.123Z.txt",
  "2024-09-02T09-15-45.678Z.txt"
]
```

## Testing

You can test the API endpoints using [Postman](https://www.postman.com/downloads/) or `curl`.

### Using Postman

1. **Create a Text File**:  
   - Method: `POST`
   - URL: `http://localhost:3000/create-file`

2. **Retrieve All Text Files**:  
   - Method: `GET`
   - URL: `http://localhost:3000/files`

### Using Curl

```bash
# Create a new file
curl -X POST http://localhost:3000/create-file

# Retrieve all text files
curl http://localhost:3000/files
```

## Deployment

### Deploying on Render

1. **Push your code to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin master
   ```

2. **Deploy to Render**:
   - Sign up or log in to [Render](https://render.com/).
   - Create a new web service.
   - Link your GitHub repository.
   - Set the build command to `npm install` and the start command to `node index.js`.
   - Deploy your application.

### Submission

Create a text file with the following information:

- **Render URL**: Your Render deployment URL (e.g., `https://nodejs-filesystem-txkk.onrender.com`).
- **GitHub Repository URL**: (e.g., `https://github.com/yourusername/nodejs-filesystem`).
- **Last Committed Hash ID**: (e.g., `a1b2c3d4e5f6g7h8i9j0`).

## Contributing

If you'd like to contribute to this project, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

