<template>
    <div class="component-footer">
        <div class="container">
            <div
                :class="!isPC ? 'flex-wrap' : ''"
                class="footer-content flex justify-between"
            >
                <div
                    :class="!isPC ? 'flex-wrap' : ''"
                    class="footer-left inline-flex"
                >
                    <div
                        v-for="(i, j) in linkList"
                        :key="j"
                        class="footer-item"
                    >
                        <p class="title">{{ i.name }}</p>

                        <p
                            v-for="(x, y) in i.list"
                            :key="y"
                        >
                            <a :href="x.link">{{ x.name }}</a>
                        </p>
                    </div>
                </div>

                <div class="footer-right">
                    <img
                        src="~/assets/image/logo.png"
                        alt="logo"
                    >
                </div>
            </div>

            <div
                :class="!isPC ? 'flex-wrap' : ''"
                class="footer-foot flex justify-between align-items"
            >
                <div
                    :class="!isPC ? 'justify-between' : ''"
                    class="footer-left flex"
                >
                    <img
                        src="~/assets/image/footer/share-01.png"
                        alt="share"
                    >
                    <img
                        src="~/assets/image/footer/share-02.png"
                        alt="share"
                    >
                    <img
                        src="~/assets/image/footer/share-03.png"
                        alt="share"
                    >
                    <img
                        src="~/assets/image/footer/share-04.png"
                        alt="share"
                    >
                    <img
                        src="~/assets/image/footer/share-05.png"
                        alt="share"
                    >
                    <img
                        src="~/assets/image/footer/share-06.png"
                        alt="share"
                    >
                </div>

                <div class="footer-right">
                    <p>Git ??? Software Freedom Conservancy ??????????????????GitLab ??? GitLab B.V.???????????????????????????????????????????????????GitLab??????</p>
                    <p>???ICP???2021008419???-1</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';

@Component
export default class FooterComponent extends Vue {
    isPC = false;

    linkList: Array<any> = [];

    created() {
        this.getLinkList();
    }

    mounted() {
        this.isPC = document.body.clientWidth > 768;
    }

    getLinkList() {
        this.linkList = [
            {
                name: '????????????',
                list: [
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/services/',
                    },
                    {
                        name: '?????????????????????',
                        link: 'https://gitlab.cn/enterprise/',
                    },
                    {
                        name: 'CI/CD',
                        link: 'https://gitlab.cn/stages-devops-lifecycle/continuous-integration/',
                    },
                    {
                        name: '???????????????',
                        link: 'https://gitlab.cn/stages-devops-lifecycle/source-code-management/',
                    },
                    {
                        name: 'Auto DevOps',
                        link: 'https://gitlab.cn/stages-devops-lifecycle/auto-devops/',
                    },
                    {
                        name: 'DevSecOps',
                        link: 'https://gitlab.cn/solutions/dev-sec-ops/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/solutions/agile-delivery/',
                    },
                    {
                        name: '???????????????',
                        link: 'https://gitlab.cn/solutions/value-stream-management/',
                    },
                    {
                        name: 'GitOps',
                        link: 'https://gitlab.cn/solutions/gitops/',
                    },
                    {
                        name: '??????',
                        link: 'https://gitlab.cn/pricing/',
                    },
                ],
            },
            {
                name: '??????',
                list: [
                    {
                        name: '??????',
                        link: 'https://docs.gitlab.cn/',
                    },
                    {
                        name: '??????',
                        link: 'https://gitlab.cn/community/',
                    },
                    {
                        name: '??????',
                        link: 'https://forum.gitlab.cn/',
                    },
                    {
                        name: '??????',
                        link: 'https://gitlab.cn/blog/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/services/education/',
                    },
                    {
                        name: '??????????????????',
                        link: 'https://gitlab.cn/solutions/open-source/',
                    },
                    {
                        name: '??????????????????',
                        link: 'https://gitlab.cn/solutions/open-source/partners/',
                    },
                    {
                        name: '?????????????????????',
                        link: 'https://gitlab.cn/solutions/startups/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/solutions/education/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/install/',
                    },
                ],
            },
            {
                name: '??????',
                list: [
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/support/',
                    },
                    {
                        name: '??????????????????',
                        link: 'https://gitlab.cn/partners/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/get-help/',
                    },
                ],
            },
            {
                name: '????????????',
                list: [
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/company/',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/company/contact',
                    },
                    {
                        name: '????????????',
                        link: 'https://gitlab.cn/press/',
                    },
                    {
                        name: '?????????????????????GitLab???',
                        link: 'https://gitlab.cn/is-it-any-good/',
                    },
                    {
                        name: '?????? Handbook',
                        link: 'https://gitlab.cn/handbook/',
                    },
                ],
            },
        ];
    }
}
</script>

<style lang="scss">
@import '@/assets/styles/home/footer.scss';
</style>
