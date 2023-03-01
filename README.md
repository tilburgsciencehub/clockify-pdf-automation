<a name="readme-top"></a>
<h3 align="center">Clockify to PDF automation</h3>
<p align="center">
    Automate filling in the PDF forms with hours from Clockify
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#workflow">Workflow</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project
At Tilburg Science Hub, we track our working hours in [Clockify](https://clockify.me/). In the past, to be paid for the hours we worked, we had to manually complete the [form](https://www.tilburguniversity.edu/system/files?file=download/Hours%20under%20standby%20contract%20UK%20as%20of%202023.pdf) each month, based on our Clockify records. Then, the form had to be signed by our supervisor. Finally, we had to send the signed form to [HR services](hrservices@tilburguniversity.edu) before the 5th of each month.

However, as our team grew, this process became messy with sending the forms back and forth. Not only was it time-consuming for us to manually enter the hours from Clockify and convert them to decimals, but it was also labour-intensive for our supervisors to receive and sign each form separately.

Therefore, we decided to create a script, which will retrieve our working hours via [Clockify API](https://clockify.me/developers-api) and fill in the PDF forms for each of us.  This way, one person can run the script on the 1st of each month and send all of the forms to a supervisor at once.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow the steps:

### Prerequisites
In order to be able to run the script, you need to install the [PyPDF2](https://pypi.org/project/PyPDF2/) and [holidays](https://pypi.org/project/holidays/) libraries.

  ```sh
  pip install PyPDF2
  ```
  
  ```sh
  pip install holidays
  ```  

### Installation

1. Generate your Clockify API key in [Profile Settings](https://clockify.me/user/settings).

*Warning: in order to access Billable Hours, you need to have Admin role in Clockify.*

2. Store your API key as an environment variable called *Clockify-API-Key*.

*Learn how to [Configure Environment Variables](https://tilburgsciencehub.com/building-blocks/store-and-document-your-data/store-data/environment-variables/).*

3. Clone the repository.
   ```sh
   git clone https://github.com/tilburgsciencehub/clockify-pdf-automation
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- WORKFLOW -->
## Workflow
The following workflow describes a new process of getting the forms signed:
1. **Everyone:** By the end of each month, make sure you logged all your hours.
2. **One assigned person:** Run the script on the 1st of each month.
3. **One assigned person:** Share all of the forms with a supervisor (typically Hannes or Tobias).
4. **One assigned person:** Receive the forms back from a supervisor and share them with the rest of Research Assistants.
5. **Everyone:** Send the form to [HR services](mailto:hrservices@tilburguniversity.edu) before the 5th of each month.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
