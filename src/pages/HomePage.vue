<template>
    <q-page class="flex flex-center">
        <div style="height: calc(100vh - 100px)">
            <div class="q-mb-xl">
                <q-tabs v-model="tab" dense>
                    <q-tab name="pessoal" label="Pessoal" />
                    <q-tab name="profissional" label="Profissional" />
                    <q-tab name="todos" label="Todos" />
                </q-tabs>
            </div>

            <div class="q-mb-lg">
                <div class="text-center text-h6 q-pt-md">
                    Criar Tarefa
                </div>
                <q-input rounded outlined dense v-model="todo">
                    <template v-slot:append>
                        <q-btn rounded color="primary" size="sm" label="Criar" @click="createTodo(todo)" />
                    </template>
                </q-input>
            </div>

            <div>
                <q-tab-panels v-model="tab">
                    <q-tab-panel name="pessoal">
                        <div class="text-h6">Pessoal</div>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    </q-tab-panel>

                    <q-tab-panel name="profissional">
                        <div class="text-h6">Profissional</div>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    </q-tab-panel>

                    <q-tab-panel name="todos">
                        <div class="text-h6">Todos</div>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    </q-tab-panel>
                </q-tab-panels>
            </div>
        </div>
    </q-page>
</template>

<script>
export default {
    name: "HomePage",

    data() {
        return {
            tab: "pessoal",
            todo: "",
            todoList: [],
        };
    },

    methods: {
        createTodo(val){
            this.todoList.push(val);
        }
    },
};
</script>

<style lang="scss" scoped></style>
