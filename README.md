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
            "actualResult": ""
        },
        {
            "test_number": "02",
            "result": "bean bag",
            "scenario": "Dark Lighting",
            "actualResult": ""
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

# Script video demo

Video Link: https://drive.google.com/file/d/1EM7NWKahXYODYIOR0ngYjVOd54CGjxJE/view?usp=sharing
