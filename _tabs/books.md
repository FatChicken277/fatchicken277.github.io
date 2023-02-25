---
layout: page
icon: fas fa-book
order: 3
---

<details>
    <summary>How to download the books (free)</summary>
    <br>
    <iframe class="embed-video youtube lazyloaded" src="https://www.youtube.com/embed/e4yeggrTfDo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>
    <p>Link: <a>https://libgen.is/</a></p>
</details>

---

> Use the **ISBN** code instead of the book name to download it
{: .prompt-tip }

<div>
    <!-- Security as Code -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book1-min.png" width="100%">
        </div>
        <div class="book-content">
            <div>
                <h2>Security as Code</h2>
                <ul>
                    <li><b>By: </b>BK Sarthak Das, Virginia Chu</li>
                    <li><b>ISBN: </b><isbn>9781098127466</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, DevSecOps, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Kubernetes Security and Observability -->
    <div class="book-card"> 
        <div class="book-img">
            <img src="/assets/img/books/book2-min.png" width="100%">
        </div>
        <div class="book-content">
            <div>
                <h2>Kubernetes Security and Observability</h2>
                <ul>
                    <li><b>By: </b>Brendan Creane, Amit Gupta</li>
                    <li><b>ISBN: </b><isbn>9781098107109</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, DevSecOps, Cybersecurity, Kubernetes</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Practical Cloud Security -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book3-min.png" width="100%">
        </div>
        <div class="book-content">
            <div>
                <h2>Practical Cloud Security</h2>
                <ul>
                    <li><b>By: </b>Chris Dotson</li>
                    <li><b>ISBN: </b><isbn>9781492037514</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, Cloud, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- DevOpsSec -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book4-min.png" width="100%">
        </div>
        <div class="book-content">
            <div>
                <h2>DevOpsSec</h2>
                <ul>
                    <li><b>By: </b>Jim Bird</li>
                    <li><b>ISBN: </b><isbn>9781491958995</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, DevSecOps, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Securing DevOps -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book5-min.png" width="100%">
        </div>
        <div class="book-content">
            <div>
                <h2>Securing DevOps: Security in the Cloud</h2>
                <ul>
                    <li><b>By: </b>Julien Vehent</li>
                    <li><b>ISBN: </b><isbn>9781617294136</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, DevSecOps, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Agile Application Security -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book6-min.png" width="100%">
        </div>
        <div class="book-content">  
            <div>
                <h2>Agile Application Security</h2>
                <ul>
                    <li><b>By: </b>Laura Bell, Michael Brunton-Spall, Rich Smith, Jim Bird</li>
                    <li><b>ISBN: </b><isbn>9781491938799</isbn></li>
                    <li><b>Tags: </b><bt>Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Container Security -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book7-min.png" width="100%">
        </div>
        <div class="book-content">  
            <div>
                <h2>Container Security</h2>
                <ul>
                    <li><b>By: </b>Liz Rice</li>
                    <li><b>ISBN: </b><isbn>9781492056706</isbn></li>
                    <li><b>Tags: </b><bt>Docker, Kubernetes, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Hands-On Security in DevOps -->
    <div class="book-card">
        <div class="book-img">
            <img src="/assets/img/books/book8-min.png" width="100%">
        </div>
        <div class="book-content">  
            <div>
                <h2>Hands-On Security in DevOps</h2>
                <ul>
                    <li><b>By: </b>Tony Hsu</li>
                    <li><b>ISBN: </b><isbn>9781788995504</isbn></li>
                    <li><b>Tags: </b><bt>DevOps, DevSecOps, Cybersecurity</bt></li>
                </ul>
            </div>
        </div>
    </div>
</div>

<style>
    details {
        padding: 1rem;
    }

    .book-card {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
        grid-gap: 0 5%;

        background-color: var(--search-wrapper-bg);
        border-radius: 10px;
        padding: 2rem;
        margin: 1rem;
    }

    .book-card h1, h2, h3, h4 {    
        margin: 0;
    }

    .book-img {
        display: flex;
        justify-content: center;
    }

    .book-card img {
        padding: 0;
    }

    .book-content {
        padding: 1rem 0;
        text-align: left;
    }

    .book-isbn {
        color: var(--prompt-danger-icon-color);
    }

    isbn {
        color: red;
    }

    bt {
        color: var(--text-muted-color);
        font-style: italic;
    }

    /* mobile */
    @media (max-width: 425px) {
        .book-card {
            grid-template-columns: repeat(auto-fit, minmax(50vw, 1fr));
        }
    }
</style>