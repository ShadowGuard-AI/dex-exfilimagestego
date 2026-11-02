![Banner](banner.png)

# dex-ExfilImageStego
Embeds data within a PNG image using LSB steganography. Takes data and an image as input, outputs a new PNG image containing the hidden data. - Focused on Simulates data exfiltration techniques by generating realistic fake data (e.g., usernames, passwords, financial records), staging it in various formats, and then simulating its transmission over different protocols (e.g., HTTP, DNS tunneling). Used for testing data loss prevention (DLP) systems and incident response playbooks.

## Install
`git clone https://github.com/ShadowGuard-AI/dex-exfilimagestego`

## Usage
`python3 main.py IMAGE_PATH`

## Parameters
- `IMAGE_PATH`: Path to the PNG image to use as a cover image.
- `-h`: Show help message and exit
- `-o`: Path to save the steganographically encoded PNG image (default: `output.png`).
- `-d`: Path to a file containing data to embed. If not provided, fake data is generated.
- `-g`: Generate fake data for embedding. Overrides --data_file.
- `-s`: Size of fake data to generate, in bytes (default: 1024). Only applicable with `-g`.
- `-e`: Simulated exfiltration protocol, `http` or `dns` (optional).

## Verified run note

The parameters above are taken from the argument parser in `main.py`. A live run in this environment is blocked because the `faker` package is not installed here, so even `--help` stops at that import; no run result is claimed for this tool.

## License
Licensed under the terms in LICENSE.
