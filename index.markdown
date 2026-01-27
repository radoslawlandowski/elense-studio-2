---
layout: default
---

<div class="home">
  <h1 class="page-heading">Elense Studio</h1>

  <div class="tiles-container">
    <a href="{{ '/software/' | relative_url }}" class="tile">
      <div class="tile-content">
        <h2>Elense Software</h2>
      </div>
    </a>
    <a href="{{ '/engineering/' | relative_url }}" class="tile">
      <div class="tile-content">
        <h2>Elense Engineering</h2>
      </div>
    </a>
    <a href="{{ '/leathercraft/' | relative_url }}" class="tile">
      <div class="tile-content">
        <h2>Elense Leathercraft</h2>
      </div>
    </a>
  </div>
</div>

<style>
.tiles-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 40px;
}

.tile {
  display: block;
  text-decoration: none;
  color: inherit;
  border: 1px solid #e8e8e8;
  border-radius: 8px;
  padding: 40px 20px;
  text-align: center;
  transition: transform 0.2s, box-shadow 0.2s;
  background-color: #fdfdfd;
}

.tile:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  text-decoration: none;
  color: #2a7ae2;
}

.tile h2 {
  margin: 0;
}
</style>
