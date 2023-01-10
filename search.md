---
layout: default
permalink: search
title: search
baseurl: mysearch
---

{% capture initSearch %}

<form id="search-form" action="">
    <label class="label" for="search">BUSQUEDA (acepta expresión regular):</label>
    <br/>
    <input 
        class="input" 
        id="search" 
        type="text" 
        name="search" 
        autofocus 
        placeholder="e. g. Promise" 
        autocomplete="off">

    <ul class="list list--results" id="list">
    </ul>
</form>

<script type="test/javascript" src="{{site.baseurl}}/assets/src/search.js"></script>

<script type="test/javascript">

    const search = new JekyllSearch{
        '{{site.baseurl}}/assets/src/search.json',
        '#search'
        '#list'
        '{{site.baseurl}}
    };
    search.init();

</script>


{% endcapture %}

{{ initSearch | lstrip }}
