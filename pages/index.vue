<template>
    <div class="content-vh">
        <a-flex gap="50" horizontal justify="center" align="center">
            <div class="profile-info">

                <!-- Info -->
                <a-typography-title :level="4" style="margin: 0">
                    {{ content.role }}
                </a-typography-title>
                <a-typography-title :level="1" style=" margin: 0 0 10px 0; font-weight: bold;">
                    {{ content.name }}
                </a-typography-title>
                <a-typography-paragraph align="justify" style="font-size: 16px; color: #71717a;">
                    {{ content.description }}
                </a-typography-paragraph>

                <!-- Buttons -->
                <a-flex gap="8" style="margin-top: 25px;">
                    <NuxtLink to="/about">
                        <a-button type="primary">More About Me
                            <RightOutlined />
                        </a-button>
                    </NuxtLink>
                </a-flex>
            </div>
        </a-flex>
    </div>
</template>

<script setup lang="ts">
import content from '~/static/content.json';
</script>

<style scoped>
.profile-image {
    display: none;
    rotate: 4deg;
}

.sm-profile-image {
    border-radius: 100%;
    margin-bottom: 18px;
}

:deep(.ant-image-mask) {
    border-radius: 15px;
}

.content-vh {
    padding-top: 85px !important;
}

/* lg */
@media (min-width: 768px) {
    .profile-info {
        width: 60%;
    }

    .profile-image {
        display: block;
    }

    .sm-profile-image {
        display: none;
    }

    .content-vh {
        padding-top: 0 !important;
    }
}
</style>