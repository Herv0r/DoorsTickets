<script>
  let testimonials = [
    {
      id: 1,
      date: "Mar 16, 2023",
      title: "Increible atención",
      excerpt: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim ven do eiusmod tempor incididunt ut labore et dolore magna aliqua et dolore magna aliqua et dolore magna al Lorem ipsum dolor.",
      author: {
        name: "Michael Foster",
        role: "Co-Founder / CTO",
        image: "https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
      }
    },
    {
      id: 2,
      date: "Mar 16, 2023",
      title: "Increible atención",
      excerpt: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim ven do eiusmod tempor incididunt ut labore et dolore magna aliqua et dolore magna aliqua et dolore magna al Lorem ipsum dolor.",
      author: {
        name: "Michael Foster",
        role: "Co-Founder / CTO",
        image: "https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
      }
    },
    // Más testimonios...
  ];
</script>

<div class="blog-section">
  <div class="blog-content">
    <div class="blog-header">
      <h2 class="blog-title">¿Qué opinan nuestros clientes?</h2>
      <p class="blog-description">Testimonios destacados del mes</p>
      <hr />
    </div>
    <div class="blog-posts">
      {#each testimonials as testimonial (testimonial.id)}
        <article class="blog-post">
          <div class="post-meta">
            <time datetime={testimonial.date} class="post-date">{testimonial.date}</time>
          </div>
          <div class="post-title">
            <h3 class="post-title-text">
              <a href="/">{testimonial.title}</a>
            </h3>
            <p class="post-excerpt">{testimonial.excerpt}</p>
          </div>
          <div class="post-author">
            <img src={testimonial.author.image} alt="" class="author-image" />
            <div class="author-info">
              <p class="author-name">
                <a href="/">{testimonial.author.name}</a>
              </p>
              <p class="author-role">{testimonial.author.role}</p>
            </div>
          </div>
        </article>
      {/each}
    </div>
  </div>
</div>
