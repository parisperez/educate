<template>
    <Layout>
        <div class="card content-box">
            <div class="card__content">
                <h1>About 'Educate Your Sons Campaign'</h1>
                <p class="card__description">
                    “tk</p>
                <h2>tk</h2>
                <p class="card__description">
                    tk
                </p>
                <h2 class="card__description"> 
                    tk
                </h2>
                <p class="card__description">
                    tk
                </p>
                <ul>
                    <li>
                        <a href="tk" target="_blank">tk</a>
                        </li>
                </ul>
                <p class="card__description">
                    tk
                </p>
                <h2 class="card__description"> 
                    Who this blog is for 
                </h2>
                <ul>
                    <li>tk </li>
                    <li>tk</li>
                </ul>
                <h2 class="card__description"> 
                    tk
                </h2>
                <p class="card__description">
                     tk
                </p>
                <p class="card__description">
                    tk
                </p>
            </div>
          </div>
    </Layout>
</template>

<style lang="scss">
    .card {
      margin-bottom: var(--space);
      position: relative;
    
      &__header {
        margin-left: calc(var(--space) * -1);
        margin-right: calc(var(--space) * -1);
        margin-bottom: calc(var(--space) / 2);
        margin-top: calc(var(--space) * -1);
        overflow: hidden;
        border-radius: var(--radius) var(--radius) 0 0;
    
        &:empty {
          display: none;
        }
      }
    
      &__image {
        min-width: 100%;
      }
    
      &__title {
        margin-top: 0;
      }
    
      &:hover {
        transform: translateY(-5px);
        box-shadow: 1px 10px 30px 0 rgba(0,0,0,.1);
      }
    
      &__link {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        opacity: 0.0;
        overflow: hidden;
        text-indent: -9999px;
        z-index: 0;
      }
    }
    </style>
    