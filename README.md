<style>
.floating { 
  animation: floating 3s ease-in-out infinite;
}

@keyframes floating {
  0% { transform: translate(0, 0px); }
  50% { transform: translate(0, -15px); }
  100% { transform: translate(0, 0px); }
}

.pulse {
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.05); }
  100% { transform: scale(1); }
}
</style>

<div align="center">

<img src="https://via.placeholder.com/150" class="floating" style="border-radius: 50%;">

<h1 class="pulse">¡Bienvenido a mi perfil! 🚀</h1>

</div>
