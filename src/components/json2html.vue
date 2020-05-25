<template>
  <div class="index-view" v-html="content"></div>
</template>

<script>
// import componentItem from "./item";
const json2Html = require("html2json").json2html;
export default {
  name: "HelloWorld",
  components: {
    // componentItem,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      content: "content",
      items: {
        node: "root",
        child: [
          {
            node: "element",
            tag: "div",
            attr: { id: "1", class: "form-content" },
            child: [
              {
                node: "element",
                tag: "h1",
                child: [{ node: "text", text: "客户详情" }],
              },
              {
                node: "element",
                tag: "pre",
                attr: { id: "demo", class: ["foo", "bar"] },
                child: [{ node: "text", text: "{{content}}" }],
              },
              {
                node: "element",
                tag: "pre",
                attr: { id: "output", class: "goo" },
                child: [{ node: "text", text: "goo" }],
              },
              {
                node: "element",
                tag: "input",
                attr: { id: "execute", type: "button", value: "execute" },
              },
            ],
          },
          {
            node: "element",
            tag: "table",
            attr: { class: ["el-table", "el-table--border"] },
            child: [
              {
                node: "element",
                tag: "thead",
                child: [
                  {
                    node: "element",
                    tag: "th",
                    child: [{ node: "text", text: "商品名称" }],
                  },
                  {
                    node: "element",
                    tag: "th",
                    child: [{ node: "text", text: "成交数量" }],
                  },
                  {
                    node: "element",
                    tag: "th",
                    child: [{ node: "text", text: "成交金额（1️元）" }],
                  },
                  {
                    node: "element",
                    tag: "th",
                    child: [{ node: "text", text: "已支付金额" }],
                  },
                  {
                    node: "element",
                    tag: "th",
                    child: [{ node: "text", text: "有效期" }],
                  },
                ],
              },
              {
                node: "element",
                tag: "tbody",
                child: [
                  {
                    node: "element",
                    tag: "tr",
                    child: [
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "321" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312.32" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312.3232" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "2020-05-25~2020-05-29" }],
                      },
                    ],
                  },
                ],
              },
            ],
          },
          {
            node: "element",
            tag: "table",
            attr: { class: ["el-table", "el-table--border"] },
            child: [
              {
                node: "element",
                tag: "tbody",
                child: [
                  {
                    node: "element",
                    tag: "tr",
                    child: [
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "321" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312.32" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "312.3232" }],
                      },
                      {
                        node: "element",
                        tag: "td",
                        child: [{ node: "text", text: "2020-05-25~2020-05-29" }],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        ],
      },
    };
  },
  mounted() {
    this.content = json2Html(this.items);
  },
  methods: {
    getValue(value) {
      return value || "hhahah";
    },
  },
};
</script>

<style>
.index-view {
  height: 100%;
}
.form-content {
  background: red;
  width: 100%;
}
</style>
