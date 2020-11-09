<template>
  <section name="review">
    <article v-for="item in reviews" :key="item.id">
      <img :src="item.avatar" class="photo" />
      <div class="column">
        <p class="name">{{ item.name }}</p>
        <p class="user_review">{{ item.review }}</p>
      </div>
    </article>
  </section>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

* {
  margin: 0;
  outline: 0;
  padding: 0;
  border: 0;
}

section {
  padding: 0 20px;
}

article {
  padding: 0 10px;
  display: flex;
  align-items: center;
  height: 60px;
}

article + article {
  margin-top: 10px;
}

p {
  font-size: 16px;
  color: black;
  font-family: "Roboto";
}

.photo {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: #808080;
  margin-right: 10px;
  object-fit: cover;
}

.column {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name {
  font-weight: bold;
  margin-bottom: 5px;
}

.user_review {
  width: 500px;
  height: 100%;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>

<script>
export default {
  name: "View",
  props: {
    reviews: Array,
  },
};
</script>
