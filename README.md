# Hostel Management Web Application

## Objective

Develop a web application to digitalize the hospitality process for group accommodation. The application will allow users to upload two CSV files to efficiently allocate rooms in hostels, ensuring that group members with the same ID stay together, and adhering to hostel capacities and gender-specific accommodations.

## Features

- **CSV File Upload**: Users can upload two CSV files: one containing guest information and another containing hostel room details.
- **Room Allocation**: The system will automatically allocate rooms based on the uploaded data.
  - Group members with the same ID are kept together.
  - Room capacities are respected.
  - Gender-specific accommodations are enforced.
- **Dashboard**: A user-friendly dashboard to view room allocation results and manage uploads.
- **Error Handling**: Handles errors such as file format issues, missing data, and capacity violations.

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript, React
- **Backend**: Node.js, Express
- **Database**: MongoDB (optional, for persistence)
- **File Handling**: Multer (for handling file uploads)
- **Room Allocation Logic**: Custom algorithm to ensure group and gender-based accommodation

## Getting Started

### Prerequisites

- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/hostel-management.git
    ```
2. Navigate to the project directory:
    ```sh
    cd hostel-management
    ```
3. Install the dependencies:
    ```sh
    npm install
    ```

### Running the Application

1. Start the backend server:
    ```sh
    npm run server
    ```
2. Start the frontend development server:
    ```sh
    npm start
    ```

### Directory Structure

```plaintext
hostel-management/
├── client/                 # Frontend code (React app)
│   ├── public/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── App.js
│   │   ├── index.js
│   │   └── ...
│   └── package.json
├── server/                 # Backend code (Express app)
│   ├── controllers/        # Controllers for handling requests
│   ├── models/             # Data models (optional)
│   ├── routes/             # API routes
│   ├── services/           # Business logic
│   ├── utils/              # Utility functions
│   ├── app.js              # Main application file
│   └── ...
├── uploads/                # Directory for uploaded files
├── .gitignore
├── README.md
└── package.json
```

### API Endpoints

- `POST /api/upload-guests`: Upload guest CSV file.
- `POST /api/upload-rooms`: Upload room CSV file.
- `GET /api/allocate-rooms`: Trigger room allocation based on uploaded data.
- `GET /api/room-allocation`: Get the room allocation result.

### CSV File Formats

#### Guests CSV

| GroupID | Name      | Gender | Age |
|---------|-----------|--------|-----|
| 1       | John Doe  | Male   | 25  |
| 1       | Jane Doe  | Female | 24  |
| 2       | Alice     | Female | 22  |
| ...     | ...       | ...    | ... |

#### Rooms CSV

| RoomID | Capacity | Gender | 
|--------|----------|--------|
| 101    | 2        | Male   |
| 102    | 2        | Female |
| 103    | 4        | Male   |
| ...    | ...      | ...    |

### Contribution

1. Fork the repository.
2. Create a new branch:
    ```sh
    git checkout -b feature/your-feature-name
    ```
3. Make your changes and commit them:
    ```sh
    git commit -m 'Add some feature'
    ```
4. Push to the branch:
    ```sh
    git push origin feature/your-feature-name
    ```
5. Open a pull request.

---

Happy Coding!
