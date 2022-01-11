# blog_rmarkdown

Using some Rmd documents build a blog website.

Remake all blog articles using below code:

```{r}
### even render_site(i) have error, such as
# Error in file.exists(in_file) : 
#   file name conversion problem -- name too long?
### can go on to make next
## this only make several html files in blog_rmarkdown dir
for(i in list.files('.', pattern = 'md$')) {
  try(rmarkdown::render_site(i))
}
```


tips:

+ OpenSSL SSL_read: Connection was reset, errno 10054
`git config --global http.sslVerify "false"`

+ Failed to connect to github.com port 443: Timed out
`git config --global --unset http.proxy`

+ warning:LF will be replaced by CRLF the file will have its original line endings in your working directory
`git config --global core.autocrlf true`

+ docs folder must have file .nojekyll


