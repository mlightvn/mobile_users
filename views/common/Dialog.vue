<template>
    <view class="btn">
        <button
            :on-press="onPressLearnMore"
            title="Learn More"
            color="white"
            accessibility-label="Learn more about this orange button"
        />
    </view>
</template>

<script>
import { Alert } from 'react-native';

export default {
    methods: {
        onPressLearnMore: function() {
            Alert.alert(
                'Alert Title',
                'My Alert Msg',
                [
                    {text: 'Ask me later', onPress: () => console.log('Ask me later pressed')},
                    {text: 'Cancel', onPress: () => console.log('Cancel Pressed'), style: 'cancel'},
                    {text: 'OK', onPress: () => console.log('OK Pressed')},
                ],
                { cancelable: false }
            );
        }
    }
}
</script>

<style scoped>
.btn{
    color: white;
    background-color: chocolate;
}
</style>