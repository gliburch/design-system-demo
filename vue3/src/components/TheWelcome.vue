<script >
import { reactive, ref, toRefs } from "vue";
import WelcomeItem from "./WelcomeItem.vue";
import DocumentationIcon from "./icons/IconDocumentation.vue";
import ToolingIcon from "./icons/IconTooling.vue";
import EcosystemIcon from "./icons/IconEcosystem.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";
import StyledCheckbox from "@/components/integration-design-system/src/components/styled-checkbox/StyledCheckbox.vue2.vue3.vue";
import StyledRadio from "@/components/integration-design-system/src/components/styled-radio/StyledRadio.vue2.vue3.vue";

export default {
  components:{
    StyledRadio,
    StyledCheckbox
  },
  setup() {
    const checkbox = reactive({
      foo: false,
      bar: true,
    });
    const radio = ref('foo');
    // const radio = ref("foo");
    const changeParent = (value) => {
      
      radio.value = value;
      console.log(value)
    };

    return {
      changeParent,
      checkbox,
      radio,
      ...toRefs(checkbox)
    };
  },
};
</script>

<template>
  <div>
    <h2>Styled Checkbox</h2>
    <ul>
      <li>
        <label>
          <StyledCheckbox v-model="checkbox.foo"
          :value="foo"
          />
          foo
        </label>
      </li>
      <li>
        <label>
          <StyledCheckbox v-model="checkbox.bar" :value="bar"/>
          bar
        </label>
      </li>
    </ul>
    <h2>Styled Radio</h2>
    <ul>
      <li>
        <label>
          <StyledRadio
            v-model="radio"
            :Name="'radio'"
            :Val="'foo'"
          />
          foo
        </label>
      </li>
      <li>
        <label>
          <StyledRadio
            v-model="radio"
            :Name="'radio'"
            :Val="'bar'"
          />
          bar
        </label>
      </li>
      <!-- <li>
        <label>
          <StyledRadio
           
            :name="'radio'"
            :Val="'foo'"
            :value="'foo'"
            @input="changeParent"
          />
          foo
        </label>
      </li>
      <li>
        <label>
          <StyledRadio
           
            :name="'radio'"
            :Val="'bar'"
            :value="'bar'"
            @input="changeParent"
          />
          bar
        </label>
      </li> -->
    </ul>
  </div>
  <!-- <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Documentation</template>

      Vue’s
      <a target="_blank" href="https://v2.vuejs.org/">official documentation</a>
      provides you with all information you need to get started.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <ToolingIcon />
      </template>
      <template #heading>Tooling</template>

      This project is served and bundled with
      <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite</a>. The recommended IDE
      setup is <a href="https://code.visualstudio.com/" target="_blank">VSCode</a> +
      <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>. If you need to
      test your components and web pages, check out
      <a href="https://www.cypress.io/" target="_blank">Cypress</a> and
      <a href="https://docs.cypress.io/guides/component-testing/introduction" target="_blank"
        >Cypress Component Testing</a
      >.

      <br />

      More instructions are available in <code>README.md</code>.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <EcosystemIcon />
      </template>
      <template #heading>Ecosystem</template>

      Get official tools and libraries for your project:
      <a target="_blank" href="https://pinia.vuejs.org/">Pinia</a>,
      <a target="_blank" href="https://v3.router.vuejs.org/">Vue Router</a>,
      <a target="_blank" href="https://vue-test-utils.vuejs.org/">Vue Test Utils</a>, and
      <a target="_blank" href="https://github.com/vuejs/devtools">Vue Dev Tools</a>. If you need
      more resources, we suggest paying
      <a target="_blank" href="https://github.com/vuejs/awesome-vue">Awesome Vue</a>
      a visit.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>Community</template>

      Got stuck? Ask your question on
      <a target="_blank" href="https://chat.vuejs.org">Vue Land</a>, our official Discord server, or
      <a target="_blank" href="https://stackoverflow.com/questions/tagged/vue.js">StackOverflow</a>.
      You should also subscribe to
      <a target="_blank" href="https://news.vuejs.org">our mailing list</a> and follow the official
      <a target="_blank" href="https://twitter.com/vuejs">@vuejs</a>
      twitter account for latest news in the Vue world.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>Support Vue</template>

      As an independent project, Vue relies on community backing for its sustainability. You can
      help us by
      <a target="_blank" href="https://vuejs.org/sponsor/">becoming a sponsor</a>.
    </WelcomeItem> -->
</template>
