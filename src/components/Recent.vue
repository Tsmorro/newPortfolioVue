


<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Recent extends Vue {
  @Prop() private project!: {
      title: string,
      tags: [],
      img: string
  };
}
</script>

<style scoped lang="scss">

</style>