# RafiuREADME-page
// Function that returns a license badge based on the selected license
// If no license is selected, returns an empty string
function renderLicenseBadge(license) {
  if (!license || license === 'None') {
    return '';
  }
  return `![License](https://img.shields.io/badge/license-${license.replace(' ', '%20')}-green.svg)`;
}

// Function that returns the link to the license's documentation
// If no license is selected, returns an empty string
function renderLicenseLink(license) {
  if (!license || license === 'None') {
    return '';
  }
  switch (license) {
    case 'MIT':
      return 'https://opensource.org/licenses/MIT';
    case 'Apache 2.0':
      return 'https://www.apache.org/licenses/LICENSE-2.0';
    case 'GPL 3.0':
      return 'https://www.gnu.org/licenses/gpl-3.0.en.html';
    case 'BSD 3':
      return 'https://opensource.org/licenses/BSD-3-Clause';
    default:
      return '';
  }
}

// Function that returns the license section of the README
// If no license is selected, returns an empty string
function renderLicenseSection(license) {
  if (!license || license === 'None') {
    return '';
  }
  return `## License

This project is licensed under the [${license}](${renderLicenseLink(license)}) license.`;
}

// Function to generate markdown content for README.md
function generateMarkdown(data) {
  return `# ${data.title}

${renderLicenseBadge(data.license)}

## Description
${data.description}

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contributing](#contributing)
- [Tests](#tests)
- [Questions](#questions)

## Installation
\`\`\`
${data.installation}
\`\`\`

## Usage
${data.usage}

${renderLicenseSection(data.license)}

## Contributing
${data.contributing}

## Tests
\`\`\`
${data.tests}
\`\`\`

## Questions
If you have any questions, please reach out:
- GitHub: [${data.github}](https://github.com/${data.github})
- Email: ${data.email}
`;
}

module.exports = generateMarkdown;


  Email: links
  LinkedIn: links
  Github: links
  Additional Information

 ** I’m always eager to connect with fellow professionals and share insights about the DevOp industry.
