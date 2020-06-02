<script>
export default {
  name: "Tabs",
  props: {
    tabs: Array
  },
  data() {
    return {
      selectedIndex: 0
    };
  },
  methods: {
    setSelected: function(index) {
      this.selectedIndex = index;
    },
    getTabElements: function(createElement, tabChildren) {
      let tabItems = [];
      for (let i = 0; i < tabChildren.length; i++) {
        tabItems.push(
          createElement(
            "div",
            {
              class: {
                tabItem: true,
                tabItemSelected: this.selectedIndex == i
              },
              on: {
                click: () => {
                  this.setSelected(i);
                }
              }
            },
            [tabChildren[i]]
          )
        );
      }
      return tabItems;
    },
    getContentElements: function(createElement, contentChildren) {
      let contentItems = [];
      for (let i = 0; i < contentChildren.length; i++) {
        contentItems.push(
          createElement(
            "div",
            {
              class: {
                contentItem: true,
                selectedContentItem: this.selectedIndex == i
              }
            },
            [contentChildren[i]]
          )
        );
      }
      return contentItems;
    }
  },
  render: function(createElement) {
    let slots = this.$scopedSlots.default();
    let tabChildren = slots[0].children;
    let contentChildren = slots[1].children;
    return createElement("div", [
      //TABS
      createElement(
        "div",
        { class: "tabs" },
        this.getTabElements(createElement, tabChildren)
      ),
      //CONTENT
      createElement(
        "div",
        { class: "content" },
        this.getContentElements(createElement, contentChildren)
      )
    ]);
  }
};
</script>

<style scoped>
.tabs {
  display: flex;
  flex-direction: row;
  gap: 5%;
}
.tabItem {
  padding: 0.25em 0.75em 0.25em 0.75em;
  border: solid #e35d5b 2px;
  border-radius: 999em;
  color: #e35d5b;
  cursor: pointer;
}
.tabItem * {
  padding: 0;
  margin: 0;
}
.tabItemSelected {
  color: white;
  background-color: #e35d5b;
  transition: all 0.3s ease-in-out;
}

.contentItem {
  transition: all 0.3s ease-in;
  display: none;
}
.selectedContentItem {
  transition: all 0.3s ease-in;
  display: block;
}
</style>
