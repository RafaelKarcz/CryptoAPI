Cryptocurrency Data Collector and Visualizer
==============================================

This document provides instructions for setting up the Python environment on a Linux system using Anaconda and Conda, and it outlines the steps for running a detailed data collection and visualization of cryptocurrency data using the CoinMarketCap API.

Project Overview
----------------

This project consists of two main parts:

1. **Data Collection**: Fetches and stores the latest cryptocurrency data using the CoinMarketCap API.
2. **Data Visualization**: Processes and visualizes the collected data to provide insights into cryptocurrency performance.

The project includes the following files:

- `data_collector.ipynb`: Collects and saves cryptocurrency data.
- `data_visualizer.ipynb`: Loads, processes, and visualizes the collected data.

Environment Setup
-----------------

1. **Creating a New Conda Environment:**

   To create a new isolated environment for the project:

   .. code-block:: bash

      conda create --name crypto_env python=your_python_version

   This command creates a new environment named ``crypto_env`` with your specified Python (e.g. 3.11.9).

2. **Activating the Environment:**

   Activate the created environment with the following command:

   .. code-block:: bash

      conda activate crypto_env

   This ensures that any Python operations or package installations are confined to this environment.

3. **Installing Jupyter Lab:**

   Install Jupyter Lab to work with notebooks and code interactively:

   .. code-block:: bash

      conda install -c conda-forge jupyterlab

   Jupyter Lab is installed from the Conda-Forge channel.

4. **Starting Jupyter Lab:**

   To launch Jupyter Lab:

   .. code-block:: bash

      jupyter lab

   This command opens Jupyter Lab in the default web browser.

5. **Additional Package Installations:**

   Install additional packages required for data manipulation and visualization:

   .. code-block:: bash

      conda install pandas requests matplotlib seaborn

CoinMarketCap API Setup
-----------------------

1. **Creating a Free Account:**

   To access the CoinMarketCap API, you need to create a free account on CoinMarketCap:

   - Go to `https://coinmarketcap.com/`
   - Sign up for a free account.
   - Once registered, navigate to the API section to get your free API key.

2. **Checking the Latest Documentation:**

   Ensure you are familiar with the latest CoinMarketCap API documentation:

   - Visit `https://coinmarketcap.com/api/documentation/v1/` to view the latest API documentation.
   - Review the available endpoints and usage limits.

Project Execution
-----------------

Data Collection
~~~~~~~~~~~~~~~

The `data_collector.ipynb` script collects the latest cryptocurrency data from the CoinMarketCap API and saves it to a CSV file. Follow these steps to run the data collection:

1. Open the `data_collector.ipynb` notebook in Jupyter Lab.
2. Execute the cells sequentially to run the script.

The data collection script fetches data for the top 15 cryptocurrencies and appends the data to `crypto_data.csv` every 24 hours.

Data Visualization
~~~~~~~~~~~~~~~~~~~~~~~

The `data_visualizer.ipynb` script loads the collected data, processes it, and creates various visualizations. Follow these steps to run the data visualization:

1. Open the `data_visualizer.ipynb` notebook in Jupyter Lab.
2. Execute the cells sequentially to run the script.

The visualization script includes:

- **Displaying Collected Data**: Shows the collected data in an HTML format.
- **Aggregating Data**: Groups and averages percentage changes for different cryptocurrencies.
- **Plotting Data**: Creates point plots for percentage changes and line plots for cryptocurrency prices over time.

Acknowledgments
---------------

- `CoinMarketCap <https://coinmarketcap.com>`_ for offering free API usage
- `AlexTheAnalyst <https://github.com/AlexTheAnalyst>`_ for making this project a reality.

Contributing
------------

Contributions to this project are welcome. Please ensure to maintain the environment specifications and follow the coding standards used in this project.

License
-------

This project is licensed under the MIT License - see the `LICENSE <LICENSE>`_ file for details.
