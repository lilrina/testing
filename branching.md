https://spin.atomicobject.com/2018/10/10/git-branching-strategy/  by Joe Chrysler

Joe Chrysler's branching strategy calls for a new branch for any change, no matter how small it is. He also advocates for "Rebase Early & Often". He also backs up his branches by adding a new branch or tag before doing rebasing. Joe doesn't follow hard rules on where new branches must be descended from: instead he tries to guess the future in order to decide branch lineage. If his guess goes wrong, he uses more advanced git concepts to clean things up.

Our team didn't consider using this strategy. For one, it makes use of frequent rebasing, and we don't want to use rebasing at all because it isn't permitted for this project and it can obscure the history of a project. However, we are using Joe's idea of creating a new branch of almost any change. This is almost by default: the 3 members of our team who are making changes are all going to make a separate branch for separate, small issues they have identified. We don't need to backup branches because we aren't using Joe's complicated ideas about rebasing. The branches will already exist in the commit history.

https://barro.github.io/2016/02/a-succesful-git-branching-model-considered-harmful/ by Jussi Judin

Jussi uses the "cactus model". The only place a new branch is permitted to start is from the master branch, and the new branches never get merged back in. Feature development takes place on the master branch. Local branches are allowed, but they are short lived and they are frequently rebased 