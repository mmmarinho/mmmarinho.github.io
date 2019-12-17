---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style type="text/css">
    
.bibbase_note {
    color: red;
    font-weight: bold;
}

.note {
    color: green;
    font-style: italic;
}

.groupby_dropdown {
  display: none;
}

</style>

<script>
// Store XMLHttpRequest and the JSON file location in variables
var xhr = new XMLHttpRequest();
var url = "https://api.elsevier.com/content/author?httpAccept=application/json&author_id=55537035800&field=citation-count&apiKey=81b027ac5f3ae6659a995219404f4544";

// Called whenever the readyState attribute changes 
xhr.onreadystatechange = function() {

  // Check if fetch request is done
  if (xhr.readyState == 4 && xhr.status == 200) { 
  
    // Parse the JSON string
    var jsonData = JSON.parse(xhr.responseText);
    
    // Call the showArtists(), passing in the parsed JSON string
    showArtists(jsonData);
  }
};

// Do the HTTP call using the url variable we specified above
xhr.open("GET", url, true);
xhr.send();

// Function that formats the string with HTML tags, then outputs the result
function showArtists(data) {
    var output = data
    
    // Output the data to the "artistlist" element
    document.getElementById("artistList").innerHTML = output;
}
</script>

<!-- The output appears here -->
<div id="artistList"></div>

### Researcher profiles
- [Google Scholar](https://scholar.google.com/citations?user=4yzonSsAAAAJ&hl)/[Scopus](https://www.scopus.com/authid/detail.uri?authorId=55537035800) profiles (for citations)
- [ResearchGate](https://www.researchgate.net/profile/Murilo_Marinho) profile (for researcher engagement)
- [arXiv](https://arxiv.org/search/cs?searchtype=author&query=Marinho%2C+M+M) profile (for pre-prints)

### Publication list
<script src="https://bibbase.org/show?bib=mmmarinho.github.io%2Ffiles%2Fmurilomarinho.bib&jsonp=1&group0=custom_type&css=mmmarinho.github.io/_sass/_bibbase.css&folding=1&nocache=1"></script> 
