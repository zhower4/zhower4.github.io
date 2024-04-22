// JavaScript for menu functionality
document.addEventListener("DOMContentLoaded", function() {
    const navLinks = document.querySelectorAll("nav ul li a");

    navLinks.forEach(link => {
        link.addEventListener("click", function(event) {
            // Prevent default link behavior
            event.preventDefault();

            // Get target section ID from href attribute
            const targetId = link.getAttribute("href").substring(1);

            // Scroll to the target section
            document.getElementById(targetId).scrollIntoView({
                behavior: "smooth"
            });
        });
    });
});
