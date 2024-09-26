<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import Welcome from '@/Components/Welcome.vue';
import Menu from '@/Components/Menu.vue';

if (document.getElementById("search-table") && typeof simpleDatatables.DataTable !== 'undefined') {
    const dataTable = new simpleDatatables.DataTable("#search-table", {
        searchable: true,
        sortable: false
    });
}

</script>

<template>
<!--    <AppLayout title="Dashboard">
        
        <div class="py-12">
            <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
                <div class="overflow-hidden bg-white shadow-xl sm:rounded-lg">
                    <Welcome />
                </div>
            </div>
        </div>
    </AppLayout>-->
<div>    
    <Menu />
</div>

<div class="p-4 bg-gray-200 sm:ml-64">
   <div class="p-4 bg-white border-2 rounded-lg mt-14">

    <div class="grid grid-cols-1 gap-1">
    <div class="flex justify-between">
        <p class="text-2xl text-black">
            Gestión de Subsedes 
         </p>
      <button data-modal-target="modal" data-modal-toggle="modal" type="button" class="boton_crear">
        <i class="mr-1 fas fa-plus"></i>
        Crear Nueva   
      </button>
    </div>  
    <div class="p-4 bg-blue-200">
     
        <!-- Data Table -->
         
        <table id="search-table">
            <thead>
                <tr>
                    <th>
                        <span class="flex items-center">
                            Company Name
                        </span>
                    </th>
                    <th>
                        <span class="flex items-center">
                            Ticker
                        </span>
                    </th>
                    <th>
                        <span class="flex items-center">
                            Stock Price
                        </span>
                    </th>
                    <th>
                        <span class="flex items-center">
                            Market Capitalization
                        </span>
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Apple Inc.</td>
                    <td>AAPL</td>
                    <td>$192.58</td>
                    <td>$3.04T</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Microsoft Corporation</td>
                    <td>MSFT</td>
                    <td>$340.54</td>
                    <td>$2.56T</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Alphabet Inc.</td>
                    <td>GOOGL</td>
                    <td>$134.12</td>
                    <td>$1.72T</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Amazon.com Inc.</td>
                    <td>AMZN</td>
                    <td>$138.01</td>
                    <td>$1.42T</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">NVIDIA Corporation</td>
                    <td>NVDA</td>
                    <td>$466.19</td>
                    <td>$1.16T</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Tesla Inc.</td>
                    <td>TSLA</td>
                    <td>$255.98</td>
                    <td>$811.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Meta Platforms Inc.</td>
                    <td>META</td>
                    <td>$311.71</td>
                    <td>$816.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Berkshire Hathaway Inc.</td>
                    <td>BRK.B</td>
                    <td>$354.08</td>
                    <td>$783.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">TSMC</td>
                    <td>TSM</td>
                    <td>$103.51</td>
                    <td>$538.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">UnitedHealth Group Incorporated</td>
                    <td>UNH</td>
                    <td>$501.96</td>
                    <td>$466.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Johnson & Johnson</td>
                    <td>JNJ</td>
                    <td>$172.85</td>
                    <td>$452.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">JPMorgan Chase & Co.</td>
                    <td>JPM</td>
                    <td>$150.23</td>
                    <td>$431.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Visa Inc.</td>
                    <td>V</td>
                    <td>$246.39</td>
                    <td>$519.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Eli Lilly and Company</td>
                    <td>LLY</td>
                    <td>$582.97</td>
                    <td>$552.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Walmart Inc.</td>
                    <td>WMT</td>
                    <td>$159.67</td>
                    <td>$429.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Samsung Electronics Co., Ltd.</td>
                    <td>005930.KS</td>
                    <td>$70.22</td>
                    <td>$429.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Procter & Gamble Co.</td>
                    <td>PG</td>
                    <td>$156.47</td>
                    <td>$366.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Nestlé S.A.</td>
                    <td>NESN.SW</td>
                    <td>$120.51</td>
                    <td>$338.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Roche Holding AG</td>
                    <td>ROG.SW</td>
                    <td>$296.00</td>
                    <td>$317.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Chevron Corporation</td>
                    <td>CVX</td>
                    <td>$160.92</td>
                    <td>$310.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">LVMH Moët Hennessy Louis Vuitton</td>
                    <td>MC.PA</td>
                    <td>$956.60</td>
                    <td>$478.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Pfizer Inc.</td>
                    <td>PFE</td>
                    <td>$35.95</td>
                    <td>$200.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Novo Nordisk A/S</td>
                    <td>NVO</td>
                    <td>$189.15</td>
                    <td>$443.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">PepsiCo, Inc.</td>
                    <td>PEP</td>
                    <td>$182.56</td>
                    <td>$311.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">ASML Holding N.V.</td>
                    <td>ASML</td>
                    <td>$665.72</td>
                    <td>$273.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">The Coca-Cola Company</td>
                    <td>KO</td>
                    <td>$61.37</td>
                    <td>$265.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Oracle Corporation</td>
                    <td>ORCL</td>
                    <td>$118.36</td>
                    <td>$319.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Merck & Co., Inc.</td>
                    <td>MRK</td>
                    <td>$109.12</td>
                    <td>$276.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Broadcom Inc.</td>
                    <td>AVGO</td>
                    <td>$861.80</td>
                    <td>$356.00B</td>
                </tr>
                <tr>
                    <td class="font-medium text-gray-900 whitespace-nowrap dark:text-white">Mastercard Incorporated</td>
                    <td>MA</td>
                    <td>$421.44</td>
                    <td>$396.00B</td>
                </tr>
            </tbody>
        </table>


        <!-- Fin Data table -->
        
        <!-- modal -->
        <div id="modal" tabindex="-1" aria-hidden="true" class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
            <div class="relative w-full max-w-md max-h-full p-4">
                <!-- Modal content -->
                <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
                    <!-- Modal header -->
                    <div class="flex items-center justify-between p-4 border-b rounded-t md:p-5 dark:border-gray-600">
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white">
                            Gestión de Subsedes
                        </h3>
                        <button type="button" class="end-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white" data-modal-hide="authentication-modal">
                            <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 14">
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
                            </svg>
                            <span class="sr-only">Close modal</span>
                        </button>
                    </div>
                    <!-- Modal body -->
                    <div class="p-4 md:p-5">
                        <form class="space-y-4" action="#">
                            <div>
                                <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Your email</label>
                                <input type="email" name="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white" placeholder="name@company.com" required />
                            </div>
                            <div>
                                <label for="password" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Your password</label>
                                <input type="password" name="password" id="password" placeholder="••••••••" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white" required />
                            </div>
                            <div class="flex justify-between">
                                <div class="flex items-start">
                                    <div class="flex items-center h-5">
                                        <input id="remember" type="checkbox" value="" class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 dark:bg-gray-600 dark:border-gray-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800" required />
                                    </div>
                                    <label for="remember" class="text-sm font-medium text-gray-900 ms-2 dark:text-gray-300">Remember me</label>
                                </div>
                                <a href="#" class="text-sm text-blue-700 hover:underline dark:text-blue-500">Lost Password?</a>
                            </div>
                            <button type="submit" class="w-full text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Login to your account</button>
                            <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
                                Not registered? <a href="#" class="text-blue-700 hover:underline dark:text-blue-500">Create account</a>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div> 
        <!--Fin Modal -->
        
    </div>
  </div>
    
   </div>
</div>

</template>
