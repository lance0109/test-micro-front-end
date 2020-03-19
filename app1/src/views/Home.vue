<template>
  <div class="home">
    <el-table
          :data="tableData"
          style="width: 100%">
          <el-table-column
            prop="date"
            label="日期"
            width="180">
          </el-table-column>
          <el-table-column
            prop="name"
            label="姓名"
            width="180">
          </el-table-column>
          <el-table-column
            prop="address"
            label="地址">
          </el-table-column>
        </el-table>
    
    <!-- <i-table :columns="columns1" :data="data1"></i-table> -->
    <img
      alt="Vue logo"
      :src="baseUrl + '/img/logo.png'"
    >
    <h1>{{ $store.state.a }}</h1>
  </div>
</template>

<script>
import logo from '@/assets/logo.png'

export default {
  name: 'home',
  data () {
    return {
        tableData: [{
                    date: '2016-05-02',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                  }, {
                    date: '2016-05-04',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1517 弄'
                  }, {
                    date: '2016-05-01',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1519 弄'
                  }, {
                    date: '2016-05-03',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1516 弄'
                  }],
        columns1: [
                            {
                                title: '姓名',
                                key: 'name'
                            },
                            {
                                title: '年龄',
                                key: 'age'
                            },
                            {
                                title: '地址',
                                key: 'address'
                            }
                        ],
                        data1: [
                            {
                                name: '王小明',
                                age: 18,
                                address: '北京市朝阳区芍药居'
                            },
                            {
                                name: '张小刚',
                                age: 25,
                                address: '北京市海淀区西二旗'
                            },
                            {
                                name: '李小红',
                                age: 30,
                                address: '上海市浦东新区世纪大道'
                            },
                            {
                                name: '周小伟',
                                age: 26,
                                address: '深圳市南山区深南大道'
                            }
                        ]
    }
  },
  mounted () {
    this.baseSetTab('模块1 主页xxx', 'home')
  },
  methods: {
  }
}
</script>
