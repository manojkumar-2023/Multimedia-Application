# Multimedia Application

## A description of the two features I built and how they work

>> I included Search and sorting feature to the multimedia app.

1. Search Feature : The search feature allows users to search for specific files based on their names. When users type a search query in the search input field, the app filters the files based on the query and displays only the files whose names contain the search query. The search is case-insensitive, meaning it matches files regardless of the letter case. The search functionality helps users quickly find files by typing a part of the file name they are looking for.

2. Sorting Feature : The sorting feature allows users to sort the files based on their attributes such as typet, the files are displayed in the order they were added. Users can sort files based on the "Type" which type of is there is it 'video','audio','document','images'.


## An explanation of why I chose these two features and why I think they are appropriate additions to the Multimedia Web App.

I chose the search and sorting features for the multimedia web app because they provide essential functionalities that enhance user experience and improve file management capabilities. Here's why I think they are appropriate additions to the app.

Search Feature:
The search feature is essential for any application dealing with a large number of files. In a multimedia app, users often accumulate a significant number of files over time, and manually scrolling through a long list of files can be time-consuming and inefficient. By implementing a search feature, users can quickly locate specific files by typing a part of the file name they are looking for. It improves productivity and helps users find files with ease.

Sorting Feature:
The sorting feature allows users to organize their files based on different attributes. In a multimedia app, files can have attributes like  type. Sorting files based on these attributes provides flexibility in organizing and managing files according to user preferences. It provides a structured view of files and enables efficient file management.

Overall, the search and sorting features complement each other in improving file management within the multimedia web app. The search feature enables quick and precise file retrieval, while the sorting feature enhances organization and accessibility. Together, they enhance user experience, save time, and make it easier for users to navigate and work with their multimedia files effectively.


## An explanation of how your code works.

1.The state variables are initialized using the useState hook:

- myFiles: Represents the list of files to be displayed.
- selectedFile: Represents the currently selected file.
- filePath: Represents the path for the file server.
- showChartModal: Controls the visibility of the chart modal.
- searchQuery: Stores the search query entered by the user.
- selectedFileType: Stores the selected file type for filtering.

2.The useEffect hook is used to set the initial value of myFiles state by assigning the imported data array. This useEffect hook runs only once when the component mounts.

3. The filteredFiles constant is created by filtering the myFiles array based on the selected file type (selectedFileType). If no type is selected, all files are shown.

- The file container consists of two sections:
   - The file list: Displays the filtered files as a list of clickable file items.       The map function is used to iterate over the filteredFiles array and create a       <div> element for each file.
  - The file viewer: Displays the details and content of the selected file based on      its type. This section conditionally renders different components (VideoPlayer,     AudioPlayer, DocumentViewer, ImageViewer) based on the selectedFile type.
    The search functionality:

4. The search input field is bound to the searchQuery state, and its value is updated as the user types.
    The filteredFiles are further filtered based on the searchQuery using the           includes method. Only files whose names contain the search query (case-             insensitive) are displayed.
    The sort functionality:

The file type select dropdown is bound to the selectedFileType state, and its value is updated when the user selects a different option.
The filteredFiles are filtered again based on the selectedFileType. If no type is selected (''), all files are displayed. Otherwise, only files matching the selected type are shown.
Other functionalities:

The rename button allows the user to rename the currently selected file by displaying a prompt dialog. The new name is entered by the user, and the file's name is updated in the myFiles state.
The delete button removes the selected file from the myFiles state.
The download button opens the selected file's path in a new browser tab.
The files breakdown button opens the chart modal by setting the showChartModal state to true.
  
  
