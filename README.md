
# Pet Store API Testing

## Overview

This repository contains Postman collections and Newman reports for testing the Pet Store API. The API testing is organized into various test cases covering different aspects of the Pet Store, including pet creation, retrieval, and deletion.

## Project Structure

- **DataFiles/**: Contains JSON files with test data used for data-driven testing.
  - `PetStore.json`: Test data for pets.
  - `Store.json`: Test data for store-related operations.
  - `User.json`: Test data for users.

- **Documentation/**: Contains project documentation.
  - `PetStoreProjectOverView.pdf`: Overview of the Pet Store project.
link for the postman Documentation :**https://documenter.getpostman.com/view/28929346/2sAXjSyTm2**



- **JenkinsReport/**: Contains reports generated from Jenkins builds.
  - `FunctionalityTests.txt`: Report of functionality tests.
  - `OrderDataDriven.txt`: Report of data-driven tests related to orders.
  - `PetDataDriven.txt`: Report of data-driven tests related to pets.
  - `UserDataDriven.txt`: Report of data-driven tests related to users.

- **PetStoreAPI_Tests.postman_collection.json**: The Postman collection for Pet Store API testing.

- **newman/**: Contains Newman reports.
  - `newman-FunctionalityTestRun-report-YYYY-MM-DD-HH-MM-SS.html`: Report of functionality tests run using Newman.
  - `newman-OrderDataDrivenRun-report-YYYY-MM-DD-HH-MM-SS.html`: Report of data-driven tests related to orders run using Newman.
  - `newman-PetDataDrivenRun-report-YYYY-MM-DD-HH-MM-SS.html`: Report of data-driven tests related to pets run using Newman.
  - `newman-UserDataDrivenRun-report-YYYY-MM-DD-HH-MM-SS.html`: Report of data-driven tests related to users run using Newman.

## Getting Started

### Prerequisites

- [Postman](https://www.postman.com/downloads/): To import and run the Postman collections.
- [Newman](https://github.com/postmanlabs/newman): Command-line tool for running Postman collections.
- [Jenkins](https://www.jenkins.io/): For continuous integration and running tests.

### Running Tests with Postman

1. **Import the Collection**: Open Postman and import the `PetStoreAPI_Tests.postman_collection.json` file.
2. **Run the Collection**: Select the collection and click "Run" to execute the tests.

### Running Tests with Newman

1. **Install Newman**: If not installed, install Newman using the following command:
   ```sh
   npm install -g newman

   ```
2. **Run the Collection**: Execute the tests using the following command:
   ```sh
   newman run PetStoreAPI_Tests.postman_collection.json
newman run "E:\Postman\PetstoreProject\PetStoreAPI_Tests.postman_collection.json" --folder  "FunctionalityTests" 
newman run "E:\Postman\PetstoreProject\PetStoreAPI_Tests.postman_collection.json" --folder  "Pet_DataDriven"  --iteration-data "E:\Postman\PetstoreProject\DataFiles\PetStore.json"
newman run "E:\Postman\PetstoreProject\PetStoreAPI_Tests.postman_collection.json" --folder  "OrderDataDriven"  --iteration-data "E:\Postman\PetstoreProject\DataFiles\Store.json" 
newman run "E:\Postman\PetstoreProject\PetStoreAPI_Tests.postman_collection.json" --folder  "UserDataDriven"  --iteration-data "E:\Postman\PetstoreProject\DataFiles\User.json"


   ```

### Running Tests with Jenkins

1. **Configure Jenkins**: Set up a Jenkins job to execute Newman commands. Ensure that Newman is installed on the Jenkins server.
2. **Create a Jenkins Pipeline**: Define a pipeline to run the tests and generate reports.

## Contributing

If you want to contribute to this project, please fork the repository and submit a pull request with your changes. Ensure that your changes do not break existing functionality.

## License

This project does not have a specific license. Feel free to use and modify the content as needed, but please note that you are responsible for ensuring compliance with any relevant laws and regulations.

## Contact

For any questions or issues, please contact Arava Venkata Jyothi at [aravavenkatajyothi@gmail.com](mailto:aravavenkatajyothi@gmail.com).
```
