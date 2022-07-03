<template>
    <div class="course-card">
        <div class="img">
            <img :src="imgUrl" alt="">
            <h6 class="price"> <span :class="{'d-none' : !isPriceNumber}">$</span>{{price}}<span class="cents" :class="{'d-none' : !isPriceNumber}">{{priceCents}}</span></h6>
        </div>
        <div class="text">
            <div class="teacher d-flex align-items-center gap-3">
                <img :src="teacherImgUrl" alt="">
                <p>{{teacherName}}</p>
            </div>
            <h5>{{courseTitle}}</h5>
            <div class="data d-flex">
                <p><i class="fa-regular fa-file-lines"></i>{{lessonsNum + ' Lessons'}}</p>
                <p><i class="fa-regular fa-user"></i>{{studentsNum + ' Students'}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        imgUrl: String,
        price: String,
        priceCents: {
            type: String,
            default: ".00"
        },
        isPriceNumber: Boolean,
        teacherImgUrl: String,
        teacherName: String,
        courseTitle: String,
        lessonsNum: String,
        studentsNum: String
    }
}
</script>

<style scoped lang="scss">
.course-card{
    cursor: pointer;
    border-radius: 0.5rem;
    overflow: hidden;
    text-align: left;
    &:hover{
        background: var(--white);
        box-shadow: 0 1rem 2rem rgba(0,0,0,0.1);
    }
    .img{
        width: 100%;
        position: relative;
        img{
            width: 100%;
        }
        .price{
            position: absolute;
            top: 0;
            right: 0;
            padding: 0.5rem;
            background: var(--jungle-green);
            color: var(--white);
            font-weight: 600;
            border-bottom-left-radius: 0.3rem;
            .cents{
                font-size: 0.9rem;
            }
        }
    }

    .text{
        padding: 1.5rem;
        .teacher{
            padding: 0.5rem 0;
            img{
                max-width: 40px;
                border-radius: 50%;
            }

            p{
                padding: 0;
                margin: 0;
            }
        }
        h5{
            font-weight: 600;
            padding: 0.5rem 0;
        }
        .data{
            padding: 1rem 0;
            p{
                padding-right: 2.5rem;
                i{
                    padding-right: 0.5rem;
                }
            }
        }
    }
}
</style>