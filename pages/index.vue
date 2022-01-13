<template>
    <div class="bg-gray-100 md:grid md:grid-cols-3">
        <div class="text-white bg-gray-600">
            <div class="md:max-h-screen w-full p-7 md:p-10 md:static md:overflow-y-auto">           
                <div class="mb-5">
                    <h1 class="text-2xl bold uppercase">Everson Araújo Barbosa</h1>
                    <p>Fullstack developer PHP, Vuejs...</p>
                </div>

                <h2 class="text-xl">Personal Info</h2>
                <p><strong>Email:</strong> eversonaraujo9@gmail.com</p>
                <p><strong>Address:</strong> Brazil, Brasília, Distrito Federal</p>
                <a href="https://www.linkedin.com/in/everson-ara%C3%BAjo-34524b58/"
                    class="bg-blue-500 p-1 px-2 inline-block mt-2 text-sm rounded-full" target="_blank">
                    Linkedin
                </a>

                <card-info title="Basics" :items="['HTML5, SEO, CSS3, SCSS, Bootstrap, Tailwind, etc.']" />
                
                <card-info title="Languages" :items="[
                    'PHP <i>(Zend, Symfony)</i>',
                    'Javascript <i>(Jquery, Vuejs, Reactjs, Nextjs, Nuxtjs)</i>',
                    'Java <i>(SpringMVC, Hibernate, Android)</i>']" 
                />
                
                <card-info title="Databases" :items="['MySQL', 'PostgreSQL', 'SQLite']" />
                
                <card-info title="DevOps" :items="['Ubuntu, Apache, Cron jobs', 'Docker and Docker Compose', 'Git', 'Jenking (<i class=\'text-sm\'>Learning</i>)']" />
                
                <card-info title="Cloud" :items="['Digital Ocean']" />
                
                <card-info title="Next Goals" :items="['Laravel, React Native, Kubernets']" />
            
            </div>
        </div>
        <div class="col-span-2 h-auto md:max-h-screen w-full p-7 md:p-10 md:static md:overflow-y-auto">           
            <h2 class="text-2xl bolder uppercase">Graduation</h2>
            
            <div class="mt-5 bg-white text-gray-700 p-7 rounded md:shadow">
                <span class="text-xs bold text-black bg-green-300 p-1 px-2 uppercase rounded-full">Graduated as</span>
                <h2 class="text-xl text-blue-800 mt-2">Analist and Developer of Software</h2>
                <p class="text-sm">Conclusion 2015, Centro Universitário IESB - Brasília-DF</p>
            </div>

            <h2 class="mt-7 text-2xl bolder uppercase">Work History</h2>

            <job-info 
                role="Designer"
                company="Photoimage"
                time="about 3 years"
                activities="Printing preparation, working with photoshop, illustrator, etc"
            />
            
            <job-info 
                role="Software Development"
                company="Quantico"
                time="7 years, from 2015 til october 2021"
                activities="On main time I worked with PHP, Symfony, Doctrine and Vuejs,
                    but somethimes Wordpress, creating Landing Pages,
                    setuping up Ubuntu's server on Digital Ocean."

                :projects="[
                    { 
                        name: 'Nicolandia Center Park Payment',
                        link: 'https://pague.yuupe.com', 
                        architecture: 'Symfony REST API, and Nuxtjs',
                        desc: 'Payment system, integrated by APIs (Wirecard, Pagar.me, Iugu).'
                    },
                    { 
                        name: 'Yuupe Landing Pages',
                        link: 'https://yuupe.com',
                        architecture: 'Symfony REST API, and Vuejs',
                        desc: 'System to creating LPs, automations lists, email marketing using Sendgrid API.'
                    },
                    { 
                        name: 'Nullar',
                        link: 'https://nullar.com.br',
                        architecture: 'Symfony REST API, and Reactjs',
                        desc: 'Schedule services for assembly mobles.'
                    }
                ]"
            />

             <job-info 
                role="Software Development Front-end"
                company="GestãoClick"
                time="current, since november 2021"
                activities="Working by squads, using Atrassian Jira, recreating pages with Vuejs"
            />
        </div>
    </div>
</template>

<style>
    html, body, #__nuxt { min-height: 100vh; } 
</style>
