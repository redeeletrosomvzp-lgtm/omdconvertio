<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OMD Convertio - Magic Video Alchemist</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <script src="components/navbar.js"></script>
    <script src="components/footer.js"></script>
</head>
<body class="bg-gray-100 min-h-screen flex flex-col">
    <custom-navbar></custom-navbar>

    <main class="flex-grow container mx-auto px-4 py-12">
        <div class="max-w-4xl mx-auto bg-white rounded-xl shadow-md overflow-hidden p-8">
            <div class="text-center mb-10">
                <h1 class="text-4xl font-bold text-indigo-700 mb-4">OMD Convertio</h1>
                <p class="text-xl text-gray-600">Your magical video converter to MP4</p>
                <div class="mt-4">
                    <i data-feather="film" class="w-16 h-16 text-indigo-500 mx-auto"></i>
                </div>
            </div>

            <div class="space-y-8">
                <!-- Upload Section -->
                <div class="border-2 border-dashed border-gray-300 rounded-lg p-8 text-center hover:border-indigo-400 transition-colors duration-300" id="dropZone">
                    <i data-feather="upload" class="w-12 h-12 text-gray-400 mx-auto mb-4"></i>
                    <h3 class="text-lg font-medium text-gray-700 mb-2">Drag & drop your video file here</h3>
                    <p class="text-gray-500 mb-4">or</p>
                    <input type="file" id="fileInput" class="hidden" accept="video/*">
                    <button id="selectFileBtn" class="px-6 py-3 bg-indigo-600 text-white rounded-lg font-medium hover:bg-indigo-700 transition-colors duration-300">
                        Select File
                    </button>
                    <p class="text-xs text-gray-400 mt-4">Supports AVI, MKV, MOV, WMV, FLV, and more</p>
                </div>

                <!-- Conversion Options -->
                <div class="bg-gray-50 rounded-lg p-6">
                    <h3 class="text-lg font-medium text-gray-800 mb-4">Conversion Settings</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Output Format</label>
                            <select class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500">
                                <option selected>MP4 (Recommended)</option>
                                <option>MP4 (High Quality)</option>
                                <option>MP4 (Smaller Size)</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Quality</label>
                            <select class="w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500">
                                <option selected>Auto (Recommended)</option>
                                <option>High (Best Quality)</option>
                                <option>Medium (Balanced)</option>
                                <option>Low (Smallest Size)</option>
                            </select>
                        </div>
                    </div>
                </div>

                <!-- Progress Section -->
                <div id="progressSection" class="hidden">
                    <div class="mb-4">
                        <div class="flex justify-between text-sm text-gray-600 mb-1">
                            <span>Converting...</span>
                            <span id="progressPercent">0%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-2.5">
                            <div id="progressBar" class="bg-indigo-600 h-2.5 rounded-full" style="width: 0%"></div>
                        </div>
                    </div>
                    <div class="text-center text-gray-500">
                        <i data-feather="clock" class="w-5 h-5 inline mr-2"></i>
                        <span id="timeRemaining">Estimated time: calculating...</span>
                    </div>
                </div>

                <!-- Result Section -->
                <div id="resultSection" class="hidden text-center p-6 bg-green-50 rounded-lg border border-green-200">
                    <i data-feather="check-circle" class="w-12 h-12 text-green-500 mx-auto mb-4"></i>
                    <h3 class="text-xl font-medium text-green-800 mb-2">Conversion Complete!</h3>
                    <p class="text-gray-600 mb-6">Your video is ready to download</p>
                    <button id="downloadBtn" class="px-6 py-3 bg-green-600 text-white rounded-lg font-medium hover:bg-green-700 transition-colors duration-300">
                        Download MP4
                    </button>
                </div>
            </div>
        </div>
    </main>

    <custom-footer></custom-footer>

    <script src="script.js"></script>
    <script>
        feather.replace();
    </script>
<script src="https://huggingface.co/deepsite/deepsite-badge.js"></script>
</body>
</html>
