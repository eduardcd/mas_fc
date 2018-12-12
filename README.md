# Project Object list merger

This project was originally created to merge the input lists that are delivered by 2 different algorithms that perceive objects. Those lists are an array of tuples that contain the following information (name_object,id_object,percentage_certainty). The algorithm presented should be able of get the tuple with the highest perrcentage of certainty, also should be able of handle complex situations. Some of them are defined on the test cases.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them
In order to be able of execute the tests pytest should be installed on your computer. 
The following command can be used from terminal in order to do so.

```
sudo apt install python-pytest
```

### Installing

A step by step series of examples that tell you how to get a development env running

Firstly from terminal run the above command to install the proper software, this will allow you to execute tests
This should trough a confirmation statement or like my case say that you have already installed the latest version.

![Install Pytest](https://drive.google.com/open?id=1pvsQqOLITP6mSviVgaumesNFUQKrJoyg)

```
eduardo@eduardo-AERO-15XV8:~$ sudo apt install python-pytest
[sudo] password for eduardo: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
python-pytest is already the newest version (2.8.7-4).
The following packages were automatically installed and are no longer required:
  linux-euclid-tools-4.4.0-9028 linux-headers-4.15.0-38
  linux-headers-4.15.0-38-generic linux-headers-4.4.0-139
  linux-headers-4.4.0-139-generic linux-image-4.15.0-38-generic
  linux-image-4.4.0-139-generic linux-image-extra-4.4.0-139-generic
  linux-modules-4.15.0-38-generic linux-modules-extra-4.15.0-38-generic
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 40 not upgraded.
```
Now you will be able of run the test cases



## Running the tests

Explain how to run the automated tests for this system
Secondly, you should chage the path to your folder where the repository was cloned (in my case) 

![Git Folder Test](https://drive.google.com/open?id=1tK7JhUPTPHhvXHqgDhMe-ZJ_wpy9K9PV)

```
 eduardo@eduardo-AERO-15XV8:~/Documents/AST/Project/project$
```

After that you should send the command that allow to execute all the test located inside that folder

![Git Command Execute Test](https://drive.google.com/open?id=1dREvmuJh5iu5HUjntkaMOkb6qNdR5S65)

```
 eduardo@eduardo-AERO-15XV8:~/Documents/AST/Project/project$ PYTHONPATH=. py.test -v
```

This will execute the test cases found which always shall named with the "test_" string if one of the files is not an executable the test will be skipped.

![Test Cases Executed](https://drive.google.com/open?id=195hgjktZBj95MzB60jupotjF0PzdUvQB)

```
eduardo@eduardo-AERO-15XV8:~/Documents/AST/Project/project$ PYTHONPATH=. py.test -v
================================ test session starts =================================
platform linux2 -- Python 2.7.12, pytest-2.8.7, py-1.4.31, pluggy-0.3.1 -- /usr/bin/python
cachedir: .cache
rootdir: /home/eduardo/Documents/AST/Project/project, inifile: 
collected 9 items 

test_Data.py::test_calculate PASSED
test_Data.py::test_calculate2 PASSED
test_Data_update_1.py::test_calculate1 PASSED
test_Data_update_1.py::test_calculate2 PASSED
test_Data_update_1.py::test_calculate3 PASSED
test_Data_update_1.py::test_calculate4 PASSED
test_Data_update_1.py::test_calculate5 PASSED
test_Data_update_1.py::test_calculate6 PASSED
Test Results/test_update_1 passing.txt SKIPPED

======================== 8 passed, 1 skipped in 0.04 seconds =========================
```


### Break down into end to end tests

Those test where defined to attempt executing complex situations for merging the lists

In this case given 2 lists of tuples containign the necessary information the implementation should be able of return the object with the higest probability of certain

```
rgbd = [('knife',1, .94),('knife',1, .69),('knife',1, .89)]
rgb =  [('knife',1, .99),('fork', 3, .99)]

Expected output = [('knife', 1, .99), ('fork',3, .99)]
```

## Deployment

Clone the project to your local repository, we recommend to do some refactoring in order to implement it on to your project

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Vahid Mohammadi Gahrooei** - *Initial work* 
  **Eduardo Cervantes Dueñas** - *Initial work*

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks for the authors of the image recognition algorithms.
* Deebul for being part of this

something
