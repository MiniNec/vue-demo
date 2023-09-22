<script setup lang="ts">
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue';

const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>

<template>
  <el-container>
    <el-header>Header</el-header>
    <el-container>
      <el-aside width="200px">
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
        >
          <el-sub-menu index="1">
            <template #title>
              <el-icon><location /></el-icon>
              <span>菜单1</span>
            </template>
            <el-menu-item-group title="组1">
              <el-menu-item index="1-1">子菜单1-1</el-menu-item>
              <el-menu-item index="1-2">子菜单1-2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group title="组2">
              <el-menu-item index="1-3">子菜单1-3</el-menu-item>
            </el-menu-item-group>
            <el-sub-menu index="1-4">
              <template #title>子菜单1-4</template>
              <el-menu-item index="1-4-1">子菜单1-4-1</el-menu-item>
            </el-sub-menu>
          </el-sub-menu>
          <el-menu-item index="2">
            <el-icon><icon-menu /></el-icon>
            <span>菜单2</span>
          </el-menu-item>
          <el-menu-item index="3" disabled>
            <el-icon><document /></el-icon>
            <span>菜单3</span>
          </el-menu-item>
          <el-menu-item index="4">
            <el-icon><setting /></el-icon>
            <span>菜单4</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<style scoped></style>
