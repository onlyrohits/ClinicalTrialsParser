ClinicalTrialsParser
====================

Python classes / functions to parse Clinical Trial data in the form of XML returned from clinicaltrials.gov. Older version also allows for parsing of Json returned from Lilly COI API.

Workflow at the moment: 

1. Make a list of IDs to focus on
    - From the simple txt file with the 10 (or more) we want to focus on

2. Get the studies listed on the ID list
    - Run get_key_studies.py
    - This will save the study XML into the ct_xml folder

3.  Convert the raw XML to raw JSON, add geolocation data
    - run xml_to_json.py

4. Convert the raw XML into osf JSON 
    - use clinical_trials_parser.py


For the future, when we'd like to update every day...

1. Get a list of studies that have been updated since yesterday
    - Run update_key_studies.py
    - saves a list called updated_ids.txt

2. Run get_key_studies again with the updated_ids.txt list?
    - What do we do with the updated files? Rename and move into archive??


