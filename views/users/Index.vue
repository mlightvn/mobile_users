<template>
    <view>
        <flat-list
            :data="list"
            :render-item="(item) => renderList(item)"
        />
         <activity-indicator v-if="false" size="large" color="#0000ff" />
    </view>
</template>

<script>
import React from 'react';
import {Text} from 'react-native';

export default {
    data() {
        return {
            list: [
                {id: 1, name: "Nguyen Ngoc Nam", email: "nam@mlight.vn"},
                {id: 2, name: "美人1", email: "bijin1@mlight.vn"},
                {id: 3, name: "美人2", email: "bijin2@mlight.vn"},
                {id: 4, name: "美人3", email: "bijin3@mlight.vn"},
            ]
        }
    },
    methods: {
        renderList: function(item) {
            return (<Text>{item.item.id} | {item.item.name} | {item.item.email}</Text>)
        }
    },
}
</script>