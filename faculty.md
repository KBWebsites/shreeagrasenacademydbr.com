---
title: Faculty
layout: default
---
<noscript>Please enable JavaScript to view the page.</noscript>
<div id="faculty" class="media">
<script>
function getName(un) {
    jQuery.getJSON('http://graph.facebook.com/' + un, function (d) {
        jQuery('#' + un.replace(/\./g, '-')).text(d.name);
    });
}

jQuery(document).ready(function () {
    var usernames = [
    "100000150790513", //gunjan.saharia
    //"shraboni.chakraborty.37",
    "100002613158299", //sandeep.poddar.52
    "100004932099854", // nandini.boseduttaroy
    "100002117854904", // soma.das.5076
    "100001689921698", // sadia.shah.940098
    "100006055026248", // jaya.chakraborty.167
    "100003544424620", // bineeta.ghose
    "100000032071819", // aparna.goenka.9
    "100006140702995", // paromitadey211
    "100002476836310", // paramita.bose.336
    "100001919700978", // sansita.dowarah
    "100004861985165", // kanchan.patel.1800
    "100005028000210"];
    for (var username = 0; username < usernames.length; username++) {
        var un = usernames[username];
        jQuery('#faculty').append('<a href="https://www.facebook.com/' + un + '"><img alt="" src="https://graph.facebook.com/' + un + '/picture?width=176&amp;height=176" width="176" height="176" /><h3 id="' + un.replace(/\./g, '-') + '"></h3></a>');
        getName(un);
    }
});
</script>
</div>