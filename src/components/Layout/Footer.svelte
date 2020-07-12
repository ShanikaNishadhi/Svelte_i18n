<!-- <script>
    import { _ } from '../../services/i18n';
</script>

<style>
    .footer {
        margin-top: 2rem;
        background-color: #ee6e73;
        color: #e98080;
        height: auto;
    }

    .footer :global(a),
    .footer :global(a:active),
    .footer :global(a:hover),
    .footer :global(a:visited) {
        color: #65b6e3;
    }
</style>

<footer class="footer">
    <div class="content has-text-centered">
        <p>
            {@html $_('footer.line1', { phraseUrl: 'https://phrase.com/blog' })}
            {@html $_('footer.line2', {
                svelteUrl: 'https://svelte.dev/',
                bulmaUrl: 'https://bulma.io',
            })}
        </p>
    </div>
</footer> -->


        <footer class="page-footer">
          <div class="container">
            <div class="row">
              <div class="col l6 s12">
                <h5 class="white-text">Footer Content</h5>
                <p class="grey-text text-lighten-4">You can use rows and columns here to organize your footer content.</p>
              </div>
              <div class="col l4 offset-l2 s12">
                <h5 class="white-text">Links</h5>
                <ul>
                  <li><a class="grey-text text-lighten-3" href="#!">Link 1</a></li>
                  <li><a class="grey-text text-lighten-3" href="#!">Link 2</a></li>
                  <li><a class="grey-text text-lighten-3" href="#!">Link 3</a></li>
                  <li><a class="grey-text text-lighten-3" href="#!">Link 4</a></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="footer-copyright">
            <div class="container">
            © 2014 Copyright Text
            <a class="grey-text text-lighten-4 right" href="#!">More Links</a>
            </div>
          </div>
        </footer>