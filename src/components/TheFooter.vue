<template>
    <footer class="pt-3 pb-4">
        <div class="container d-flex text-start py-5">
            <div class="address col-50">
                <h6>Address</h6>
                <ul>
                    <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
                    <li>+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
                    <li>support@maxcoach.com</li>
                    <div class="social d-flex gap-3">
                        <i class="fa fa-brands fa-facebook-square"></i>
                        <i class="fa fa-brands fa-twitter"></i>
                        <i class="fa fa-brands fa-instagram"></i>
                        <i class="fa fa-brands fa-linkedin"></i>
                    </div>
                </ul>
            </div>
            <div class="links col-50 d-flex">
                <div class="explore">
                    <h6>Explore</h6>
                    <ul>
                    <li><a href="#">Start here</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">About us</a></li>
                    </ul>
                </div>
                <div class="explore-2">
                    <ul>
                    <li><a href="#">Success story</a></li>
                    <li><a href="#">Courses</a></li>
                    <li><a href="#">Contact us</a></li>
                    </ul>
                </div>
                <div class="information">
                    <h6>Information</h6>
                    <ul>
                    <li><a href="#">Membership</a></li>
                    <li><a href="#">Purchase guide</a></li>
                    <li><a href="#">Privacy policy</a></li>
                    <li><a href="#">Terms of services</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2020 Maxcoach. All Rights Reserved</p>
        </div>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
footer{
    background: var(--white);
}

h6{
  font-weight: bold;
  }

    ul{
        list-style: none;
        padding: 0;
        li{
            padding: 0.5rem 0;
        }
    }

    i{
        padding: 1rem 1rem 0 0;
        font-size: 1.5rem;
        color: var(--green);
    }

    .links{
        gap: 5rem;
        padding-bottom: 2rem;
    }

    .explore-2{
        padding-top: 1.9rem;
    }

    .copyright{
        color: var(--jungle-green);
        font-weight: 600;
        font-size: 0.9rem;
        padding: 0.5rem;
    }
</style>