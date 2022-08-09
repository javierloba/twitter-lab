<template>
  <div className="tweet">
    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <UserComponent :name="user.name" :handle="user.handle" />
        <TimestampComponent :timestamp="timestamp" />
      </div>
      <MessageComponent :message="message" />
      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>
import UserComponent from "./UserComponent.vue";
import TimestampComponent from "./TimestampComponent.vue";
import ProfileImage from "./ProfileImage.vue";
import MessageComponent from "./MessageComponent.vue";
export default {
  props: ["user", "timestamp", "message"],
  components: {
    UserComponent,
    TimestampComponent,
    ProfileImage,
    MessageComponent,
  },
};
</script>
<style scoped>
a {
  color: #42b983;
}
</style>
