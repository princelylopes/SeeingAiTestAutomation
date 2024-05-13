# SeeingAiTestAutomation - Household Navigation
The script runs some automated test cases using appium and java on a android device, to test the Seeing AI app for household object detection.

## Algorithm

1. The test cases information is given in a `.json` file. 
2. The script reads the `.json` file and stores that information in a list. 
3. The script opens the app and accepts the terms and conditions.
4. The script shares the images from the photos app to the Seeing AI app and compares the generated reseults with the expected results.
5. If the expected output is a substring of the actual output the test is considered as pass.
6. The script gives the pass percentage at the end and writes the test case results to a `.json` file.

## expected_outputs.json file format
 
`expected_outputs.json` file. 

```
{
    "test_cases": [
        {
            "test_number": "01",
            "result": "water bottle",
            "scenario": "Dark Lighting",
            "actualResult": "",
            "status": ""
        },
        {
            "test_number": "02",
            "result": "bean bag",
            "scenario": "Dark Lighting",
            "actualResult": "",
            "status": ""
        },
        ...
    ]
}
```

## actual_outputs.json file format
 
`actual_outputs.json` file.

```
[
    {
        "test_number":"01",
        "result":"water bottle",
        "scenario":"Dark Lighting",
        "actualResult":"A close-up of a water bottle"
    },
    {
        "test_number":"02",
        "result":"bean bag",
        "scenario":"Dark Lighting",
        "actualResult":"A woman lying on a bean bag"
    },
    ...
]
```

## Sample Test Case Result Printing
```
TestCase No.: 26
Scenario: Color Light
Expected Result: rocking chair
Actual Result: A group of white rocking chairs on a porch
Pass

TestCase No.: 27
Scenario: Color Dark
Expected Result: dining table
Actual Result: A table and chairs in a room
Fail
```


## Sample Test Analysis
```
XXXXXXXXXXXXXXXXXXX

Test Statistics -----------------------------
Pass: 15 | Fail: 14 | Total: 29
Pass %: 51.724137931034484%

XXXXXXXXXXXXXXXXXXX

Test Coverage -----------------------------
water bottle | bean bag | bean bag | work desk | tumbler | rocking chair | baby bottle | leather shoes | water bottle | work desk | baby bottle | office chair | office chair | baby bottle | water bottle | baby bottle | office chair | sport shoes | rocking chair | water bottle | bean bag | bean bag | baby bottle | rocking chair | water bottle | rocking chair | dining table | sport shoes | leather shoes | 

XXXXXXXXXXXXXXXXXXX

Test Quality Assurance Criteria -----------------------------
A test is considered to be passed if the actual output given by the application has a substring
 of the expected output that is given in the expected_outputs.json file.
 If this cindition is not satisfied the test is considered to fail

XXXXXXXXXXXXXXXXXXX

Test Summary -----------------------------
The script ran tests for total 29 test cases out of which 51.724137931034484% passed
The summary for various scenarios is listed below:
Scenario: Orientation Vertical | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Material Leather | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Material Plastic | Pass%:  66.66667 | Fail%:  33.333336 | Total:  3.0

Scenario: Material Cloth | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Color Light | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Quality Blur | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Color Dark | Pass%:  0.0 | Fail%:  100.0 | Total:  2.0

Scenario: Quality Normal | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Bright Lighting | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Orientation Inverted | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Dark Lighting | Pass%:  100.0 | Fail%:  0.0 | Total:  2.0

Scenario: Orientation Horizontal | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Material Wood | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0

Scenario: Material Metal | Pass%:  50.0 | Fail%:  50.0 | Total:  2.0
```

# Script video demo

Video Link: https://drive.google.com/file/d/1EM7NWKahXYODYIOR0ngYjVOd54CGjxJE/view?usp=sharing
