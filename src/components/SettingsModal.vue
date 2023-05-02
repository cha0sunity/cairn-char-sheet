<template>
  <div class="modalMain" @click.self="closeModal">
    <div class="modalCenter">
        <h2>Character</h2>
        <button @click.self="saveChar">Save</button>
        <button @click.self="loadChar">Load</button>
    </div>
  </div>
</template>

<script>
export default {
    methods: {
        closeModal() {
            this.$emit('close')
        },
        saveChar() {
            this.$emit('save')
        },
        loadChar() {
            this.$emit('load')
        }
    }

}
</script>

<style>
.modalMain {
    top: 0;
    position: fixed;
    width: 500px;
    height: 800px;
    background-color: rgba(0,0,0,0.5);
}

.modalCenter {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
}

button {
  appearance: none;
  background-color: #000000;
  border: 2px solid #1A1A1A;
  border-radius: 15px;
  box-sizing: border-box;
  color: #FFFFFF;
  cursor: pointer;
  display: inline-block;
  font-family: Roobert,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  font-size: 16px;
  font-weight: 600;
  line-height: normal;
  margin: 0;
  margin-bottom: 5px;
  min-height: 60px;
  min-width: 0;
  outline: none;
  padding: 16px 24px;
  text-align: center;
  text-decoration: none;
  transition: all 300ms cubic-bezier(.23, 1, 0.32, 1);
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  width: 100%;
  will-change: transform;
}

button:disabled {
  pointer-events: none;
}

button:hover {
  box-shadow: rgba(0, 0, 0, 0.25) 0 8px 15px;
  transform: translateY(-2px);
}

button:active {
  box-shadow: none;
  transform: translateY(0);
}

*:focus {
    outline: none;
}


</style>