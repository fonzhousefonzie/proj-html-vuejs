<template>
    <header>
        <div class="container d-flex justify-content-between align-items-center py-4">
            <img src="../assets/img/dark-logo.png" alt="Max Coach Logo">
            <div class="menu d-flex gap-1">
                <ul class="menu-links d-flex list-unstyled gap-4">
                    <li v-for="item in menu" :key="item.name">{{ item.name }} <i class="fa fa-solid fa-angle-down"></i>
                        <ul class="dropdown list-unstyled">
                            <li v-for="link in item.links" :key="link">{{ link }}</li>
                        </ul>
                    </li>
                </ul>
                <ul class="icons d-flex list-unstyled gap-4">
                    <li><i class="fa fa-solid fa-cart-shopping"></i></li>
                    <li><i class="fa-regular fa-circle-user me-3"></i></li>
                </ul>
                <div class="search">
                    <input type="text" placeholder="Search...">
                    <i class="fa fa-solid fa-magnifying-glass"></i>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            menu: {
                home: {
                    name: 'Home',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                },
                pages: {
                    name: 'Pages',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                },
                courses: {
                    name: 'Courses',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                },
                features: {
                    name: 'Features',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                },
                blog: {
                    name: 'Blog',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                },
                shop: {
                    name: 'Shop',
                    links: {
                        link1: 'link1',
                        link2: 'link2',
                        link3: 'link3'
                    }
                }
            }
        }
    }
}
</script>

<style lang="scss" scoped>
header {
    background: var(--main-bg);
    color: var(--main-color);

    .container {

        img {
            max-height: 2rem;
        }

        .menu-links,
        .icons,
        .search {
            margin-bottom: 0;
            align-items: center;

            li {
                padding: 0.5rem 0;
                cursor: pointer;
            }
        }

        .search {
            position: relative;

            i {
                position: absolute;
                right: 1rem;
                top: 50%;
                transform: translateY(-50%);
                color: var(--green);
            }
        }

        .menu-links li {
            position: relative;

            ul {
                display: none;
                position: absolute;
                top: 100%;
                right: 0;
                background: var(--main-bg);
                border: 1px solid var(--blue);
                padding: 0.5rem 0;
                color: var(--main-color);

                li {
                    padding: 0.5rem 2rem;
                    cursor: pointer;

                    &:hover {
                        background: var(--white);
                        color: var(--blue);
                    }
                }
            }

            &:hover {
                color: var(--blue);
                ul {
                    display: block;
                }
            }
        }
    }


}
</style>