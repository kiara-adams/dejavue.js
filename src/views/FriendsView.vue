<template>
  <div>
    <h1>Friends View</h1>
    <div v-if="friends.length === 0">Loading...</div>
    <div v-else>
      <div v-for="(friend, index) in friends" :key="friend.id" class="friend-card" :class="{ 'male': friend.gender === 'male', 'female': friend.gender === 'female' }">
        <h2>{{ friend.firstName }} {{ friend.lastName }}</h2>
        <p>Contact Details: {{ friend.contactDetails }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import jsonData from '@/data.json'; 

export default {
  data() {
    return {
      friends: jsonData.friends,
    };
  },
};
</script>

<style scoped>
.friend-card {
  border: 2px solid transparent;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 8px;
}

.friend-card.male {
  border-color: gold;
}

.friend-card.female {
  border-color: green;
}
</style>
