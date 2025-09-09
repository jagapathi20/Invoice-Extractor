# MultiLanguage Invoice Extractor

A Streamlit web application that uses Google's Gemini AI to analyze and extract information from invoice images. This application can process invoices in multiple languages and answer questions about the uploaded invoice content.

## Features

- **Image Upload**: Support for JPG, JPEG, and PNG image formats
- **AI-Powered Analysis**: Uses Google's Gemini 2.5 Flash Lite model for intelligent invoice processing
- **Interactive Interface**: Clean and user-friendly Streamlit web interface
- **Multilanguage Support**: Can process invoices in various languages
- **Custom Queries**: Ask specific questions about the uploaded invoice

## Prerequisites

Before running this application, make sure you have:

- Python 3.7 or higher
- A Google AI API key (for Gemini access)

## Installation

1. **Clone the repository** (or download the project files):
   ```bash
   git clone <your-repository-url>
   cd multilanguage-invoice-extractor
   ```

2. **Install required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   - Create a `.env` file in the project root directory
   - Add your Google API key:
     ```
     GOOGLE_API_KEY=your_google_api_key_here
     ```

## Getting Your Google API Key

1. Go to the [Google AI Studio](https://aistudio.google.com/)
2. Sign in with your Google account
3. Create a new API key
4. Copy the API key to your `.env` file

## Usage

1. **Start the application**:
   ```bash
   streamlit run app.py
   ```

2. **Open your browser** and navigate to the URL displayed in the terminal (usually `http://localhost:8501`)

3. **Use the application**:
   - Enter a specific question about the invoice in the "Input Prompt" field
   - Upload an invoice image (JPG, JPEG, or PNG format)
   - Click "Tell me about the invoice" to get AI-powered analysis

## Example Queries

You can ask various questions about your invoices, such as:
- "What is the total amount on this invoice?"
- "Who is the vendor/supplier?"
- "What is the invoice date?"
- "List all the items and their quantities"
- "What is the tax amount?"
- "Extract all the contact information"

## Project Structure

```
multilanguage-invoice-extractor/
│
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env                  # Environment variables (create this)
└── README.md            # Project documentation
```

## Dependencies

- **streamlit**: Web application framework
- **google-generativeai**: Google's Generative AI SDK
- **python-dotenv**: Environment variable management
- **Pillow (PIL)**: Image processing
- **langchain**: LangChain framework (included for potential extensions)
- **PyPDF2**: PDF processing (included for potential extensions)
- **chromadb**: Vector database (included for potential extensions)

## Technical Details

- **AI Model**: Google Gemini 2.5 Flash Lite
- **Image Processing**: PIL (Python Imaging Library)
- **Web Framework**: Streamlit
- **Configuration**: Environment variables via python-dotenv

## Troubleshooting

### Common Issues

1. **"No file Uploaded" error**:
   - Make sure to upload an image before clicking the submit button

2. **API key errors**:
   - Verify your Google API key is correctly set in the `.env` file
   - Ensure your API key has access to the Gemini API

3. **Image format errors**:
   - Only JPG, JPEG, and PNG formats are supported
   - Ensure the image file is not corrupted

### Error Messages

- `FileNotFoundError: No file Uploaded`: Upload an image file before submitting
- API authentication errors: Check your Google API key configuration

## Future Enhancements

Potential improvements for this project:
- PDF invoice support (PyPDF2 is already included)
- Batch processing of multiple invoices
- Data export functionality (CSV, JSON)
- Invoice template recognition
- Integration with accounting systems
- Vector database storage for invoice history (ChromaDB is included)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source. Please check the repository for license details.

## Support

For issues and questions:
1. Check the troubleshooting section above
2. Review the Google Gemini API documentation
3. Create an issue in the repository

## Acknowledgments

- Google AI for the Gemini API
- Streamlit team for the excellent web framework
- The open-source community for the various libraries used
