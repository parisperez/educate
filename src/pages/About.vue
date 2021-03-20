<template>
    <Layout>
        <div class="card content-box">
            <div class="card__content">
                <h1>About 'Listen, Portland'</h1>
                <p class="card__description">
                    “A serious flaw of revolutionary movements in the past, has been that primary focus was on dismantling a current system, as opposed to imagining and ultimately creating a new and just society.” - @nowhitesaviors, @djuan___x</p>
                <h2>Purpose of this blog</h2>
                <p class="card__description">
                    To help shift Portland culture from white centrism to multiculturalism. The prerequisite reading listed below have allowed you to create consciousness around your racist behaviors. This blog is focused on turning your anti-racism commitment into actions and behaviors for your every day life. Let's experiment and define the new normal for ourselves and our kiddos. 
                </p>
                <h2 class="card__description"> 
                    Prerequisites
                </h2>
                <p class="card__description">
                    Reading these books are highly recommended to understand context for the views and terms used in this blog:
                </p>
                <ul>
                    <li>
                        <a href="https://www.powells.com/book/white-fragility-9781974923410" target="_blank">White Fragility: Why It's So Hard for White People to Talk About Racism</a>
                        </li>
                    <li>
                        <a href="https://www.powells.com/book/me-and-white-supremacy-9781728216652" target="_blank">Me and White Supremacy: How You Can Combat Racism and Change the World Today</a>
                        </li>
                    <li>
                        <a href="https://www.powells.com/book/the-new-jim-crow-9781595586438" target="_blank">The New Jim Crow: Mass Incarceration in the Age of Colorblindness</a>
                        
                    </li>
                </ul>
                <p class="card__description">
                    If you've done the reading, you will have arrived on the following truth: All Americans harbor racist views, consciously and unconsciously because of the systemic racism that’s persisted since the country’s founding. Without conscious work towards being anti-racist, Americans will default to harmful racist behavior and toxic white-centric perspectives. If you haven't arrived on this truth, read the above books. 
                </p>
                <h2 class="card__description"> 
                    Who this blog is for 
                </h2>
                <ul>
                    <li>Portlanders, especially white Portlanders, who are looking for tools to activate their allyship on a day-to-day basis. </li>
                    <li>Not-white people who regularly must inhabit spaces that are all / predominantly white. </li>
                </ul>
                <h2 class="card__description"> 
                    Who this blog is NOT for 
                </h2>
                <p class="card__description">
                     Overt racists who have not found their way to allyship yet. Anti-racist whites who are reading this, consider yourselves the best people to reach out to your overtly racist white friends, family and coworkers. You ultimately have the most influence. <br><br> I'm not-white and therefore this blog will not be attempting to do this work. Not-white Americans should not bear the emotional burden of dismantling racism at all, and CERTAINLY not on this level. Please don't make them do it. Not-white people have never been the problem. Racism was created by and is perpetuated by the power structure in America that is controlled by whites. Do your work.
                </p>
                <p class="card__description">
                    Thanks for reading. <br><br>
                    - Juno Rodriguez, a summoned mother in PDX
                </p>
                <!-- <p class="card__description">
                    Thanks for reading.<br>
                    Paris
                </p>
                <h2 class="card__description"> 
                    About me
                </h2>
                <ul>
                    <li>Not-White American</li>
                    <li>Mother</li>
                    <li>Female identifying</li>
                    <li>Cisgendered</li>
                    <li>Married</li>
                    <li>Upper middle class</li>
                    <li>Portlander</li>
                    <li>Multiracial family</li>
                    <li>Agnostic</li>
                    <li>Originally from Washington state</li>
                    <li>Previously lived in Boston and Los Angeles</li>
                    <li>Writer</li>
                    <li>Improv comedy performer</li>
                    <li>Technical project manager for web technologies</li>
                    <li>Fluent in two languages</li>
                    <li>Internationally travelled</li>
                    <li>Live in an affluent, multiracial and multicultural neighborhood</li>
                    <li>Grew up in a multiracial but white-centric community</li>
                    <li>Educated in predominantly multiracial but white-centric spaces</li>
                    <li>Experienced higher education in homogeneously not-white spaces</li>
                    <li>Inhabit social circles that are homogeneously not-white as well as all / predominantly white</li>
                    <li>Held management positions at companies that were all women.</li>
                    <li>Held management positions at companies where I was the only not-white person.</li>
                    <li>Held management positions at companies where I was the only woman in management.</li>
                    <li>Held management positions at companies that were white-centric but multiracial.</li>
                    <li>Identify as Gen X but my values align with and are informed most often by millennials.</li>
                    <li>Value multiculturalism and dismantling white capitalism and white-centric American culture.</li>
                </ul> -->
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
    