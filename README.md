# Verify domain on Bluesky using GitHub Pages

Scenario: you have an apex domain but no web server and for some reason you are 
unable to use the DNS verification method (e.g: TXT records aren't support, 
underscores aren't supported, Bluesky doesn't seem to be able to verify your 
records). The instructions that follow enable domain verification using GitHub
Pages in this rare situation.

1. Create a new GitHub repository from this template
2. Modify the contents of `.well-known/atproto-did` to contain your `did`
3. Via your repository settings go to Pages then select the "main" branch to deploy from
4. Add your domain (e.g: example.com)
5. Via your DNS records manager, [point your domain to GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) either an `A` record to `185.199.108.153` or a `ALIAS/CNAME` with `username.github.io`

After a few minutes, your domain will become active and it can be added to Bluesky.
