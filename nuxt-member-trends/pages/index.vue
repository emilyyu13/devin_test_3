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
              <option>2025</option>
            </select>
            <span>年</span>
            <select class="form-select month-select">
              <option>3</option>
            </select>
            <span>月</span>
          </div>
        </div>
        
        <div class="form-group">
          <label>店舗</label>
          <select class="form-select store-select">
            <option>長堀橋</option>
          </select>
        </div>
        
        <div class="form-actions">
          <button class="btn btn-primary">明細表示・印刷</button>
        </div>
      </div>
    </div>
  </div>
</template>

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
</style>
