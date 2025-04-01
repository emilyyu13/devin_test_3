<template>
  <div>
    <div class="breadcrumb">
      > 店舗用管理画面
    </div>

    <h1 class="page-title">会員動向表</h1>

    <div class="content-box">
      <div class="content-box-header">
        <h2>会員動向表</h2>
      </div>
      
      <div class="content-box-body">
        <div class="form-group">
          <label>対象月指定</label>
          <div class="date-selector">
            <select class="form-select year-select">
              <option>2023</option>
              <option>2024</option>
              <option selected>2025</option>
              <option>2026</option>
            </select>
            <span>年</span>
            <select class="form-select month-select">
              <option>1</option>
              <option>2</option>
              <option selected>3</option>
              <option>4</option>
              <option>5</option>
              <option>6</option>
              <option>7</option>
              <option>8</option>
              <option>9</option>
              <option>10</option>
              <option>11</option>
              <option>12</option>
            </select>
            <span>月</span>
          </div>
        </div>
        
        <div class="form-group">
          <label>店舗</label>
          <select class="form-select store-select">
            <option selected>長堀橋</option>
            <option>梅田</option>
            <option>なんば</option>
            <option>天王寺</option>
          </select>
        </div>
        
        <div class="form-actions">
          <button class="btn btn-primary" @click.prevent="showResults = true">明細表示・印刷</button>
        </div>
        
        <div v-if="showResults" class="results-section">
          <h3 class="results-title">会員動向表結果</h3>
          <table class="results-table">
            <thead>
              <tr>
                <th>会員番号</th>
                <th>氏名</th>
                <th>来店回数</th>
                <th>最終来店日</th>
                <th>ステータス</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="i in 5" :key="i">
                <td>1000{{ i }}</td>
                <td>会員 {{ i }}</td>
                <td>{{ Math.floor(Math.random() * 10) + 1 }}</td>
                <td>2025/03/{{ Math.floor(Math.random() * 28) + 1 }}</td>
                <td>アクティブ</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showResults: false
    }
  }
}
</script>

<style>
.breadcrumb {
  margin-bottom: 20px;
  color: #666;
}

.page-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.content-box {
  background-color: white;
  border-radius: 4px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
}

.content-box-header {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-bottom: 1px solid #ddd;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}

.content-box-header h2 {
  font-size: 16px;
  margin: 0;
  color: #666;
}

.content-box-body {
  padding: 20px;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

.date-selector {
  display: flex;
  align-items: center;
  gap: 5px;
}

.year-select, .month-select {
  width: 100px;
}

.store-select {
  width: 100%;
}

.form-actions {
  margin-top: 30px;
}

.results-section {
  margin-top: 30px;
  border-top: 1px solid #ddd;
  padding-top: 20px;
}

.results-title {
  font-size: 18px;
  margin-bottom: 15px;
}

.results-table {
  width: 100%;
  border-collapse: collapse;
}

.results-table th,
.results-table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

.results-table th {
  background-color: #f5f5f5;
  font-weight: bold;
}

.results-table tr:nth-child(even) {
  background-color: #f9f9f9;
}

.results-table tr:hover {
  background-color: #f0f0f0;
}
</style>
