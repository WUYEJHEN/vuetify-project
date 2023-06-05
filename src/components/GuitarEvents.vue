<template>
    <v-table hover>
      <thead class="bg-light-blue">
        <tr>
          <th>日期</th>
          <th>名稱</th>
          <th>地點</th>
          <th>主持人</th>
          <th>說明</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="event in events" :key="event.date">
          <td>{{ event.date }}</td>
          <td>{{ event.name }}</td>
          <td>{{ event.place }}</td>
          <td>{{ event.host }}</td>
          <td>
            <pre>
              {{ event.description }}
            </pre>
          </td>
        </tr>
      </tbody>
    </v-table>
  </template>
  
  <script setup>
  const events = [
    {
      date: '9/16',
      name: '社員大會',
      place: '吉他社教室',
      host: '王小明',
      description: `
        1.入社歡迎茶會
        2.指導老師致詞
        3.社長致詞
        4.社規介紹以及教學內容之簡介
      `
    },
    {
      date: '10/31',
      name: '校內吉他表演',
      place: '學校大禮堂',
      host: '王小明社長',
      description: `
        以吉他演奏演唱民歌，曲目如下
        1.海浬來的沙
        2.微風往事
        3.七月涼山
        4.明天會更好(大合唱)
      `
    }
  ]
  </script>
  