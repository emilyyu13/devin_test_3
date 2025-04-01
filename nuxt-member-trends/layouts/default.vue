<template>
  <div>
    <header class="main-header">
      <div class="logo">URBAN FIT24DM</div>
      <div class="header-controls">
        <div class="system-id">システム確認用(ID:20528)</div>
        <input type="text" class="form-control header-input" placeholder="担当者名">
        <button class="btn btn-change-staff">担当変更</button>
        <button class="btn btn-light">練習用</button>
      </div>
    </header>
    
    <div class="main-container">
      <Sidebar />
      
      <main class="content">
        <slot />
      </main>
    </div>
  </div>
</template>

<style>
/* Header styles */
.main-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #e9a84c;
  color: white;
  padding: 10px 20px;
  height: 60px;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.header-controls {
  display: flex;
  align-items: center;
  gap: 10px;
}

.system-id {
  margin-right: 10px;
}

.header-input {
  width: 150px;
  height: 30px;
}

.btn {
  padding: 6px 12px;
  border-radius: 4px;
  border: 1px solid #ccc;
  cursor: pointer;
  font-size: 14px;
}

.btn-light {
  background-color: white;
  color: #333;
}

.btn-primary {
  background-color: #337ab7;
  color: white;
  border-color: #2e6da4;
}

/* Special styling for the 担当変更 button */
.btn-change-staff {
  background-color: #31b0d5;
  border-color: #269abc;
  color: white;
}

/* Main container */
.main-container {
  display: flex;
  min-height: calc(100vh - 60px);
}

/* Content styles */
.content {
  flex: 1;
  padding: 20px;
}
</style>
