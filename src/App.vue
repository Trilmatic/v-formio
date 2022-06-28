<template>
  <form ref="$form" @submit.prevent="submit()"></form>
</template>

<script>
import FormBuilder from "@trilmatic/form-builder";
import "@trilmatic/form-builder/src/tabs.css";
import "@trilmatic/form-builder/src/sections.css";
import "@trilmatic/form-builder/src/rows.css";
import "@trilmatic/form-builder/src/forms.css";

export default {
  name: "App",
  data() {
    return {
      endpoint: "/submit",
      tabs: [
        {
          id: "tab1",
          label: "Tab 1",
          selected: true,
          sections: [
            {
              id: "personal-section",
              label: "Personal Information",
              rows: [
                {
                  id: "row1",
                  schema: [
                    {
                      id: "firstname",
                      type: "text",
                      label: "First Name",
                      placeholder: "First Name",
                      required: true,
                      onChange: () => {
                        console.log(this.data);
                      },
                    },
                    {
                      id: "lastname",
                      type: "text",
                      label: "Last Name",
                      required: true,
                      onChange: () => {
                        console.log(this.data);
                      },
                    },
                    {
                      id: "test",
                      type: "text",
                      label: "Last Name",
                      required: true,
                      onChange: () => {
                        console.log(this.data);
                      },
                    },
                  ],
                },
              ],
            },
          ],
        },
        {
          id: "tab2",
          label: "Tab 2",
          selected: false,
          disabled: true,
        },
      ],
      /*schema: {
        foo: {
          label: "foo",
          type: "text",
          required: true,
          disabled: (value) => {
            if (value == "foo") return true;
            return false;
          },
          onChange: () => {
            console.log(this.data.foo);
          },
        },
        bar: {
          label: "bar",
          type: "email",
          debounce: 1000,
          placeholder: "Placeholder",
          required: true,
        },
        aaa: {
          type: "hidden",
        },
        submitBtn: {
          type: "button",
          btnType: "button",
          html: "Check Data",
          onClick: () => {
            console.log(this.$refs);
          },
        },
      },*/
    };
  },
  mixins: [FormBuilder],
};
</script>

<style>
#app {
  font-family: "Rubik", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 2rem;
}
</style>
