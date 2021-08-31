<template>
  <div>
    <md-table v-model="foods" md-sort="name" md-sort-order="asc" md-card>
      <md-table-toolbar>
        <h1 class="md-title">점심메뉴</h1>
      </md-table-toolbar>

      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="음식" md-sort-by="name">
          {{ item.name }}
        </md-table-cell>
        <md-table-cell md-label="슈퍼패스" md-sort-by="email">
          {{ item.email }}
        </md-table-cell>
        <md-table-cell md-label="슈퍼패스" md-sort-by="email2">
          <md-button class="md-icon-button md-raised md-accent">
            <md-icon>thumb_up</md-icon>
          </md-button>
        </md-table-cell>
        <md-table-cell md-label="추천 수" md-sort-by="gender">
          {{ item.gender }}
        </md-table-cell>
        <md-table-cell md-label="추천" md-sort-by="title">
          <md-button class="md-fab md-mini md-primary">
            <md-icon>add</md-icon>
          </md-button>
        </md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "IconButtons",
  data: () => ({
    foods: [
      {
        id: 1,
        name: "치킨",
        email: "이주상",
        gender: "2",
      },
      {
        id: 2,
        name: "피자",
        email: "",
        gender: "3",
      },
      {
        id: 3,
        name: "짜글이",
        email: "",
        gender: "5",
      },
      {
        id: 4,
        name: "곱창",
        email: "유순조",
        gender: "6",
      },
      {
        id: 5,
        name: "중식",
        email: "",
        gender: "1",
      },
    ],
  }),
};
</script>
