1-How to clone your Hugo project which has a theme as a Git submodule

cd $HOME/STORE/WEBSITE/

git clone https://github.com/ng0177/theme-iris.git
cd ./theme-iris

#git pull
#git submodule update --init --recursive # fills it up!

2-How to modify theme-iris

git add .
git commit -m "My site"
git remote add origin https://github.com/ng0177/theme-iris.git
git remote -v
git status

3-How to push modifications

git push -u origin master


A-How to add theme-iris as a Git submodule

rm -rf themes/hugo-theme-iris
git rm -r themes/hugo-theme-iris
git submodule add https://github.com/peaceiris/hugo-theme-iris.git ./themes/hugo-theme-iris


B-How to update a theme which is installed as a Git submodule

cd ./themes/hugo-theme-iris
git fetch
git checkout master
#git checkout v0.16.0
#git branch
cd ../..
git add themes/hugo-theme-iris
git commit -m "deps: bump hugo-theme-iris to latest"
git push origin master
