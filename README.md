heroku create -a api-ade-2020
heroku create -a frontend-ade-2020
heroku buildpacks:add -a api-ade-2020 https://github.com/heroku/heroku-buildpack-multi-procfile
heroku buildpacks:add -a frontend-ade-2020 https://github.com/heroku/heroku-buildpack-multi-procfile
heroku config:set -a api-ade-2020 PROCFILE=api/Procfile
heroku config:set -a frontend-ade-2020 PROCFILE=frontend/Procfile
git push https://git.heroku.com/api-ade-2020.git HEAD:master
git push https://git.heroku.com/frontend-ade-2020.git HEAD:master