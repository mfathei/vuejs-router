<template>
    <div>
        <h3>Some User Details</h3>
        <p>User loaded id : {{ $route.params.id }}</p>
        <router-link tag="button" 
        :to="{ name: 'editUser', params: { id: $route.params.id} }"
        class="btn btn-primary">Edit User</router-link>
    </div>
</template>