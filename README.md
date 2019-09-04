# How-to-Add-Odd-And-Even-Class-to-WordPress-Posts



// add odd and even class to wordpress posts
function oddeven_post_class ( $classes ) {
    global $current_class;
    $classes[] = $current_class;
    $current_class = ( $current_class == 'odd' ) ? 'even' : 'odd';
    return $classes;
}
add_filter ( 'post_class' , 'oddeven_post_class' );
global $current_class;
$current_class = 'odd';
