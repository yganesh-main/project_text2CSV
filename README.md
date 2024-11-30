**Text to CSV Conversion Using AWS S3 and Lambda
**Overview

This project automates the conversion of text files (.txt) to CSV format (.csv) using AWS S3 and Lambda. It also provides a user-friendly interface built with Streamlit for uploading .txt files and downloading the converted .csv files.
**Folder Structure

.
├── frontend-app.py       # Streamlit app for user interaction
├── iam-policy.json       # IAM policy for Lambda and S3 access
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies for the project
└── t2c-lambda.py         # Lambda function for text-to-CSV conversion

**Features

    AWS S3 Integration:
        .txt files uploaded to the S3 bucket trigger a Lambda function.
        The Lambda function converts .txt files into .csv format and reuploads them to the bucket.

    Streamlit Interface:
        Users can upload .txt files, monitor the conversion process, and download .csv files.
        Provides a simple and interactive way to manage files.

    Automation:
        Eliminates manual file conversions by automating the process through AWS Lambda.

Setup Instructions
1. Install Dependencies

Install the required Python packages using requirements.txt:

pip install -r requirements.txt

2. Configure AWS

    Ensure you have an S3 bucket set up.
    Use the iam-policy.json file to create an IAM role with the necessary permissions for Lambda and S3.

3. Deploy Lambda Function

    Upload the t2c-lambda.py to AWS Lambda.
    Attach the IAM role created earlier to the Lambda function.
    Configure an S3 trigger for .txt file uploads.

4. Run the Streamlit App

Launch the Streamlit app to upload and download files:

streamlit run frontend-app.py

**Technologies Used

    AWS S3: For cloud file storage.
    AWS Lambda: For processing file conversions.
    Streamlit: For creating the web interface.
    Python: For scripting the Lambda function and Streamlit app.

**Future Enhancements

    Add support for additional file formats.
    Enable cross-account S3 bucket operations.
    Implement real-time progress updates in the Streamlit app.