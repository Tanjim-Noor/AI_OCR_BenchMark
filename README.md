# AI OCR BenchMark

A comprehensive system for benchmarking and comparing the performance of various AI models on Optical Character Recognition (OCR) tasks with structured data extraction.

## Features

- **Multi-Model Support**: Seamlessly switch between and compare performance across Google Gemini, OpenAI GPT, and Anthropic Claude.
- **Structured Data Extraction**: Specialized in extracting complex data from documents like invoices, receipts, and payslips into structured JSON format.
- **Batch Processing**: Efficiently process entire directories of images for large-scale benchmarking.
- **Performance Analytics**: Track and compare model accuracy, processing time, and success rates across different prompt versions.
- **Image Optimization**: Built-in image resizing and compression to optimize API usage and improve processing speed.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/AI_OCR_BenchMark.git
   cd AI_OCR_BenchMark
   ```

2. **Install dependencies**:
   It is recommended to use a virtual environment.
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   Copy the `.env.example` file to `.env` and add your API keys:
   ```bash
   cp .env.example .env
   ```
   Fill in your keys in the `.env` file:
   - `GOOGLE_API_KEY`
   - `OPENAI_API_KEY`
   - `ANTHROPIC_API_KEY`

## Quick Start / Usage

The project is primarily driven through Jupyter Notebooks:

1. **Main OCR & Benchmarking**:
   Open [image_to_text.ipynb](image_to_text.ipynb) to run the core OCR logic. This notebook contains the `OCRBenchmark` class which handles image processing, model interaction, and result scoring.

2. **Prompt Engineering & API Calls**:
   Refer to [api_call.ipynb](api_call.ipynb) for examples of how to construct specialized prompts for different document types (e.g., cash expenses, payslips) and how to make direct API calls.

3. **Running a Benchmark**:
   - Configure your image directory and ground truth data in the notebook.
   - Select the models you wish to test.
   - Execute the benchmark cells to generate results in the `OCR_Benchmark_result/` directory.

## Project Structure

- [image_to_text.ipynb](image_to_text.ipynb): The primary entry point containing the core OCR and benchmarking implementation.
- [api_call.ipynb](api_call.ipynb): Utility notebook for prompt management and sample API interactions.
- `OCR_Benchmark_result/`: Stores detailed JSON reports of benchmark runs, including model performance metrics.
- `OCR_Output/`: Contains raw OCR extraction results and intermediate scoring data.
- [requirements.txt](requirements.txt): List of required Python packages.
- [.env.example](.env.example): Template for required environment variables.

## Configuration

You can adjust image processing settings globally in [image_to_text.ipynb](image_to_text.ipynb):

- `ENABLE_IMAGE_OPTIMIZATION`: Toggle image resizing (default: `True`).
- `IMAGE_RESIZE_RATIO`: Scale factor for resizing (default: `0.5`).
- `MAX_IMAGE_DIMENSION`: Maximum width/height in pixels (default: `1024`).
- `JPEG_QUALITY`: Compression quality for JPEG images (default: `70`).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.
