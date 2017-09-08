# osjs
<h2>Search GitHub Projects</h2>

<div class="center">

 

<form id="search" onsubmit="return doSearch();">

  Search projects: <input type="text" name="q">

  <input type="button" onclick="doSearch()" value="Submit">

</form>

 

<script language="javascript">

var accounts = [

'ajaxorg', 

'alexa', 

'amazon-archives', 

'amazonwebservices',

'amzn',

'aws',

'aws-quickstart', 

'aws-samples',

'awsdocs', 

'awslabs', 

'blindsightcorp',

'blox',

'boto', 

'c9', 

'Carbonado',

'cloud9ide', 

'Goodreads',

'Justintv',

'Twitchdev',

'twitchscience',

'twitchtv',

'Zappos',

 

 

];

 

function doSearch() {

    // eg: https://github.com/search?utf8=%E2%9C%93&q=fpga+user%3Aaws+user%3Aawsdocs+user%3Aawslabs+user%3Aamzn+user%3Ablox&type=Repositories&ref=advsearch&l=&l=

    var search = document.forms["search"]["q"].value;

    var url = 'https://github.com/search?utf8=%E2%9C%93&q=' + search;

    for (var i = 0; i < accounts.length; i++) {

        url = url + '+user%3A' + accounts[i];

    }

    url = url + '&type=Repositories&ref=advsearch&l=&l=';

    window.open(url, '_blank');

    return false;

}

</script>
