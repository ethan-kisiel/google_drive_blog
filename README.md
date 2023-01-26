
# Google API Blog

This is a back end written in python with flask, which leverages the Google Docs and Google Drive API's to automatically manage and update content.

#
# Theory
The main program will consist of two threads.  The first thread will be responsible for answering requests/delivering content from a NoSQL database(I have decided on a NoSQL database because the purpose of the database is only to store documents/document data). The second thread will be responsible for continuously checking the google drive location which is designated for stroing the blog posts(Google Documents). This thread will fetch all documents which are marked for publishing, and compare the resulting list of documents to the documents stored in the NoSQL databse. Any changes found between the database and the results of fetch request will be applied to the databse. The google docs api will be used for getting specific information on the formatting and information contained in each document.
