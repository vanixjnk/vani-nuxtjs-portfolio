<template>
    <div class="content-vh">
        <div class="content">
            <a-typography-title style="font-weight: bold; font-size: 40px;">
                Let's Get in Touch:
                <span style="color: #1677FF;">Ways to Connect with Me</span>
            </a-typography-title>
            <a-typography-paragraph>
                Cảm ơn bạn đã quan tâm đến việc liên hệ với tôi. Tôi hoan nghênh phản hồi, câu hỏi và đề xuất của bạn. Nếu bạn có câu hỏi hoặc nhận xét cụ thể, vui lòng gửi email trực tiếp cho tôi theo địa chỉ <span style="color: #1677FF">{{ content.email }}</span>. Tôi cố gắng trả lời tất cả tin nhắn trong vòng 24 giờ, mặc dù tôi có thể mất nhiều thời gian hơn trong thời gian bận rộn. Cuối cùng, nếu bạn muốn kết nối trên mạng xã hội, bạn có thể kết nối với tôi bằng các liên kết mạng xã hội bên dưới.
            </a-typography-paragraph>

            <a :href="content.social_links.facebook" target="_blank">
                <a-button type="text">
                    <facebook-outlined /> Follow on Facebook
                </a-button>
            </a>

            <br />

            <a :href="content.social_links.instagram" target="_blank">
                <a-button type="text">
                    <instagram-outlined /> Follow on Instagram
                </a-button>
            </a>

            <br />

            <a :href="content.social_links.twitter" target="_blank">
                <a-button type="text">
                    <twitter-outlined /> Follow on Twitter
                </a-button>
            </a>

            <br />

            <a-divider></a-divider>

            <a :href="'mailto:' + content.email">
                <a-button type="text">
                    <mail-outlined /> vanixjnk@gmail.com
                </a-button>
            </a>
        </div>
    </div>
</template>

<script setup lang="ts">
import content from '~/static/content.json';

useHead({
    title: "Contact",
})
</script>

<style scoped>
.ant-typography {
    font-size: 16px;
}

.ant-btn {
    font-size: 16px;
}

.anticon {
    color: #1677FF;
}

.content {
    width: 100%;
}

/* lg */
@media (min-width: 1024px) {
    .content {
        width: 80%;
    }
}
</style>