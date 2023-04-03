<template>
  <div class="container">
    <h1>Callout Component Example</h1>
    <h2>Basic</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
    </StyledCallout>
    <br>
    <h2>Outlined</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Outlined>
    </StyledCallout>
    <br>
    <h2>Color Changed</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Color="var(--blue-grey-600)">
    </StyledCallout>
    <br>
    <h2>Close Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Dismissable
      @close="closeCallback">
    </StyledCallout>
    <br>
    <h2>Right Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:right><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Bottom Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:bottom><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Left Icon</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:left>
        <i class="ii ii-info-circle-outline"></i>
      </template>
    </StyledCallout>
    <br>
    <h2>Close Button+Right Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Dismissable
      @close="closeCallback">
      <template v-slot:right><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Close Button+Bottom Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Dismissable
      @close="closeCallback">
      <template v-slot:bottom><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Left Icon+Right Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:left>
        <i class="ii ii-info-circle-outline"></i>
      </template>
      <template v-slot:right><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Left Icon+Bottom Button</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:left>
        <i class="ii ii-info-circle-outline"></i>
      </template>
      <template v-slot:bottom><StyledButton>button</StyledButton></template>
    </StyledCallout>
    <br>
    <h2>Close Button+Left Icon</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Dismissable
      @close="closeCallback">
      <template v-slot:left>
        <i class="ii ii-info-circle-outline"></i>
      </template>
    </StyledCallout>
    <br>
    <h2>Image</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다.">
      <template v-slot:bottom>
        <img src="https://images.pexels.com/photos/3683095/pexels-photo-3683095.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" alt="image" />
      </template>
    </StyledCallout>
    <br>
    <h2>All</h2>
    <StyledCallout
      Title="메디스트림 | Medistream"
      Content="의료인이 진료에 집중할수록 사람들은 더욱 건강해집니다."
      Dismissable
      Outlined
      Color="red"
      @close="closeCallback">
      <template v-slot:left>
        <a class="ii ii-info-circle-outline"></a>
      </template>
      <template v-slot:right><StyledButton>button</StyledButton></template>
    </StyledCallout>
  </div>
</template>

<script>
import StyledCallout from '@/components/integration-design-system/src/components/styled-callout/StyledCallout.vue2.vue3.vue'
import StyledButton from '@/components/integration-design-system/src/components/styled-button/StyledButton.vue2.vue3.vue'

export default {
  name: 'StyledCalloutExample',
  components: {
    StyledCallout,
    StyledButton,
  },
  methods: {
    closeCallback () {
      console.info('Callout Closed')
    }
  }
}
</script>

<style lang="scss" scoped>

.container {
  display: flex;
  width: 550px;
  height: 100%;
  flex-direction: column;
  padding: 50px;

}

h1 {
  margin: 30px 0;
}

.StyledCallout {
  margin: 10px 0;
}

</style>
