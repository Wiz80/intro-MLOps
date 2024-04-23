<p align="center">
  <img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100" alt="project-logo">
</p>
<p align="center">
    <h1 align="center">MLOps</h1>
</p>
<p align="center">
    <em>Empowering AI innovation, one deployment at a time.</em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/Wiz80/intro-MLOps?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/Wiz80/intro-MLOps?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/Wiz80/intro-MLOps?style=default&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/Wiz80/intro-MLOps?style=default&color=0080ff" alt="repo-language-count">
<p>
<p align="center">
	<!-- default option, no dependency badges. -->
</p>

<br><!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary><br>

- [ Overview](#-overview)
- [ Features](#-features)
- [ Repository Structure](#-repository-structure)
- [ Modules](#-modules)
- [ Getting Started](#-getting-started)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Tests](#-tests)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ License](#-license)
- [ Acknowledgments](#-acknowledgments)
</details>
<hr>

##  Overview

The intro-MLOps project provides a robust Machine Learning Operations solution. It facilitates automated model training, endpoint testing, version control for datasets and models, and continuous integration/continuous deployment workflows. Leveraging FastAPI and DVC, it guarantees data integrity, reproducibility, and model efficacy. With a central API for making predictions and a structured model training process using Pydantic models and Gradient Boosting Regressor, intro-MLOps streamlines machine learning development and deployment, ensuring efficiency and scalability in ML operations.

---

##  Features

|    |   Feature         | Description |
|----|-------------------|---------------------------------------------------------------|
| ⚙️  | **Architecture**  | The project consists of an MLOps pipeline implemented with FastAPI for API handling and model deployment. It includes Dockerfile setup, DVC for data versioning, and GitHub Actions for CI/CD automation. Modular components for training, prediction, and data preparation enhance scalability and maintainability. |
| 🔩 | **Code Quality**  | The codebase maintains high quality with clear structure and adherence to PEP8 standards. It includes separate modules for model training, API handling, and data preparation, facilitating readability and maintenance. Extensive use of Python typing and consistent coding style ensures robustness and ease of development. |
| 📄 | **Documentation** | The project includes detailed documentation files such as `initializer.sh`, `requirements.txt`, and descriptive comments in the codebase. The README provides essential information about project setup, dependencies, and usage instructions. Comprehensive documentation enables seamless integration and collaboration among team members. |
| 🔌 | **Integrations**  | Key integrations include FastAPI for API development, DVC for data versioning, GitHub Actions for CI/CD automation, and Python libraries like Pandas, Scikit-learn, and Tornado. These integrations enhance productivity, maintainability, and scalability of the MLOps pipeline. |
| 🧩 | **Modularity**    | The codebase exhibits high modularity with separate modules for API handling, model training, and data preparation. Each component is well-encapsulated, promoting reusability and easy extension of functionalities. Modular design facilitates code maintenance and integration of new features. |
| 🧪 | **Testing**       | Testing is conducted using FastAPI's TestClient in the `tests.py` file to verify the null prediction endpoint. This ensures the reliability and correctness of the API response. Including testing frameworks like pytest ensures code quality and robustness of the MLOps pipeline. |
| ⚡️  | **Performance**   | The project demonstrates efficient performance with optimized code for model training, prediction, and API deployment. Leveraging tools like Gradient Boosting Regressor and FastAPI enhances speed and resource utilization, leading to reliable model predictions and API responses. |
| 🛡️ | **Security**      | Security measures are implemented, such as generating JSON files for service account keys in `setter.py` to enhance access control and data protection. Dependency on libraries like Cryptography ensures secure handling of sensitive information within the project. |
| 📦 | **Dependencies**  | Key dependencies include FastAPI, DVC, Pandas, Scikit-learn, Tornado, and various other libraries for model training, API development, and data versioning. These libraries enhance the functionality and performance of the MLOps pipeline. |

---

##  Repository Structure

```sh
└── intro-MLOps/
    ├── .github
    │   └── workflows
    ├── Dockerfile
    ├── LICENSE
    ├── README.md
    ├── api
    │   ├── app
    │   └── main.py
    ├── dataset
    │   ├── finantials.csv.dvc
    │   ├── movies.csv.dvc
    │   └── opening_gross.csv.dvc
    ├── dvc.lock
    ├── dvc.yaml
    ├── initializer.sh
    ├── model
    │   ├── model.pkl
    │   └── model.pkl.dvc
    ├── notebooks
    │   ├── .ipynb_checkpoints
    │   └── Modeling.ipynb
    ├── report.txt
    ├── requirements.txt
    ├── src
    │   ├── prepare.py
    │   ├── requirements.txt
    │   ├── train.py
    │   └── utils.py
    ├── tests.py
    └── utilities
        └── setter.py
```

---

##  Modules

<details closed><summary>.</summary>

| File                                                                                  | Summary                                                                                                                                                                                                                                                        |
| ---                                                                                   | ---                                                                                                                                                                                                                                                            |
| [initializer.sh](https://github.com/Wiz80/intro-MLOps/blob/master/initializer.sh)     | Starts the API server using Gunicorn and Uvicorn Worker with specified configurations from the main file in the api module.                                                                                                                                    |
| [requirements.txt](https://github.com/Wiz80/intro-MLOps/blob/master/requirements.txt) | Specifies dependencies for the project, enabling integration with various libraries and tools. Facilitates seamless execution and compatibility across different parts of the repository. Essential for maintaining a robust and functional project ecosystem. |
| [Dockerfile](https://github.com/Wiz80/intro-MLOps/blob/master/Dockerfile)             | Build Docker image for MLOps pipeline.-Set up Python environment.-Copy API and model to Docker image.-Execute initializer script.-Expose port 8000.-Implemented in Dockerfile within the MLOps repository.                                                     |
| [dvc.yaml](https://github.com/Wiz80/intro-MLOps/blob/master/dvc.yaml)                 | Defines the data preparation stage in the MLOps pipeline. Executes the `prepare.py` script to generate `full_data.csv` for downstream tasks. Central to ensuring data integrity and model efficacy.                                                            |
| [report.txt](https://github.com/Wiz80/intro-MLOps/blob/master/report.txt)             | Describes model pipeline using SimpleImputer and GradientBoostingRegressor. Highlights training, testing, and validation scores. Central to the machine learning model execution within the intro-MLOps repository.                                            |
| [tests.py](https://github.com/Wiz80/intro-MLOps/blob/master/tests.py)                 | Tests null prediction endpoint using FastAPIs TestClient against the main API. Verifies successful response status code and checks if the predicted worldwide gross is zero.                                                                                   |

</details>

<details closed><summary>dataset</summary>

| File                                                                                                    | Summary                                                                                                                                                                           |
| ---                                                                                                     | ---                                                                                                                                                                               |
| [movies.csv.dvc](https://github.com/Wiz80/intro-MLOps/blob/master/dataset/movies.csv.dvc)               | Enables tracking dataset versioning and integrity through metadata in movies.csv.dvc. Essential for ensuring data consistency and reproducibility in machine learning operations. |
| [opening_gross.csv.dvc](https://github.com/Wiz80/intro-MLOps/blob/master/dataset/opening_gross.csv.dvc) | Enables tracking and versioning of opening_gross.csv dataset file in intro-MLOps repository. Supports reproducibility and collaboration in machine learning operations.           |
| [finantials.csv.dvc](https://github.com/Wiz80/intro-MLOps/blob/master/dataset/finantials.csv.dvc)       | Generates hashed metadata for the `finantials.csv` dataset to track changes and versions effectively within the MLOps repository architecture.                                    |

</details>

<details closed><summary>utilities</summary>

| File                                                                              | Summary                                                                                                                                                    |
| ---                                                                               | ---                                                                                                                                                        |
| [setter.py](https://github.com/Wiz80/intro-MLOps/blob/master/utilities/setter.py) | Generates a JSON file from a base64-encoded key and prints the file path. This script facilitates the setup of service account keys for enhanced security. |

</details>

<details closed><summary>.github.workflows</summary>

| File                                                                                                                  | Summary                                                                                                                                                                                                   |
| ---                                                                                                                   | ---                                                                                                                                                                                                       |
| [continuos_training.yaml](https://github.com/Wiz80/intro-MLOps/blob/master/.github/workflows/continuos_training.yaml) | Automates model training using GitHub Actions.-Triggers workflow on dataset changes.-Builds and saves models.-Ensures continuous integration with the repository.                                         |
| [testing.yaml](https://github.com/Wiz80/intro-MLOps/blob/master/.github/workflows/testing.yaml)                       | Automates testing workflow with Github Actions. Executes unit tests, ensuring code quality and stability. Seamless integration within the repositorys MLOps architecture for efficient testing processes. |
| [ci_cd.yaml](https://github.com/Wiz80/intro-MLOps/blob/master/.github/workflows/ci_cd.yaml)                           | Automates CI/CD pipeline for the MLOps project. Sets up workflow actions for testing and building. Integrates with GitHub Actions for efficient development lifecycle management.                         |

</details>

<details closed><summary>model</summary>

| File                                                                                  | Summary                                                                                                                                                                                                           |
| ---                                                                                   | ---                                                                                                                                                                                                               |
| [model.pkl.dvc](https://github.com/Wiz80/intro-MLOps/blob/master/model/model.pkl.dvc) | Specifies meta-information for model.pkl.dvc, maintaining hash, size, path, and md5. Facilitates model versioning and tracking in ML pipeline with reproducibility and consistency across the project repository. |

</details>

<details closed><summary>api</summary>

| File                                                                    | Summary                                                                                                    |
| ---                                                                     | ---                                                                                                        |
| [main.py](https://github.com/Wiz80/intro-MLOps/blob/master/api/main.py) | Enables making model predictions using FastAPI, fetching prediction request data and returning a response. |

</details>

<details closed><summary>api.app</summary>

| File                                                                            | Summary                                                                                                                                                     |
| ---                                                                             | ---                                                                                                                                                         |
| [models.py](https://github.com/Wiz80/intro-MLOps/blob/master/api/app/models.py) | Defines Pydantic models for input and output data, facilitating data validation and serialization in the ML API. Enhances data integrity and API responses. |
| [utils.py](https://github.com/Wiz80/intro-MLOps/blob/master/api/app/utils.py)   | Retrieves a machine learning model and transforms input into a DataFrame using the specified model path and Pydantic BaseModel.                             |
| [views.py](https://github.com/Wiz80/intro-MLOps/blob/master/api/app/views.py)   | Generates predictions using the loaded model based on request data, with a minimum prediction value of 0.                                                   |

</details>

<details closed><summary>notebooks</summary>

| File                                                                                        | Summary                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ---                                                                                         | ---                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Modeling.ipynb](https://github.com/Wiz80/intro-MLOps/blob/master/notebooks/Modeling.ipynb) | This code file in the intro-MLOps repository serves the critical function of training machine learning models for financial and movie data. It leverages the data stored in DVC-tracked files to build and save models for predictive analysis. The model training process is implemented in a structured and reproducible manner through the use of Python scripts, ensuring the accuracy and scalability of the predictive models. |

</details>

<details closed><summary>notebooks..ipynb_checkpoints</summary>

| File                                                                                                                                 | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---                                                                                                                                  | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Modeling-checkpoint.ipynb](https://github.com/Wiz80/intro-MLOps/blob/master/notebooks/.ipynb_checkpoints/Modeling-checkpoint.ipynb) | This code file in the parent repository `intro-MLOps` serves the critical purpose of training a machine learning model using the specified dataset and features. It contributes to the overall architecture by encapsulating the model training logic, thus enabling the automation of model updates and improvements. The file plays a pivotal role in ensuring the efficiency and effectiveness of the machine learning operations within the repository. |

</details>

<details closed><summary>src</summary>

| File                                                                                      | Summary                                                                                                                                                                                                                                                                               |
| ---                                                                                       | ---                                                                                                                                                                                                                                                                                   |
| [requirements.txt](https://github.com/Wiz80/intro-MLOps/blob/master/src/requirements.txt) | Enumerates dependencies for the projects source code, ensuring the necessary libraries for building and running the software are readily available.                                                                                                                                   |
| [utils.py](https://github.com/Wiz80/intro-MLOps/blob/master/src/utils.py)                 | Updates and saves model state, generates a descriptive report on model performance, and visualizes test set predictions performance. These critical features enhance monitoring and analysis capabilities in the machine learning operations workflow in the repository.              |
| [train.py](https://github.com/Wiz80/intro-MLOps/blob/master/src/train.py)                 | Trains a Gradient Boosting Regressor model using cross-validation and hyperparameter tuning. Evaluates model performance and updates the best model. Logs key steps, ensures model quality, and saves metrics. Contributing to the ML Ops pipeline with robust training capabilities. |
| [prepare.py](https://github.com/Wiz80/intro-MLOps/blob/master/src/prepare.py)             | Prepares** movie dataset by fetching, cleaning, and merging financial, opening gross, and movie data. Generates complete dataset for machine learning model training. Integrates with DVC for data versioning in the MLOps project architecture.                                      |

</details>

---

##  Getting Started

**System Requirements:**

* **Python**: `version x.y.z`

###  Installation

<h4>From <code>source</code></h4>

> 1. Clone the intro-MLOps repository:
>
> ```console
> $ git clone https://github.com/Wiz80/intro-MLOps
> ```
>
> 2. Change to the project directory:
> ```console
> $ cd intro-MLOps
> ```
>
> 3. Install the dependencies:
> ```console
> $ pip install -r requirements.txt
> ```

###  Usage

<h4>From <code>source</code></h4>

> Run intro-MLOps using the command below:
> ```console
> $ python main.py
> ```

###  Tests

> Run the test suite using the command below:
> ```console
> $ pytest
> ```

---

##  Project Roadmap

- [X] `► INSERT-TASK-1`
- [ ] `► INSERT-TASK-2`
- [ ] `► ...`

---

##  Contributing

Contributions are welcome! Here are several ways you can contribute:

- **[Report Issues](https://github.com/Wiz80/intro-MLOps/issues)**: Submit bugs found or log feature requests for the `intro-MLOps` project.
- **[Submit Pull Requests](https://github.com/Wiz80/intro-MLOps/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.
- **[Join the Discussions](https://github.com/Wiz80/intro-MLOps/discussions)**: Share your insights, provide feedback, or ask questions.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/Wiz80/intro-MLOps
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="center">
   <a href="https://github.com{/Wiz80/intro-MLOps/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=Wiz80/intro-MLOps">
   </a>
</p>
</details>

---

##  License

This project is protected under the [SELECT-A-LICENSE](https://choosealicense.com/licenses) License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

##  Acknowledgments

- List any resources, contributors, inspiration, etc. here.

[**Return**](#-overview)

---
