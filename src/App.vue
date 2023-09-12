<script setup>
import { BryntumScheduler } from "@bryntum/scheduler-vue-3";
import { reactive } from "vue";
import { ref, watch } from "vue";

const config = reactive({
  startDate: new Date(2024, 0, 1, 6),
  endDate: new Date(2024, 0, 1, 20),
  viewPreset: "hourAndDay",
  eventColor: "green",
  rowHeight: 50,
  columns: [
    { text: "Name", field: "name", width: 130 },
    { text: "Age", field: "age", width: 50 },
  ],
  eventEditFeature: {
    // Start disabled
    disabled: true,
  },
  events: [
    {
      id: 1,
      resourceId: 1,
      startDate: new Date(2024, 0, 1, 10),
      endDate: new Date(2024, 0, 1, 12),
      name: "Click me",
      iconCls: "b-fa b-fa-mouse-pointer",
    },
    {
      id: 2,
      resourceId: 2,
      startDate: new Date(2024, 0, 1, 12),
      endDate: new Date(2024, 0, 1, 13, 30),
      name: "Drag me",
      iconCls: "b-fa b-fa-arrows-alt",
    },
    {
      id: 3,
      resourceId: 3,
      startDate: new Date(2024, 0, 1, 14),
      endDate: new Date(2024, 0, 1, 16),
      name: "Double click me",
      eventColor: "purple",
      iconCls: "b-fa b-fa-mouse-pointer",
    },
    {
      id: 4,
      resourceId: 4,
      startDate: new Date(2024, 0, 1, 8),
      endDate: new Date(2024, 0, 1, 11),
      name: "Right click me",
      iconCls: "b-fa b-fa-mouse-pointer",
    },
    {
      id: 5,
      resourceId: 5,
      startDate: new Date(2024, 0, 1, 15),
      endDate: new Date(2024, 0, 1, 17),
      name: "Resize me",
      iconCls: "b-fa b-fa-arrows-alt-h",
    },
    {
      id: 6,
      resourceId: 6,
      startDate: new Date(2024, 0, 1, 16),
      endDate: new Date(2024, 0, 1, 19),
      name: "Important meeting",
      iconCls: "b-fa b-fa-exclamation-triangle",
      eventColor: "red",
    },
    {
      id: 7,
      resourceId: 6,
      startDate: new Date(2024, 0, 1, 6),
      endDate: new Date(2024, 0, 1, 8),
      name: "Sports event",
      iconCls: "b-fa b-fa-basketball-ball",
    },
    {
      id: 8,
      resourceId: 7,
      startDate: new Date(2024, 0, 1, 9),
      endDate: new Date(2024, 0, 1, 11, 30),
      name: "Dad's birthday!",
      iconCls: "b-fa b-fa-birthday-cake",
      style: "background-color : teal; font-size: 18px",
    },
  ],
  resources: [
    { id: 1, name: "Mike", age: 25, meta: { job: "Developer" } },
    { id: 2, name: "Linda", age: 26, meta: { job: "Developer" } },
    { id: 3, name: "Don", age: 34, meta: { job: "Designer" } },
    { id: 4, name: "Karen", age: 22, meta: { job: "Developer" } },
    { id: 5, name: "Doug", age: 29, meta: { job: "Developer" } },
    { id: 6, name: "Peter", age: 25, meta: { job: "Designer" } },
    { id: 7, name: "Sam", age: 54, meta: { job: "Project Manager" } },
    { id: 8, name: "Melissa", age: 29, meta: { job: "Developer" } },
    { id: 9, name: "John", age: 21, meta: { job: "Designer" } },
    { id: 10, name: "Ellen", age: 32, meta: { job: "Developer" } },
  ],
});
</script>

<template>
  <BryntumScheduler v-bind="config" />
</template>
