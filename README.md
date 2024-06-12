# Selenium Web Automation Script

This repository contains a Python script that automates web interactions using Selenium WebDriver. The script logs into a specified website, performs operations to add and delete documents and AI models, and handles error scenarios.

## Table of Contents

1. [Setup and Initialization](#setup-and-initialization)
2. [Login Function](#login-function)
3. [Add Bucket and Document Function](#add-bucket-and-document-function)
4. [Upload Documents Function](#upload-documents-function)
5. [Analyze Files Function](#analyze-files-function)
6. [Create AI and Translate Function](#create-ai-and-translate-function)
7. [Navigation Functions](#navigation-functions)
8. [Delete AI Function](#delete-ai-function)
9. [Delete Bucket Function](#delete-bucket-function)
10. [Main Function](#main-function)

## Setup and Initialization

```python
import os
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.keys import Keys
from webdriver_manager.chrome import ChromeDriverManager
import time

# Initialize the WebDriver
service = Service(ChromeDriverManager().install())
driver = webdriver.Chrome(service=service)
