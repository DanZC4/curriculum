<template>
  <div
    class="flex justify-center transform duration-300"
    :class="{
      'bg-gray-100 text-gray-900':
        darkmode,
      ' bg-gray-800  text-gray-100':
        lightmode,
    }">
    <div class="w-full ">
     <Header :darkmode="darkmode"
        :lightmode="lightmode"
        :chancheMode="chancheMode" />
     <Proyect :darkmode="darkmode"
        :lightmode="lightmode"
        :chancheMode="chancheMode" 
        :pages="pages"/>
        <Abilities :darkmode="darkmode"
        :lightmode="lightmode"
        :chancheMode="chancheMode"
        :tecnologies="tecnologies"
        />
        <Contact :darkmode="darkmode"
        :lightmode="lightmode"
        :chancheMode="chancheMode"/>
    </div>
  </div>
</template>

<script>

 
export default {
  data() {
    return {
      pages: [
          {
            id: 1,
          name: 'Manor Lodge',
          image: 'ManorLodge.png',
          link: 'https://www.manorlodgedentalsurgery.co.uk/'
        },
      ],
      tecnologies: [
        {
          name:'JS',
          color:'text-black  bg-gradient-to-tl from-yellow-400 to-yellow-600'
        },
        {
          name:'HTML',
          color:'text-white  bg-gradient-to-tl from-yellow-500 to-red-600'
        },
        {
          name:'CSS',
          color:'text-whie bg-gradient-to-tl from-blue-800 to-blue-400'
        },
        {
          name:'PHP',
          color:'text-black bg-gradient-to-tl from-purple-900  to-blue-500'
        },
        {
          name:'Laravel',
          color:'text-red-600 bg-gradient-to-tl from-black via-black to-gray-900'
        },
          {
          name:'VUE',
          color:'text-white  bg-gradient-to-tl from-green-500 to-gray-200'
        },
          {
          name:'node.js',
          color:'text-green-600 bg-gray-800'
        },
          {
          name:'GIT',
          color:'text-black bg-gradient-to-tl from-yellow-500 to-red-500'
        },
           {
          name:'Github',
          color:'text-white bg-gradient-to-tl from-gray-800 to-gray-700'
        },
          {
          name:'Gitlab',
          color:'text-white bg-gradient-to-tr from-red-500 to-yellow-400'
        },
          {
          name:'Tailwind',
          color:'text-white bg-gradient-to-tl from-green-400 to-blue-300'
        },
            {
          name:'TS',
          color:'text-white bg-blue-700'
        },
            {
          name:'Graphql',
          color:'text-white bg-pink-600'
        }

      ]
   
    };
  },
  
  props: {
    darkmode: Boolean,
    lightmode: Boolean,
    chancheMode: Function,
  },
};
</script>
