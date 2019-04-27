<template>
    <div id="first-scroll" class="wrapper first-scroll">
        <div class="background-first-scroll">
                <div class="background-first-scroll__sights background-style"></div>
                <div :style="{ margin: `0 0 -${scrolled / 300}%  -${scrolled / 80}%` }"  class="background-first-scroll__field-left background-style"></div>
                <div :style="{ margin: `0 -${scrolled / 300}% -${scrolled / 80}% 0` }" class="background-first-scroll__field-right background-style"></div>
                <div :style="{ margin: `${scrolled / 20}px`, transform: `scale(${1 + scrolled / 5000 })` }" class="background-first-scroll__man background-style"></div>
                <div :style="{ margin: `0 -${scrolled / 200}% -${scrolled / 70}% 0`, transform: `scale(${1 - scrolled / 5000 })` }" class="background-first-scroll__bush background-style"></div>
        </div>
        <div class="layout">
            <div class="header">
                <svg class="logo" width="251" height="59" viewBox="0 0 251 59" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M8.93438 35.7004C8.93438 35.7004 15.0658 43.2334 14.8907 48.6641C14.7155 53.9196 8.58401 41.3063 8.58401 41.3063L8.93438 35.7004Z" fill="url(#paint0_linear)"/>
                    <path d="M42.0443 29.9194V9.42279H23.6499L8.40888 14.5031L5.08038 29.9194V37.4523C5.08038 37.4523 4.55482 46.9123 7.18259 49.7152C9.98554 52.6933 16.6426 59 23.4747 59C30.3069 59 37.1391 52.6933 39.7669 49.7152C42.5698 46.7371 41.8691 37.4523 41.8691 37.4523L42.0443 29.9194Z" fill="url(#paint1_linear)"/>
                    <path d="M21.0221 32.5471V41.6567C21.0221 41.6567 21.0221 44.1093 23.6499 44.1093C26.2777 44.1093 26.2777 41.6567 26.2777 41.6567V32.5471H21.0221Z" fill="url(#paint2_linear)"/>
                    <path d="M21.7229 34.8245V41.4815C21.7229 41.4815 21.7229 43.2334 23.6499 43.2334C25.5769 43.2334 25.5769 41.4815 25.5769 41.4815V34.8245H21.7229Z" fill="url(#paint3_linear)"/>
                    <path d="M21.7229 34.299V40.956C21.7229 40.956 21.7229 42.7079 23.6499 42.7079C25.5769 42.7079 25.5769 40.956 25.5769 40.956V34.299H21.7229Z" fill="url(#paint4_linear)"/>
                    <path d="M22.2484 35.7004V40.7808C22.2484 40.7808 22.2484 42.1823 23.6499 42.1823C25.0514 42.1823 25.0514 40.7808 25.0514 40.7808V35.7004H22.2484Z" fill="url(#paint5_linear)"/>
                    <path d="M31.1828 31.3208C33.8106 31.3208 35.9128 31.3208 36.7887 33.423C36.7887 33.2479 36.7887 32.8975 36.7887 32.7223C36.7887 29.569 34.161 26.9412 31.0076 26.9412C27.8543 26.9412 25.2265 29.569 25.2265 32.7223C25.2265 32.8975 25.2265 33.2479 25.2265 33.423C26.2777 31.3208 28.5551 31.3208 31.1828 31.3208Z" fill="url(#paint6_linear)"/>
                    <path d="M15.7666 31.3208C13.1388 31.3208 11.0366 31.3208 10.1607 33.423C10.1607 33.2479 10.1607 32.8975 10.1607 32.7223C10.1607 29.569 12.7884 26.9412 15.9418 26.9412C19.0951 26.9412 21.7228 29.569 21.7228 32.7223C21.7228 32.8975 21.7228 33.2479 21.7228 33.423C20.4966 31.3208 18.2192 31.3208 15.7666 31.3208Z" fill="url(#paint7_linear)"/>
                    <path d="M31.7084 32.7223C32.9347 32.7223 33.9858 33.4231 34.5113 34.6494C34.5113 34.4742 34.5113 34.4742 34.5113 34.299C34.5113 32.7223 33.285 31.496 31.7084 31.496C30.1317 31.496 28.9054 32.7223 28.9054 34.299C28.9054 34.4742 28.9054 34.4742 28.9054 34.6494C29.2558 33.5982 30.3069 32.7223 31.7084 32.7223Z" fill="#332314"/>
                    <path d="M35.212 29.2187C35.3872 29.2187 35.3872 29.0435 35.212 29.2187C34.5113 27.9924 32.0587 25.5398 28.3798 27.2916C27.5039 27.8172 27.8543 28.8683 28.555 28.8683C29.0806 28.5179 31.8835 27.4668 35.212 29.2187Z" fill="url(#paint8_linear)"/>
                    <path d="M15.2411 32.7223C14.0148 32.7223 12.9637 33.4231 12.4381 34.6494C12.4381 34.4742 12.4381 34.4742 12.4381 34.299C12.4381 32.7223 13.6644 31.496 15.2411 31.496C16.8177 31.496 18.044 32.7223 18.044 34.299C18.044 34.4742 18.044 34.4742 18.044 34.6494C17.6936 33.5982 16.4674 32.7223 15.2411 32.7223Z" fill="url(#paint9_linear)"/>
                    <path d="M11.7374 29.2187C11.5622 29.2187 11.387 29.0435 11.7374 29.2187C12.4381 27.9924 14.8907 25.5398 18.5695 27.2916C19.4455 27.8172 19.0951 28.8683 18.3944 28.8683C17.6936 28.5179 15.0659 27.4668 11.7374 29.2187Z" fill="url(#paint10_linear)"/>
                    <path d="M5.25551 32.8975C5.25551 32.8975 0.700712 24.1383 3.85403 17.1309C5.95624 13.4521 6.65698 12.9265 6.65698 12.9265C6.65698 12.9265 10.511 -3.8912 32.4091 0.838775C24.3506 3.29136 21.898 5.91912 21.898 5.91912C21.898 5.91912 26.628 2.41543 33.8106 3.11617C36.7887 3.46654 38.1902 4.69283 43.4457 6.61986C40.4676 7.3206 38.7157 8.3717 38.7157 8.3717C38.7157 8.3717 40.4676 8.02133 43.7961 10.1235C47.2998 12.2258 46.9494 13.452 50.2779 14.1528C47.8253 16.9557 44.3216 17.4813 44.3216 17.4813C44.3216 17.4813 43.6209 31.1457 41.869 33.7734C41.1683 33.2479 41.8691 27.8172 39.0661 25.0142C37.1391 22.912 41.1683 19.5835 39.2413 19.2331C38.7157 19.058 27.6791 23.0872 8.93438 18.0068C8.75919 18.8828 9.98549 20.4594 7.53291 23.2624C4.72995 27.1164 5.25551 32.8975 5.25551 32.8975Z" fill="url(#paint11_linear)"/>
                    <path d="M9.63513 18.182C9.63513 18.182 12.2629 10.9994 23.4747 12.9265C34.6865 14.8535 45.8983 17.8316 50.4531 14.1528C49.2268 17.1309 30.3069 24.6638 9.63513 18.182Z" fill="url(#paint12_linear)"/>
                    <path d="M43.6209 6.4447C43.6209 6.4447 39.7668 7.4958 38.8909 8.19654C37.4894 8.7221 34.3361 10.4739 34.3361 10.4739L28.3799 12.7513L20.6717 7.32062C20.6717 7.32062 25.5769 2.94101 32.4091 2.94101C37.3143 2.94101 38.3654 4.86804 43.6209 6.4447Z" fill="url(#paint13_linear)"/>
                    <path d="M18.7447 47.4378C18.5695 47.4378 18.3944 47.613 18.3944 47.7882C18.9199 50.2408 21.0221 51.9926 23.4747 51.9926C25.9273 51.9926 28.0295 50.2408 28.5551 47.7882C28.5551 47.613 28.3799 47.4378 28.2047 47.4378H18.7447Z" fill="#742E2B"/>
                    <path d="M21.1973 51.2919C21.1973 51.2919 21.5477 49.1897 24.1755 49.0145C26.8032 49.0145 27.504 50.2408 27.504 50.2408C27.504 50.2408 24.8762 53.2189 21.1973 51.2919Z" fill="#B95878"/>
                    <path d="M20.4966 7.32059C22.2485 5.91912 25.7521 3.64172 30.3069 3.11617C28.2047 2.41543 25.9273 1.88988 23.2996 1.71469C1.22632 2.41543 0.350403 27.2916 0.350403 27.2916C0.350403 27.2916 0.350403 27.2916 2.27743 27.2916C2.80299 17.8317 11.387 8.89725 20.4966 7.32059Z" fill="url(#paint14_linear)"/>
                    <path d="M38.891 8.37167C38.891 8.37167 34.161 10.6491 34.161 10.8243C39.7669 14.5031 43.9713 20.6346 44.3217 27.4668C46.4239 27.4668 46.4239 27.4668 46.4239 27.4668C46.4239 27.4668 46.0735 15.9046 38.891 8.37167Z" fill="url(#paint15_linear)"/>
                    <path d="M45.8983 39.9049H43.7961V27.642H45.8983C46.2487 27.642 46.4239 27.8172 46.4239 28.1675V39.3793C46.2487 39.7297 46.0735 39.9049 45.8983 39.9049Z" fill="#232B30"/>
                    <path d="M45.8983 40.4304H44.8472C44.4968 40.4304 44.1465 40.0801 44.1465 39.7297V27.8172C44.1465 27.4668 44.4968 27.1164 44.8472 27.1164H45.8983C46.2487 27.1164 46.599 27.4668 46.599 27.8172V39.5545C46.599 40.0801 46.2487 40.4304 45.8983 40.4304Z" fill="url(#paint16_linear)"/>
                    <path d="M43.6209 41.1312H42.5698C41.8691 41.1312 41.3435 40.6056 41.3435 39.9049V27.8172C41.3435 27.1164 41.8691 26.5909 42.5698 26.5909H43.6209C43.7961 26.5909 43.7961 26.7661 43.7961 26.7661V40.7808C43.7961 40.956 43.6209 41.1312 43.6209 41.1312Z" fill="url(#paint17_linear)"/>
                    <path d="M0.875958 40.0801H2.97817V27.8172H0.875958C0.525589 27.8172 0.350403 27.9924 0.350403 28.3427V39.5545C0.350403 39.9049 0.525589 40.0801 0.875958 40.0801Z" fill="#232B30"/>
                    <path d="M0.700737 40.6057H1.75184C2.10221 40.6057 2.45258 40.2553 2.45258 39.9049V28.1676C2.45258 27.8172 2.10221 27.4668 1.75184 27.4668H0.700737C0.350368 27.4668 0 27.8172 0 28.1676V39.9049C0 40.2553 0.350368 40.6057 0.700737 40.6057Z" fill="url(#paint18_linear)"/>
                    <path d="M3.1533 41.3064H4.2044C4.90514 41.3064 5.43069 40.7808 5.43069 40.0801V27.9923C5.43069 27.2916 4.90514 26.7661 4.2044 26.7661H3.1533C2.97811 26.7661 2.97811 26.9412 2.97811 26.9412V40.956C2.80293 41.1312 2.97811 41.3064 3.1533 41.3064Z" fill="url(#paint19_linear)"/>
                    <path d="M71.1249 36.7516V40.2553C71.1249 42.0071 69.8986 43.0582 67.9716 43.0582C65.8693 43.0582 64.8182 41.8319 64.8182 40.2553V25.5398C64.8182 23.7879 66.0445 22.7368 67.9716 22.7368H73.7526C79.5337 22.7368 82.6871 25.8901 82.6871 29.7442C82.6871 33.5983 79.5337 36.7516 73.7526 36.7516C73.7526 36.7516 71.1249 36.7516 71.1249 36.7516ZM73.7526 31.496C75.1541 31.496 76.03 30.6201 76.03 29.569C76.03 28.5179 75.1541 27.642 73.7526 27.642H71.1249V31.3208L73.7526 31.496Z" fill="white"/>
                    <path d="M103.884 34.6494C103.884 39.5545 100.205 43.2334 94.2492 43.2334C88.2929 43.2334 84.6141 39.5545 84.6141 34.6494V30.6201C84.6141 25.715 88.2929 22.0361 94.2492 22.0361C100.205 22.0361 103.884 25.715 103.884 30.6201V34.6494ZM97.4025 30.6201C97.4025 28.3427 96.0011 26.9413 94.2492 26.9413C92.4974 26.9413 91.0959 28.3427 91.0959 30.6201V34.6494C91.0959 36.9268 92.4974 38.3283 94.2492 38.3283C96.0011 38.3283 97.4025 36.9268 97.4025 34.6494V30.6201Z" fill="white"/>
                    <path d="M113.169 40.0801C113.169 41.8319 111.943 42.883 110.016 42.883C107.914 42.883 106.862 41.6567 106.862 40.0801V25.0142C106.862 23.2624 108.089 22.2113 110.016 22.2113C112.118 22.2113 113.169 23.4376 113.169 25.0142V40.0801Z" fill="white"/>
                    <path d="M123.33 33.5983V40.2553C123.33 42.0071 122.104 43.0582 120.177 43.0582C118.074 43.0582 117.023 41.8319 117.023 40.2553V25.1894C117.023 23.4376 118.249 22.3865 120.177 22.3865C121.928 22.3865 122.979 23.4376 124.206 25.1894L129.111 31.8464H129.461V25.1894C129.461 23.4376 130.688 22.3865 132.615 22.3865C134.717 22.3865 135.768 23.6128 135.768 25.1894V40.2553C135.768 42.0071 134.542 43.0582 132.615 43.0582C130.863 43.0582 129.812 42.0071 128.585 40.2553L123.68 33.5983H123.33V33.5983Z" fill="white"/>
                    <path d="M140.848 28.3427C138.746 28.3427 137.695 27.1164 137.695 25.5398C137.695 23.7879 138.921 22.7368 140.848 22.7368H153.637C155.739 22.7368 156.79 23.9631 156.79 25.5398C156.79 27.2916 155.564 28.3427 153.637 28.3427H150.308V40.2553C150.308 42.0071 149.082 43.0582 147.155 43.0582C145.053 43.0582 144.002 41.8319 144.002 40.2553V28.3427H140.848Z" fill="white"/>
                    <path d="M157.841 30.6201C157.841 25.715 161.52 22.0361 167.476 22.0361C172.557 22.0361 175.36 24.8391 175.36 26.9413C175.36 28.5179 174.309 29.569 172.206 29.569C169.929 29.569 169.579 27.4668 167.476 27.4668C165.549 27.4668 164.323 28.6931 164.323 30.6201V34.6494C164.323 36.5764 165.549 37.8027 167.476 37.8027C169.053 37.8027 170.279 36.9268 170.279 36.9268V35.7005H169.403C167.651 35.7005 166.6 34.4742 166.6 33.0727C166.6 31.6712 167.827 30.445 169.403 30.445H173.433C175.184 30.445 176.06 31.3209 176.06 33.0727V38.3283C176.06 40.4305 172.907 43.2334 167.476 43.2334C161.52 43.2334 157.841 39.5545 157.841 34.6494V30.6201V30.6201Z" fill="white"/>
                    <path d="M179.038 34.9998V25.1894C179.038 23.4376 180.265 22.3865 182.192 22.3865C184.294 22.3865 185.345 23.6128 185.345 25.1894V34.9998C185.345 37.102 186.571 38.1531 188.148 38.1531C189.9 38.1531 190.951 36.9268 190.951 34.9998V25.1894C190.951 23.4376 192.177 22.3865 194.104 22.3865C196.207 22.3865 197.258 23.6128 197.258 25.1894V34.9998C197.258 39.9049 193.754 43.4086 187.973 43.4086C182.542 43.4086 179.038 39.9049 179.038 34.9998Z" fill="white"/>
                    <path d="M207.769 40.0801C207.769 41.8319 206.542 42.883 204.615 42.883C202.513 42.883 201.462 41.6567 201.462 40.0801V25.0142C201.462 23.2624 202.688 22.2113 204.615 22.2113C206.718 22.2113 207.769 23.4376 207.769 25.0142V40.0801Z" fill="white"/>
                    <path d="M229.667 34.1238C229.667 39.029 225.988 42.7078 219.681 42.7078H214.601C212.499 42.7078 211.448 41.4815 211.448 39.9049V25.5398C211.448 23.7879 212.674 22.7368 214.601 22.7368H219.681C225.813 22.7368 229.667 26.4157 229.667 31.3208V34.1238ZM217.754 27.8172V37.6275H219.681C221.783 37.6275 223.185 36.226 223.185 34.1238V31.3208C223.185 29.2186 221.783 27.8172 219.681 27.8172H217.754Z" fill="white"/>
                    <path d="M239.127 28.3427V30.0946H244.557C246.309 30.0946 247.36 31.3209 247.36 32.7223C247.36 34.1238 246.134 35.3501 244.557 35.3501H239.127V37.1019H247.185C249.287 37.1019 250.339 38.3282 250.339 39.9049C250.339 41.4815 249.112 42.7078 247.185 42.7078H235.973C233.871 42.7078 232.82 41.4815 232.82 39.9049V25.5398C232.82 23.7879 234.046 22.7368 235.973 22.7368H247.01C249.112 22.7368 250.163 23.9631 250.163 25.5398C250.163 27.2916 248.937 28.3427 247.01 28.3427H239.127Z" fill="white"/>
                    <defs>
                        <linearGradient id="paint0_linear" x1="16.8081" y1="45.8548" x2="6.49147" y2="39.8986" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F2D1C9" stop-opacity="0"/>
                            <stop offset="0.518" stop-color="#ECAD9F" stop-opacity="0.518"/>
                            <stop offset="1" stop-color="#E78F7D"/>
                        </linearGradient>
                        <linearGradient id="paint1_linear" x1="7.62896" y1="15.5252" x2="43.5023" y2="45.6266" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F2D1C9"/>
                            <stop offset="0.2221" stop-color="#F0C7BE"/>
                            <stop offset="0.6123" stop-color="#ECAEA0"/>
                            <stop offset="1" stop-color="#E78F7D"/>
                        </linearGradient>
                        <linearGradient id="paint2_linear" x1="22.3011" y1="32.2045" x2="25.3877" y2="43.7237" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F2D1C9" stop-opacity="0.1"/>
                            <stop offset="0.3144" stop-color="#EDB3A8" stop-opacity="0.3201"/>
                            <stop offset="1" stop-color="#E26955" stop-opacity="0.8"/>
                        </linearGradient>
                        <linearGradient id="paint3_linear" x1="22.6725" y1="34.5991" x2="24.9529" y2="43.1097" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F2D1C9" stop-opacity="0.1"/>
                            <stop offset="0.6303" stop-color="#D7776A" stop-opacity="0.6673"/>
                            <stop offset="1" stop-color="#C64031"/>
                        </linearGradient>
                        <linearGradient id="paint4_linear" x1="22.6466" y1="33.9772" x2="24.927" y2="42.4878" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#F2D1C9" stop-opacity="0.1"/>
                            <stop offset="0.3144" stop-color="#EDB3A8" stop-opacity="0.3201"/>
                            <stop offset="1" stop-color="#E26955" stop-opacity="0.8"/>
                        </linearGradient>
                        <linearGradient id="paint5_linear" x1="23.2461" y1="42.1036" x2="23.9227" y2="35.6668" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00189568" stop-color="#F2D1C9" stop-opacity="0.8"/>
                            <stop offset="0.0564102" stop-color="#EFBCB2" stop-opacity="0.7563"/>
                            <stop offset="0.1407" stop-color="#EBA395" stop-opacity="0.6888"/>
                            <stop offset="0.2352" stop-color="#E88D7E" stop-opacity="0.613"/>
                            <stop offset="0.3426" stop-color="#E57D6B" stop-opacity="0.5269"/>
                            <stop offset="0.4701" stop-color="#E3725F" stop-opacity="0.4247"/>
                            <stop offset="0.6378" stop-color="#E26B57" stop-opacity="0.2903"/>
                            <stop offset="1" stop-color="#E26955" stop-opacity="0"/>
                        </linearGradient>
                        <linearGradient id="paint6_linear" x1="31.0185" y1="33.6734" x2="30.9036" y2="27.0917" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#EDB4AF" stop-opacity="0"/>
                            <stop offset="0.2886" stop-color="#E8AAA3" stop-opacity="0.2889"/>
                            <stop offset="0.8042" stop-color="#DC9084" stop-opacity="0.805"/>
                            <stop offset="0.999" stop-color="#D68577"/>
                        </linearGradient>
                        <linearGradient id="paint7_linear" x1="15.9308" y1="33.6752" x2="16.0458" y2="27.0937" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#EDB4AF" stop-opacity="0"/>
                            <stop offset="0.2886" stop-color="#E8AAA3" stop-opacity="0.2889"/>
                            <stop offset="0.8042" stop-color="#DC9084" stop-opacity="0.805"/>
                            <stop offset="0.999" stop-color="#D68577"/>
                        </linearGradient>
                        <linearGradient id="paint8_linear" x1="27.7627" y1="27.95" x2="35.3681" y2="27.95" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#512F17"/>
                            <stop offset="0.6316" stop-color="#3F2815"/>
                            <stop offset="1" stop-color="#332314"/>
                        </linearGradient>
                        <linearGradient id="paint9_linear" x1="12.3968" y1="33.0727" x2="18.1521" y2="33.0727" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#512F17"/>
                            <stop offset="0.6313" stop-color="#3F2815"/>
                            <stop offset="1" stop-color="#332314"/>
                        </linearGradient>
                        <linearGradient id="paint10_linear" x1="11.5273" y1="27.95" x2="19.1328" y2="27.95" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#512F17"/>
                            <stop offset="0.6313" stop-color="#3F2815"/>
                            <stop offset="1" stop-color="#332314"/>
                        </linearGradient>
                        <linearGradient id="paint11_linear" x1="4.66181" y1="13.335" x2="48.0107" y2="24.143" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#834F38"/>
                            <stop offset="0.3838" stop-color="#814D37"/>
                            <stop offset="0.5941" stop-color="#794732"/>
                            <stop offset="0.7624" stop-color="#6B3D29"/>
                            <stop offset="0.9077" stop-color="#582E1D"/>
                            <stop offset="0.999" stop-color="#472213"/>
                        </linearGradient>
                        <linearGradient id="paint12_linear" x1="29.6484" y1="11.6438" x2="30.4339" y2="20.623" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#512F17" stop-opacity="0"/>
                            <stop offset="0.6257" stop-color="#4F2D16" stop-opacity="0.6253"/>
                            <stop offset="0.9265" stop-color="#4A2514" stop-opacity="0.9264"/>
                            <stop offset="1" stop-color="#472213"/>
                        </linearGradient>
                        <linearGradient id="paint13_linear" x1="22.3856" y1="3.5363" x2="41.2126" y2="11.9187" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#512F17" stop-opacity="0"/>
                            <stop offset="0.6723" stop-color="#502D16" stop-opacity="0.672"/>
                            <stop offset="0.9214" stop-color="#4A2614" stop-opacity="0.9213"/>
                            <stop offset="1" stop-color="#472213"/>
                        </linearGradient>
                        <linearGradient id="paint14_linear" x1="20.0667" y1="-0.463705" x2="9.40218" y2="30.508" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#7C939E"/>
                            <stop offset="0.2505" stop-color="#778D97"/>
                            <stop offset="0.6069" stop-color="#6A7B84"/>
                            <stop offset="0.999" stop-color="#566168"/>
                        </linearGradient>
                        <linearGradient id="paint15_linear" x1="43.4778" y1="9.89385" x2="38.2182" y2="25.1684" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#7C939E"/>
                            <stop offset="0.2505" stop-color="#778D97"/>
                            <stop offset="0.6069" stop-color="#6A7B84"/>
                            <stop offset="0.999" stop-color="#566168"/>
                        </linearGradient>
                        <linearGradient id="paint16_linear" x1="41.6695" y1="30.5543" x2="49.1974" y2="37.0979" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#4D5E68"/>
                            <stop offset="0.2826" stop-color="#425058"/>
                            <stop offset="0.7013" stop-color="#364046"/>
                            <stop offset="1" stop-color="#323A3F"/>
                        </linearGradient>
                        <linearGradient id="paint17_linear" x1="38.7611" y1="30.2696" x2="46.9289" y2="37.3698" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#7C939E"/>
                            <stop offset="0.2505" stop-color="#778D97"/>
                            <stop offset="0.6069" stop-color="#6A7B84"/>
                            <stop offset="0.999" stop-color="#566168"/>
                        </linearGradient>
                        <linearGradient id="paint18_linear" x1="-2.52511" y1="30.7752" x2="4.99784" y2="37.315" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#4D5E68"/>
                            <stop offset="0.2826" stop-color="#425058"/>
                            <stop offset="0.7013" stop-color="#364046"/>
                            <stop offset="1" stop-color="#323A3F"/>
                        </linearGradient>
                        <linearGradient id="paint19_linear" x1="-0.23249" y1="30.474" x2="7.93022" y2="37.5699" gradientUnits="userSpaceOnUse">
                            <stop offset="0.00094784" stop-color="#7C939E"/>
                            <stop offset="0.2505" stop-color="#778D97"/>
                            <stop offset="0.6069" stop-color="#6A7B84"/>
                            <stop offset="0.999" stop-color="#566168"/>
                        </linearGradient>
                    </defs>
                </svg>
                <button class="header__contact" @click="showModal">Contact us</button>
            </div>
            <div class="heading">
                <h1 class="heading__title title">An easy and fun way to explore cities</h1>
                <h3 class="heading__descr descr">Listen to the best guides directly with your phone while travelling with your frienga</h3>
                <div class="heading__buttons">
                    <DownloadButtons />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
import DownloadButtons from './DownloadButtons'
import ContactPopup from './ContactPopup/ContactPopup.vue'

export default {
  name: 'FirstScroll',
  data() {
    return {
      scrolled: 0,
    }
  },
  components: {
    DownloadButtons,
    ContactPopup
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrolled = Math.floor(window.pageYOffset)
    },
    showModal() {
      this.$modal.show(ContactPopup)
    }
  },
  watch: {
    'scrolled'(value) {
      if (value > document.getElementById('first-scroll').clientHeight) {
        this.scrolled = 0
        return window.removeEventListener('scroll', this.handleScroll)
      }
      return window.addEventListener('scroll', this.handleScroll)
    }
  },
}
</script>

<style scoped lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Questrial');
    .first-scroll {
        position: relative;
        overflow: hidden;
        background: #9b70fa;
        background: -moz-linear-gradient(top, #9b70fa 0%, #590ff2 100%);
        background: -webkit-linear-gradient(top, #9b70fa 0%,#590ff2 100%);
        background: linear-gradient(to bottom, #9b70fa 0%,#590ff2 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#9b70fa', endColorstr='#590ff2',GradientType=0 );
        display: block;
        height: 920px;
        width: 100%;
        padding: 0 20px;
        box-sizing: border-box;
    }

    .header {
        max-width: 1170px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 10px 0;
        &__logo {
            width: 250px;
            margin: 0 10px;
        }
        &__contact {
            border: 2px solid;
            background-color: transparent;
            padding: 10px 30px;
            color: #fff;
            font-size: 18px;
            outline: none;
            cursor: pointer;
            transition: .3s;
            margin: 0 10px;
            &:hover {
                transition: .3s;
                background-color: rgba(255, 255, 255, 0.16);
            }
        }
    }
    .heading {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        color: #fff;
        padding: 40px 0 0 0;
        font-family: "Questrial", sans-serif;
    }
    .background-style {
        position: absolute;
        background-repeat: no-repeat;
    }
    .background-first-scroll {
        max-width: 1170px;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: 1;
        right: 0;
        margin: auto;
        &__sights {
            background-image: url('../assets/img/sights.png');
            height: 50%;
            width: 100%;
            max-width: 1170px;
            background-repeat: no-repeat;
            background-size: contain;
            background-position: left;
            position: absolute;
            bottom: 67px;
            left: 0;
            right: 0;
            margin: auto;
        }
        &__field-left {
            background-image: url('../assets/img/field-left.png');
            background-size: contain;
            height: 315px;
            width: 1600px;
            bottom: 0;
            left: -800px;
        }
        &__field-right {
            background-image: url('../assets/img/field-right.png');
            height: 300px;
            width: 13005px;
            background-position: bottom right;
            background-size: contain;
            bottom: 0;
            right: -600px;
        }
        &__bush {
            background-image: url('../assets/img/bush.png');
            background-position: bottom right;
            background-size: contain;
            height: 280px;
            width: 1300px;
            right: -600px;
            bottom: 0;
        }
        &__man {
            background-image: url('../assets/img/man.png');
            background-size: contain;
            width: 350px;
            height: 480px;
            bottom: -60px;
            left: 20px;
        }
    }
    .animate {
        transition-delay: .1s;
        transition-duration: .25s;
        transition-timing-function: ease-in;
    }

    .slide-up {
        transform: translateY(0);
    }

    .slide-up.animate-active {
        transform: translateY(-100px);
    }
    @media (max-width: 768px), (max-height: 420px){
        .first-scroll {
            padding: 0 10px;
            box-sizing: border-box;
        }
        .logo {
            width: 175px;
        }
        .header__contact {
            font-size: 14px;
            margin: 0;
        }
        .title {
            font-size: 32px;
            line-height: 35px;
        }
        .descr {
            font-size: 14px;
            line-height: 16px;
        }
        .first-scroll {
            height: 650px;
        }
        .background-first-scroll {
             &__man {
                 background-size: contain;
                 width: 224px;
                 height: 320px;
                 bottom: -44px;
                 z-index: 20;
                 left: 20px;
             }
             &__bush {
                 background-position: bottom right;
                 background-size: contain;
                 height: 196px;
                 width: 600px;
                 right: -300px;
                 bottom: 0;
             }
             &__field-left {
                 background-size: cover;
                 height: 200px;
                 width: 600px;
                 bottom: 0;
                 left: auto;
                 right: -50px;
             }
             &__field-right {
                 height: 200px;
                 width: 600px;
                 background-position: bottom right;
                 background-size: cover;
                 bottom: 0;
                 right: auto;
                 left: -34px;
             }
             &__sights {
                 bottom: 35px;
             }
         }
    }
    @media (max-height: 420px) {
        .layout {
            width: 80%;
            max-width: 320px;
        }
        .background-first-scroll__field-left {
            left: 188px;
        }
    }
    @media (max-width: 500px) {
        .background-first-scroll {
            &__man {
                background-size: contain;
                width: 224px;
                height: 320px;
                bottom: -44px;
                z-index: 20;
                left: 20px;
            }
            &__bush {
                background-position: bottom right;
                background-size: contain;
                height: 196px;
                width: 600px;
                right: -300px;
                bottom: 0;
            }
            &__field-left {
                background-size: cover;
                height: 200px;
                width: 600px;
                bottom: 0;
                left: 0;
            }
            &__field-right {
                height: 200px;
                width: 600px;
                background-position: bottom right;
                background-size: cover;
                bottom: 0;
                right: 0;
            }
            &__sights {
                bottom: 35px;
            }
        }
    }
    @media (max-width: 320px) {
        .logo {
            width: 140px;
        }
        .header__contact {
            font-size: 12px;
        }
    }
</style>
