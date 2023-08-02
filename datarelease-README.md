------------------ 
TABLE OF CONTENTS
------------------

* GENERAL INFORMATION
  * TITLE
  * AUTHORS AND BEST CONTACT
  * RECOMMENDED CITATION
  * LICENSES
  * USEFUL LINKS
* DATE OF DATA COLLECTION
* FILE ORGANIZATION
* FUNDING
* ADDITIONAL NOTES/COMMENTS

**Note:** *If you are viewing on Zenodo, please check the GitHub link <insert link> for updates to this file.*

--------------------
GENERAL INFORMATION
--------------------

1. **Publication or Dataset Title:**  

2. **Authors:**

3. **Contact Information**  <who should be contacted about this data>
* Name: <FName LName>
* Organization/institution: <Contact person affiliation>
* Email: <institutional email address>

4. **Links to publications that cite or use the data:** 
<include DOI and APA citation to publications that use this data, if applicable>

5. **Recommended citation for this dataset:**  
<Following standard APA citation format>  
<Author Last, Author F. (Year). Title of data set (Version number) [Description of form]. Location: Name of producer.> 

6. **Licenses/restrictions placed on the data:** 
<e.g. CC BY https://creativecommons.org/licenses/by/4.0/>
  
7. **For more information, go to:** <Insert links where applicable to tissue-atlas.org or other landing page>

-------------------
FILE ORGANIZATION
------------------

1. **FILE NAMING CONVENTIONS:**   
Each file follows the following naming convention:  

2. **FILE TYPES/SUMMARY:**
Each folder corresponds to a patient sample (N). The following files are available for each patient and are located on [Synapse/AWS/Etc].

 <Data should be uploaded to the appropriate public repository where applicable>
 <DATA SHOULD NOT BE STORED ON GITHUB>
 <If you are not sure which repository to use for your data type reach out to your Data Managers>
 
|File Type     | Description                                                                        | Location|
|--------      | ----------------------------------------------------------------------------------|---------|
|N.ome.tif	   | Stitched multiplex CyCIF image pyramid in ome.tif format                           | AWS     |
|N_HE.vsi	     | Hematoxylin and Eosin stained image of adjacent FFPE tissue section in .vsi format | AWS     |
|\_N\_HE\_/    | folder: raw image data accompanying .vsi file                                      | AWS     |
|markers.csv   | list of all markers in ome.tif image                                               | [Synapse](https://www.synapse.org/)|
|N.csv         | single-cell feature table, including intensity data for all channels               | Synapse |
|N_ROI.csv     | X and Y coordinates for histologically annotated regions in CyCIF and H&E images   | Synapse |
|raw/          | folder of raw IF image data in .rcpnl format                                       | AWS     |
|segmentation/ |  folder of segmentation maps for tissue image in .tif format                       | AWS     |
| | Sequencing data | GEO|

 **Synapse Library:** [Edit this to link directly to your public Synapse Library](https://www.synapse.org/)  
  >*Free account registration is required to download files from Synapse.*  
 
 **Images and metadata are available in the bucket at the following AWS location:** [ADD BUCKET DETAILS]   
  >*Files available through AWS S3 are made available using a “requester pays” model.*   
  >*The person downloading the data must have an AWS account, and AWS will charge the user's account $0.10/GB for downloading all or part 
of the data.*
 
*Note About Accessing AWS Data:*

>To browse and download the data use either a graphical file transfer application
that supports S3 such as [CyberDuck](https://cyberduck.io), or the [AWS CLI
tools](https://aws.amazon.com/cli/). A graphical tool may be more convenient but
the CLI tools will likely offer higher download speeds. Please refer to the
documentation for your chosen tool on how to sign in and enable access to
requester-pays buckets. There is unfortunately no web-browser-based mechanism
for accessing a requester-pays bucket. Keep in mind the download costs, which
will run over $200 for downloading one copy of the entire dataset. For users who
wish to perform processing within AWS to avoid transfer charges, note that the
bucket is located in the `us-east-1` region so any other resources must be
instantiated in this same region.

3. **FILE LIST** <*list all files (or folders, as appropriate for dataset organization) contained in the Synapse repository, with a brief description*>

**N.ome.tif**

|Patient | File Name       | Location| File size |
|------- | ----------------|---------|-----------|
|ID | ID.ome.tif | AWS     | 90.6 GB   |


**N_HE.vsi**

|Patient | File Name      | Location| File size|
|--------| ---------------|---------|----------|
|ID | ID.ome.tif_HE.vsi | AWS     | 531.2 KB |


**\_N\_HE\_/**

|Patient | File Name   | Location| File size|
|------- | ------------|---------|----------|
|ID | frame_t.ets | AWS     | 928.7 MB |

**markers.csv**

|Patient | File Name   | Synapse ID  | File size|
|------- | ----------- |------------ |----------|
|ID | markers.csv | syn12345678 | 530 bytes|

**N.csv**

|Patient | File Name   | Synapse ID | File size |
|------- | ------------|------------|-----------|
|ID | ID.csv |  |  |

**N_ROI.csv**

|Patient | File Name       | Synapse ID  | File size|
|------- | ----------------|-------------|----------|
|ID | ID_ROI.csv |  |    |

**raw/**

|Patient | Number of Files | Folder size| Location|
|------- |-----------------|------------|---------|
|ID | 13              |     |      |


**segmentation/**

|Patient | Number of Files | Folder size| Location|
|------- |-----------------|------------|---------|
|ID |               |     |      |


--------------------------
FUNDING
--------------------------
Please add relevant funding details <This can be copied directly from your manuscript> 
 
 --------------------------
ADDITIONAL NOTES/COMMENTS
--------------------------

Please let **(Name, contact information)** know if any errors are found in this data.  
