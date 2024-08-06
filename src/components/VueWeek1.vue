<script setup>
import { ref } from 'vue'

const drinks = ref([
  {
    id: 1,
    item: '珍珠奶茶',
    desc: '香濃奶茶搭配QQ珍珠',
    price: 50,
    qty: 20
  },
  {
    id: 2,
    item: '冬瓜檸檬',
    desc: '清新冬瓜配上新鮮檸檬',
    price: 45,
    qty: 18
  },
  {
    id: 3,
    item: '翡翠檸檬',
    desc: '綠茶與檸檬的完美結合',
    price: 55,
    qty: 34
  },
  {
    id: 4,
    item: '四季春茶',
    desc: '香醇四季春茶，回甘無比',
    price: 45,
    qty: 10
  },
  {
    id: 5,
    item: '阿薩姆奶茶',
    desc: '阿薩姆紅茶搭配香醇鮮奶',
    price: 50,
    qty: 25
  },
  {
    id: 6,
    item: '檸檬冰茶',
    desc: '檸檬與冰茶的清新組合',
    price: 45,
    qty: 20
  },
  {
    id: 7,
    item: '芒果綠茶',
    desc: '芒果與綠茶的獨特風味',
    price: 55,
    qty: 18
  },
  {
    id: 8,
    item: '抹茶拿鐵',
    desc: '抹茶與鮮奶的絕配',
    price: 60,
    qty: 20
  }
])
</script>
<template>
  <h1>Week1</h1>
  <div>
    <table>
      <thead>
        <tr>
          <th scope="col">品項</th>
          <th scope="col">描述</th>
          <th scope="col">價格</th>
          <th scope="col">庫存</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, key) in drinks" :key="item.id">
          <td>{{ item.item }}</td>
          <td>
            <small>{{ item.desc }}</small>
          </td>
          <td>{{ item.price }}</td>
          <td>
            <button type="button" @click="item.qty > 0 ? item.qty-- : 0">-</button>{{ item.qty
            }}<button type="button" @click="item.qty++">+</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
