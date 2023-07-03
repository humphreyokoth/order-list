
<template>
    <div id="app">
        <div class="text-uppercase text-bold">id selected:{{ selected }}</div>
        <table class="table table-striped table-hover">
            <thead>
                <tr>
                    <th><label class="form-checkbox">
                            <input type="checkbox" v-model="selectAll" @click="select">
                            <i class="form-icon"></i>
                        </label></th>
                    <th>id</th>
                    <th>name</th>
                    <th>email</th>

                </tr>
            </thead>
            <tbody>
                <tr v-for="i in items">
                    <td>
                        <label class="form-checkbox">
                            <input type="checkbox" :value="i.id" v-model="selected">
                            <i class="form-icon"></i>
                        </label>
                    </td>
                    <td>{{ i.id }}</td>
                    <td>{{ i.name }}</td>
                    <td>{{ i.email }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>