<template>
  <commentTable :thead="['Name', 'Text', 'Status', 'Change Status', 'Delet']">
    <tbody slot="tbody">
      <tr v-for="comment in comments" :key="comment.id">
        <td>
          <span>{{ comment.name }}</span>
        </td>
        <td>
          <span>{{ comment.text }}</span>
        </td>
        <td>
          <span v-if="comment.status" class="status true">Publish</span>
          <span v-else class="status false">Hiden</span>
        </td>
        <td>
          <span @click="changeComment(comment.id)" class="link">Change Status</span>
        </td>
        <td>
          <span @click="deleteComment(comment.id)" class="link">Delete</span>
        </td>
      </tr>
    </tbody>
  </commentTable>
</template>

<script>
import commentTable from "@/components/Admin/CommentTable.vue";
export default {
  components: { commentTable },
  layout: "admin",
  data() {
    return {
      comments: [
        {
          id: 1,
          name: "Alex",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          status: true,
        },
        {
          id: 2,
          name: "Aaron",
          text:
            "Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          status: false,
        },
      ],
    };
  },
  methods: {
    changeComment(id) {
      console.log(`Chenge comment id - ${id}`);
    },
    deleteComment(id) {
      console.log(`Delete comment id - ${id}`);
    }
  },
};
</script>
