## libraries installation ##
**Package Managers**  
- Using pip  
```python
# Installing a package
pip install <package_name>

# Upgrading an existing package
pip install --upgrade <package_name>

# Installing a specific version
pip install <package_name>==<version>

# Installing from a requirements file
pip install -r requirements.txt

# Installing multiple packages at once
pip install numpy pandas matplotlib
```  
**Virtual Environments**  
```python
# Creating a virtual environment
python -m venv myenv

# Activating the virtual environment
# Windows:
myenv\Scripts\activate
# macOS/Linux:
source myenv/bin/activate

# Deactivating the virtual environment
deactivate
```
**Virtual Environments**   
```python
# Creating a virtual environment
python -m venv myenv

# Activating the virtual environment
# Windows:
myenv\Scripts\activate
# macOS/Linux:
source myenv/bin/activate

# Deactivating the virtual environment
deactivate
```
**Managing Package Versions**    
```python
# Listing installed packages with their versions
pip list

# Checking details of a specific package
pip show <package_name>

# Installing a specific version of a package
pip install numpy==1.20.3
```
**Installing from Source or URLs**   
```python
# Installing from a GitHub repository
pip install git+https://github.com/owner/repo.git

# Installing from a local directory
pip install ./path/to/package
```
