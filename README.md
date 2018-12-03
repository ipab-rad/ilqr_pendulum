# ilqr_pendulum
ILQR implementation (following [Tassa et al - IROS 1012](https://homes.cs.washington.edu/~todorov/papers/TassaIROS12.pdf)) for gym pendulum environment, using both known model and linear Gaussian dynamic model learning ([Levine et al - JMLR 2016](https://arxiv.org/pdf/1504.00702.pdf)).

* [gaussian_model_learner.ipynb](gaussian_model_learner.ipynb) shows how to learn a conditionally linear Gaussian dynamics model by fitting a joint Gaussian to state action pairs.

* [ilqr.ipynb](ilqr.ipynb) is an ILQR implementation for a kinematic motion model of a wheeled mobile robot.

* [ilqr-gym.ipynb](ilqr-gym.ipynb) is an ILQR implementation for an OpenAI gym inverted pendulum, given a known dynamics model.

* [ilqr_model_learner.ipynb](ilqr_model_learner.ipynb) is an ILQR implementation for an OpenAI gym inverted pendulum, which attempts to learn the dynamics using motor babbling to fit a set of linear Gaussian dynamics models, as in the guided policy search paper. This works pretty poorly, as local linear models make it hard to plan ahead for a longer horizon, and it can be hard to gather data in terminal pendulum positions.

## Requires

* [autograd](https://pypi.org/project/autograd/)
* [openai gym pendulum environment](https://github.com/openai/gym/wiki/Pendulum-v0)
