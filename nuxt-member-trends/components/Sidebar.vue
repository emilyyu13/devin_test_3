<template>
  <aside class="sidebar">
    <div class="sidebar-header">
      <select class="form-select">
        <option>文書管理</option>
      </select>
      <button class="btn btn-light">変更</button>
    </div>
    
    <div class="search-box">
      <input type="text" class="form-control" placeholder="会員検索">
      <button class="btn btn-search">
        <span class="search-icon">⚲</span>
      </button>
    </div>
    
    <nav class="sidebar-nav">
      <ul>
        <li><a href="#"><span class="icon">🔍</span> 会員情報検索・確認</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">📅</span> 入会予約管理</a>
          <ul class="dropdown-menu">
            <li><a href="#">新規入会予約登録・確認</a></li>
          </ul>
        </li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">👤</span> パーソナル予約管理</a>
        </li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">🏢</span> 法人情報 管理</a>
        </li>
        <li><a href="#"><span class="icon">👥</span> 来館中会員一覧</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">💬</span> 伝言管理</a>
        </li>
        <li><a href="#"><span class="icon">📧</span> メールマガジン</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">👨‍💼</span> スタッフ管理</a>
        </li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">📊</span> 帳票出力</a>
        </li>
        <li><a href="#"><span class="icon">📍</span> 会員プロッティング</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle"><span class="icon">⚙️</span> 基本情報管理</a>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<style scoped>
/* Sidebar styles */
.sidebar {
  width: 250px;
  background-color: #2c3e50;
  color: white;
  padding: 15px 0;
}

.sidebar-header {
  display: flex;
  padding: 0 15px 15px;
  border-bottom: 1px solid #34495e;
}

.form-select {
  padding: 6px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

.search-box {
  display: flex;
  padding: 15px;
  gap: 5px;
}

.form-control {
  padding: 6px;
  border-radius: 4px;
  border: 1px solid #ccc;
  width: 100%;
}

.btn-search {
  background-color: #2c3e50;
  border: none;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 30px;
}

.search-icon {
  font-size: 18px;
}

.sidebar-nav ul {
  list-style: none;
}

.sidebar-nav li {
  margin-bottom: 2px;
}

.sidebar-nav a {
  display: block;
  padding: 10px 15px;
  color: white;
  text-decoration: none;
}

.sidebar-nav a:hover {
  background-color: #34495e;
}

.dropdown-toggle::after {
  content: "▼";
  font-size: 10px;
  margin-left: 5px;
}

.dropdown-menu {
  padding-left: 20px;
  display: none;
}

.dropdown:hover .dropdown-menu {
  display: block;
}

.icon {
  margin-right: 5px;
  width: 16px;
  display: inline-block;
}
</style>
