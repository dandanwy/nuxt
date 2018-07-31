<template>
  <div>
      <h2>News Index page</h2>
      <p>NEWSID:{{$route.params.newsId}}</p>
       <ul>
        <li><nuxt-link :to="{name:'index'}"></nuxt-link>Home</li>
        <li><nuxt-link :to="{name:'news-id',params:{id:123,title:'dandan.com'}}">News-1</nuxt-link></li>
        <li><nuxt-link :to="{name:'news-id',params:{id:456}}">News-2</nuxt-link></li>
      </ul>
  </div>
</template>