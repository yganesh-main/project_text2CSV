**Text to CSV Conversion Using AWS S3 and Lambda**
**Overview**

This project automates the conversion of text files (.txt) to CSV format (.csv) using AWS S3 and Lambda. It also provides a user-friendly interface built with Streamlit for uploading .txt files and downloading the converted .csv files.
Folder Structure

.
├── frontend-app.py      # Streamlit app for user interaction
├── iam-policy.json      # IAM policy for Lambda and S3 access
├── README.md            # Project documentation
├── requirements.txt     # Python dependencies for the project
└── t2c-lambda.py        # Lambda function for text-to-CSV conversion

**Features**

**AWS S3 Integration**

1..txt files uploaded to the S3 bucket trigger a Lambda function.
2.The Lambda function converts the .txt files into .csv format and reuploads them to the same S3 bucket.

**Streamlit Interface**

    Users can upload .txt files, monitor the conversion process, and download the resulting .csv files.
    Provides a simple, interactive web interface for easy file management.

**Automation**

    Eliminates manual file conversion processes by automating everything through AWS Lambda.

**Setup Instructions**
1. **Install Dependencies**

    First, install the required Python packages listed in requirements.txt:

        pip install -r requirements.txt

2. **Configure AWS**

    Set up an S3 bucket where users will upload their .txt files.
    Use the iam-policy.json file to create an IAM role with the necessary permissions for Lambda and S3.

3. **Deploy Lambda Function**

    Upload the t2c-lambda.py file to AWS Lambda.
    Attach the IAM role (created earlier) to the Lambda function.
    Configure the Lambda function to be triggered by .txt file uploads to the S3 bucket.

4. **Run the Streamlit App**

    Launch the Streamlit app to enable users to upload and download files:

        streamlit run frontend-app.py

**Technologies Used**

    AWS S3: For cloud-based file storage.
    AWS Lambda: For processing the conversion of .txt to .csv.
    Streamlit: For creating the user interface.
    Python: For scripting the Lambda function and the Streamlit app.

**Future Enhancements**

    Support for additional file formats.
    Enable cross-account S3 bucket operations.
    Real-time progress updates for file conversion in the Streamlit app.