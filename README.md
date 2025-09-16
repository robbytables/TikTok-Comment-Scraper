# TikTok Comment Scraper

A Python tool for collecting comments and replies from TikTok videos for academic research purposes.

## Overview

This script enables researchers to systematically collect comments and their associated replies from TikTok videos. It was developed specifically for academic research in areas such as human-computer interaction, social media studies, digital anthropology, and computational social science. **NOTE** You'll need some basic understanding of how to run Python scripts to install and run this software. If it behave well, great. Otherwise, you might need some level of Python coding abilities to troubleshoot or understand what's going on.

## Features

- Scrape comments and replies from TikTok videos
- Batch processing of multiple URLs via CSV input
- Single URL testing mode for exploratory analysis
- Research-focused data output format
- Rate limiting to respect platform resources

## Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Setup

1. Clone this repository:
```bash
git clone https://github.com/robbytables/TikTok-Comment-Scraper.git
cd TikTok-Comment-Scraper
```

2. Create a virtual environment:
```bash
python3 -m venv ttscrape
source ttscrape/bin/activate  # On Windows: ttscrape\Scripts\activate
```

3. Install dependencies:
```bash
pip3 install -r requirements.txt
```

## Usage

### Basic Usage

Run the scraper:
```bash
python3 ttscrape.py
```

### Single URL Testing

For testing or exploring a single video's comments, you can provide a TikTok URL directly when prompted. This mode does not write data to files and is useful for:
- Initial data exploration
- Testing the tool's functionality
- Checking data quality before batch processing

### Batch Processing

For systematic data collection:

1. Add TikTok video URLs to `tiktok_urls.csv` (one URL per line)
2. Run the script as above
3. The tool will process all URLs and save results to output files

### Input Format

The `tiktok_urls.csv` file should contain one TikTok video URL per line:
```
https://www.tiktok.com/@username/video/1234567890
https://www.tiktok.com/@username/video/0987654321
```

## Data Output

The scraper collects the following data points:
- Comment text
- Comment metadata (timestamp, likes, etc.)
- Reply text and metadata
- User information (as publicly available)
- Video association

*Note: Specific output format details depend on the current implementation. Check the output files for the exact data structure.*

## Ethical Considerations

### Research Ethics

This tool is intended solely for legitimate academic research. Before using this scraper, researchers should:

- Obtain appropriate Institutional Review Board (IRB) approval where required
- Consider the ethical implications of collecting social media data
- Respect user privacy and platform terms of service
- Follow institutional guidelines for human subjects research
- Consider data minimization principles (collect only what is necessary)

### Responsible Use

- **Rate Limiting**: The scraper includes rate limiting to avoid overwhelming TikTok's servers
- **Respect robots.txt**: Be aware of platform policies regarding automated access
- **Data Storage**: Implement appropriate security measures for collected data
- **Anonymization**: Consider anonymizing or pseudonymizing data when possible
- **Data Retention**: Establish clear data retention and deletion policies

## Legal Considerations

- Review TikTok's Terms of Service before use
- Ensure compliance with relevant data protection regulations (GDPR, CCPA, etc.)
- Consider copyright implications of collecting user-generated content
- Consult with your institution's legal counsel if needed

## Limitations

- Subject to changes in TikTok's website structure and anti-scraping measures
- May not capture all comments due to dynamic loading or privacy settings
- Rate limiting may affect data collection speed
- Not suitable for real-time data collection

## Troubleshooting

### Common Issues

1. **Installation Errors**: Ensure you're using Python 3.7+ and have updated pip
2. **Connection Issues**: Check your internet connection and try again
3. **URL Errors**: Verify that TikTok URLs are properly formatted and accessible
4. **Rate Limiting**: If you encounter rate limits, wait before retrying
5. **Odd Scraping Behavior**: Note that TikTok may change the format of the web elements at any time. If that's the case, you'll need to update the parsing strategy- and please submit a PR! (See Contributing section below).

### Getting Help

For technical issues:
1. Check existing GitHub issues
2. Create a new issue with detailed error information
3. Include Python version, operating system, and error messages

## Contributing

Contributions are welcome, especially from the research community. Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add appropriate tests
5. Submit a pull request

### Areas for Contribution

- Improved error handling
- Additional data export formats
- Enhanced rate limiting
- Documentation improvements

## Academic Citation

If you use this tool in your research, please cite it appropriately. Consider including:

- The repository URL
- The version or commit hash used
- The date of data collection
- Any modifications made to the original code

Example citation format:
```
[Author Name]. (Year). TikTok Comment Scraper. GitHub repository. 
https://github.com/robbytables/TikTok-Comment-Scraper
```

## Related Work

This tool may be useful for research in:
- Social media linguistics and discourse analysis
- Platform studies and digital culture research
- Human-computer interaction studies
- Computational social science
- Digital ethnography and anthropology

## License

This software is being made available via the GNU General Public License v3.0. See `LICENSE` file for more information.


## Disclaimer

This tool is provided for academic research purposes only. Users are responsible for ensuring their use complies with applicable laws, regulations, institutional policies, and platform terms of service. The authors assume no liability for misuse of this tool.

## Support

For academic collaborations or research-specific questions, please open an issue or contact the maintainers through appropriate academic channels.

---

**Research Responsibly** This tool supports important academic research, but ethical considerations should always be your first priority.
