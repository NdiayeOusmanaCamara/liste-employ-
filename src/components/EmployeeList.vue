<template>
    <div>
      <h1>Liste des employés</h1>
      <ol>
        <li v-for="employee in employees" :key="employee.id" @mouseover="hover = employee.id" @mouseleave="hover = null" :class="{ 'hovered': hover === employee.id }">
          {{ employee.name }}
        </li>
      </ol>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        employees: [
          { id: 1, name: 'Samba' },
          { id: 2, name: 'Mohmed' },
          { id: 3, name: 'Bambi' },
          { id: 4, name: 'Lamine' },
          { id: 5, name: 'Bandia' },
          { id: 6, name: 'Koita' },
          { id: 7, name: 'Mariam' },

        ],
        hover: null
      };
    }
  }
  </script>
  
  <style scoped>
ol {
  padding-left: 20px;
  max-width: 400px;
  margin: 0 auto;
  border-radius: 8px;
  background-color: #f9f9f9;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}



li {
  padding: 12px;
  margin: 8px 0;
  border-radius: 6px;
  transition: background-color 0.3s ease, transform 0.3s ease;
  font-size: 1.1em;
  font-weight: 500;
  color: #333;
  background-color: #ffffff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}


li.hovered {
  background-color: #e3f2fd; 
  color: #0d47a1; 
  transform: translateY(-2px); 
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}


h1 {
  font-size: 1.8em;
  font-weight: 600;
  margin-bottom: 20px;
  color: #333;
  text-align: center;
  border-bottom: 2px solid #ddd;
  padding-bottom: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
</style>
