Active-Styles-On-Scroll
=======================

jQuery to add active css style once you scroll to specified anchor. Repeat below code for each menu link.
Commits to simiplfy this is welcome.

/* Active styles on scroll */
jQuery(window).bind('scroll',function() {
    var vPos = jQuery(window).scrollTop(); //The current scroll bar position
    var totalH = jQuery('#Home').offset().top; // Distance content from top
    var finalSize = totalH - vPos; // Get the difference of the distances

    console.log(finalSize);

    if (finalSize <= 50) {
        jQuery('.navbar').fadeIn(600);
        jQuery('#link01').css('border-bottom', '4px solid #ff8336'); /* ID of link clicked */
        jQuery('#link02, #link03, #link04').css('border-bottom', 'none'); /* list IDs of all other links */
    } else {
        jQuery('#link01').css('border-bottom', 'none'); /* ID of link clicked */
    }
});
