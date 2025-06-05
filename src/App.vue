<template>
  <div class="app-layout">
    <aside class="sidebar">
      <h1 class="sidebar-title">Materi Vue.js</h1>

      <div class="section">
        <h2>Pertemuan 2</h2>
        <ul>
          <li @click="currentView = 'DeclarativeRendering'">Declarative Rendering</li>
          <li @click="currentView = 'AtributBindings'">Attribute Bindings</li>
          <li @click="currentView = 'EventListeners'">Event Listeners</li>
          <li @click="currentView = 'ConditionalRendering'">Conditional Rendering</li>
        </ul>
      </div>

      <div class="section">
        <h2>Pertemuan 3</h2>
        <ul>
          <li @click="currentView = 'ListRendering'">List Rendering</li>
          <li @click="currentView = 'FormBindings'">Form Bindings</li>
          <li @click="currentView = 'ComputedProperty'">Computed Property</li>
          <li @click="currentView = 'Watchers'">Watchers</li>
          <li @click="currentView = 'LifecycleTemplateRefs'">Lifecycle & Template Refs</li>
        </ul>
      </div>
    </aside>

    <main class="content">
      <component :is="currentView" />
    </main>
  </div>
</template>

<script>
import AtributBindings from './components/icons/AtributBindings.vue';
import EventListeners from './components/icons/EventListeners.vue';
import DeclarativeRendering from './components/icons/DeclarativeRendering.vue';
import FormBindings from './components/icons/FormBindings.vue';
import ComputedProperty from './components/icons/ComputedProperty.vue';
import ConditionalRendering from './components/icons/ConditionalRendering.vue';
import LifecycleTemplateRefs from './components/icons/LifecycleTemplateRefs.vue';
import ListRendering from './components/icons/ListRendering.vue';
import Watchers from './components/icons/Watchers.vue';

export default {
  name: 'App',
  components: {
    DeclarativeRendering,
    AtributBindings,
    EventListeners,
    ConditionalRendering,
    ListRendering,
    FormBindings,
    ComputedProperty,
    Watchers,
    LifecycleTemplateRefs
  },
  data() {
    return {
      currentView: 'DeclarativeRendering'
    }
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.app-layout {
  display: flex;
  min-height: 100vh;
  background-color: #f9f9f9;
}

/* Sidebar */
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 260px;
  height: 100vh;
  background-color: #2c3e50;
  color: #ecf0f1;
  padding: 20px;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
  overflow-y: auto;
}

.sidebar-title {
  font-size: 24px;
  margin-bottom: 30px;
  text-align: center;
  font-weight: bold;
  color: #1abc9c;
}

.section {
  margin-bottom: 30px;
}

.section h2 {
  font-size: 18px;
  margin-bottom: 10px;
  border-bottom: 1px solid #34495e;
  padding-bottom: 5px;
  color: #bdc3c7;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  padding: 8px 12px;
  margin-bottom: 6px;
  border-radius: 4px;
  cursor: pointer;
  transition: background 0.2s ease;
}

.sidebar li:hover {
  background-color: #34495e;
}

/* Content */
.content {
  margin-left: 260px;
  padding: 30px;
  flex: 1;
}
</style>
