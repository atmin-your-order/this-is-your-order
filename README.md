<html>
<head>
    <title>Hubungi Kami di WhatsApp</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"></link>
    <style>
        @keyframes slideInFromRight {
            0% {
                transform: translateX(100%);
                opacity: 0;
            }
            100% {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .slide-in {
            animation: slideInFromRight 0.5s ease-out forwards;
        }
    </style>
    <script>
        function sendMessage(phoneNumber, message) {
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        function openLink(url) {
            window.open(url, '_blank');
        }

        function showOptions(option) {
            const options = {
                'KIA ASU ASLI': [
                    { text: 'I Love U', message: 'I Love U' },
                    { text: 'NAJISS BET ANJG', message: 'NAJISS BET ANJG' }
                ],
                'AKU SUKA MEGURU': [
                    { text: 'Aku Sangat Mencintaimu', message: 'Aku Sangat Mencintaimu' },
                    { text: 'Kamu Cantik Bagaikan Bintang', message: 'Kamu Cantik Bagaikan Bintang' }
                ],
                'NAU PEDHO AKUT': [
                    { text: 'LU PEDO ANJG', message: 'LU PEDO ANJG' },
                    { text: 'AKU SUKA KAMU NAU', message: 'AKU SUKA KAMU NAU' }
                ],
                'RIZKY GANTENG BANGET': [
                    { text: 'Kamu Emang Seganteng Itu', message: 'Kamu Emang Seganteng Itu' },
                    { text: 'Jelek Banget', link: 'https://youtu.be/xvFZjo5PgG0?si=ywdanbrPL7NxinIv' }
                ]
            };

            const container = document.getElementById('initial-options');
            container.innerHTML = '';

            const newContainer = document.getElementById('additional-options');
            newContainer.innerHTML = '';

            if (option === 'KIA ASU ASLI') {
                options[option].forEach(opt => {
                    const button = document.createElement('button');
                    button.className = 'bg-blue-500 text-white py-2 px-4 rounded mt-2 font-semibold slide-in';
                    button.innerText = opt.text;
                    button.onclick = () => sendMessage('+6282281786829', opt.message);
                    newContainer.appendChild(button);
                });
            } else if (option === 'AKU SUKA MEGURU') {
                options[option].forEach(opt => {
                    const button = document.createElement('button');
                    button.className = 'bg-blue-500 text-white py-2 px-4 rounded mt-2 font-semibold slide-in';
                    button.innerText = opt.text;
                    button.onclick = () => sendMessage('+6282221307257', opt.message);
                    newContainer.appendChild(button);
                });
            } else if (option === 'NAU PEDHO AKUT') {
                options[option].forEach(opt => {
                    const button = document.createElement('button');
                    button.className = 'bg-blue-500 text-white py-2 px-4 rounded mt-2 font-semibold slide-in';
                    button.innerText = opt.text;
                    button.onclick = () => sendMessage('+628896687486', opt.message);
                    newContainer.appendChild(button);
                });
            } else if (option === 'RIZKY GANTENG BANGET') {
                options[option].forEach(opt => {
                    const button = document.createElement('button');
                    button.className = 'bg-blue-500 text-white py-2 px-4 rounded mt-2 font-semibold slide-in';
                    button.innerText = opt.text;
                    if (opt.link) {
                        button.onclick = () => openLink(opt.link);
                    } else {
                        button.onclick = () => sendMessage('+6283133328750', opt.message);
                    }
                    newContainer.appendChild(button);
                });
            } else {
                options[option].forEach(opt => {
                    const button = document.createElement('button');
                    button.className = 'bg-blue-500 text-white py-2 px-4 rounded mt-2 font-semibold slide-in';
                    button.innerText = opt;
                    button.onclick = () => sendMessage('YOUR_PHONE_NUMBER', opt);
                    newContainer.appendChild(button);
                });
            }

            document.getElementById('back-button').classList.remove('hidden');
            document.getElementById('initial-options').style.backgroundImage = "url('https://oyster.ignimgs.com/mediawiki/apis.ign.com/genshin-impact/f/f5/Hu_Tao_Birthday_Banner.png')";
            documen
