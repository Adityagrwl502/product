<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Graza - Product</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.16/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100">
    <div class="container mx-auto">
        <div class="flex">
            <!-- Carousel -->
            <div class="w-2/3">
                <div class="swiper-container">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide">
                            <img src="https://www.graza.co/uploads/1080x675/Graza_GF01.jpg" alt="GF01">
                        </div>
                        <div class="swiper-slide">
                            <img src="https://www.graza.co/uploads/1080x675/Graza_GF02.jpg" alt="GF02">
                        </div>
                        <div class="swiper-slide">
                            <img src="https://www.graza.co/uploads/1080x675/Graza_GF03.jpg" alt="GF03">
                        </div>
                    </div>
                </div>
            </div>

            <!-- Right Section -->
            <div class="w-1/3 ml-8">
                <h1 class="text-3xl font-bold mb-4">Sizzle Drizzle Combo Pack</h1>

                <!-- Quantity Selector -->
                <div class="flex items-center mb-4">
                    <button class="bg-gray-200 text-gray-600 py-1 px-3 rounded-l">-</button>
                    <input type="text" value="1" class="border-t border-b border-r border-gray-300 text-center w-12">
                    <button class="bg-gray-200 text-gray-600 py-1 px-3 rounded-r">+</button>
                </div>

                <!-- Buttons -->
                <div class="flex justify-between mb-4">
                    <button class="bg-green-500 text-white py-2 px-6 rounded">Add to Cart</button>
                    <button class="bg-blue-500 text-white py-2 px-6 rounded">Buy Now</button>
                </div>

                <!-- Accordion -->
                <div class="accordion">
                    <button class="accordion-title bg-gray-200 py-2 px-4 rounded-lg mb-2">Description</button>
                    <div class="accordion-content bg-gray-100 p-4 rounded-lg">
                        <p>Discover the power of natural charcoal. The Sizzle Drizzle Combo Pack offers the ultimate charcoal blast for perfect flavor, aroma, and smokiness.
                        </p>
                    </div>

                    <button class="accordion-title bg-gray-200 py-2 px-4 rounded-lg mb-2">Harvest</button>
                    <div class="accordion-content bg-gray-100 p-4 rounded-lg">
                        <p>Harvest is the practice of cutting or picking and collecting a product from its place of origin. 
                        </p>
                    </div>

                    <button class="accordion-title bg-gray-200 py-2 px-4 rounded-lg mb-2">Use Case</button>
                    <div class="accordion-content bg-gray-100 p-4 rounded-lg">
                        <p>Sizzle Drizzle Combo Pack can be used to grill or bake, providing an excellent charcoal blast. 
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Initialize Swiper
        var swiper = new Swiper('.swiper-container', {
            slidesPerView: 1,
            spaceBetween: 10,
            loop: true,
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
        });

        // Accordion functionality
        const accordionTitles = document.querySelectorAll('.accordion-title');
        const accordionContents = document.querySelectorAll('.accordion-content');

        accordionTitles.forEach((title, index) => {
            title.addEventListener('click', () => {
                accordionContents[index].classList.toggle('hidden');
            });
        });
    </script>
</body>
</html>
