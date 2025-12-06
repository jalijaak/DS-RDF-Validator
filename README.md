[README.md](https://github.com/user-attachments/files/23991000/README.md)

[**Launch the RDF Vocabulary Manager Application**](index.html)

# **3DEXPERIENCE RDF Vocabulary Manager & Validator**

This is a single-file web application (rdf\_validator.html) designed to create, validate, and manage RDF/XML vocabularies used for tagging and data structuring within the 3DEXPERIENCE platform.  
It provides a user-friendly interface to define predicates (attributes) and essential ontology metadata, ensuring the output conforms to 3DEXPERIENCE standards, particularly the use of the ds6w (6W) taxonomy.

## **Key Features**

* **Vocabulary Metadata Editor:** Easily set the Vocabulary Name (Ontology Label), Version, and Comment. The Namespace URI is automatically generated based on the name.  
* **Attribute Management:** Define attributes (predicates) with their unique ID, human-readable label, and descriptive comment.  
* **6W Taxonomy Integration:** Assign each attribute to one of the six ds6w dimensions (what, who, when, where, why, how) via a simple dropdown.  
* **Validation & Error Reporting:** Real-time validation checks for critical errors such as:  
  * Missing or invalid Vocabulary Name.  
  * Duplicate Attribute IDs.  
  * Empty Attribute IDs.  
  * Common typos (e.g., "desciption").  
* **Import/Export Capabilities:**  
  * **Load RDF:** Upload existing .rdf or .xml files to parse and edit the vocabulary.  
  * **Export RDF:** Generate and download a complete, compliant RDF/XML file.  
  * **Import/Export CSV:** Manage attributes using standard CSV files.  
* **Live RDF Source:** Displays the generated RDF/XML code in real-time.

## **Usage**

The application is entirely self-contained within the rdf\_validator.html file.

1. **Open the Application:** Open rdf\_validator.html in any modern web browser.  
2. **Set Vocabulary Settings:** Fill out the **Vocabulary Settings** section (Name, Version, and Comment). The Name is crucial as it defines the Namespace URI.  
3. **Manage Attributes:**  
   * Click **Add Attribute** to manually add a new row.  
   * Edit the **ID**, **Label**, **6W Dimension**, and **Comment** directly in the table.  
   * Use the **Import CSV** button to load a bulk list of attributes.  
4. **Check Validation:** The **Validation Report** on the left panel provides feedback on any issues (Critical or Warnings). The status badge (**Ready to Build**, **Warnings**, or **Critical Issues**) updates instantly.  
5. **Export:** Click **Export RDF** to generate the final vocabulary file (\[VocabularyName\].rdf).

## **Technical Notes**

* **Technology Stack:** Pure HTML, Tailwind CSS (via CDN), and Vanilla JavaScript.  
* **Namespace Convention:** All vocabularies use the fixed base: http://www.3ds.com/vocabularies/\[VocabularyName\]/.  
* **6W Mapping:** Attributes are mapped to rdfs:subPropertyOf pointing to the relevant ds6w:what, ds6w:who, etc.
