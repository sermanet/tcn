# Time-Contrastive Networks:<br> Self-Supervised Learning from Multi-View Observation
Pierre Sermanet\*, Corey Lynch\*†, Jasmine Hsu, Sergey Levine<br>
Google Brain<br>
(* equal contributions, † Google Brain Residency program [g.co/brainresidency](https://research.google.com/teams/brain/residency/))

### [[ Paper ]](https://arxiv.org/abs/1704.06888) [[ Video ]](https://www.youtube.com/watch?v=sErz1jyhTXk)

<a href="http://www.youtube.com/watch?feature=player_embedded&v=sErz1jyhTXk" target="_blank">
 <img src="figs/youtube_front.png" alt="TCN" width="480">
</a>

##### Abstract
We propose a self-supervised approach for learning representations entirely from unlabeled videos recorded from multiple viewpoints. This is particularly relevant to robotic imitation learning, which requires a viewpoint-invariant understanding of the relationships between humans and their environment, including object interactions, attributes and body pose. We train our representations using a triplet loss, where multiple simultaneous viewpoints of the same observation are attracted in the embedding space, while being repelled from temporal neighbors which are often visually similar but functionally different. This signal encourages our model to discover attributes that do not change across viewpoint, but do change across time, while ignoring nuisance variables such as occlusions, motion blur, lighting and background. Our experiments demonstrate that such a representation even acquires some degree of invariance to object instance. We demonstrate that our model can correctly identify corresponding steps in complex object interactions, such as pouring, across different videos with different instances. We also show what is, to the best of our knowledge, the first self-supervised results for end-to-end imitation learning of human motions by a real robot.

# Unsupervised Objects Interactions

### Training Sequences
<img src='figs/pouring_data.mov.gif' height='270'>

### Semantic Alignment / Nearest Neighbor Imitation
<img src='figs/pouring_human.mov.gif'>

### 'Fake' pouring imitation
<img src='figs/pouring_fake.mov.gif' height='270'>

### Imitation Errors
<img src='figs/pouring_failure.mov.gif' height='270'>

### Robotic Imitation (end-effector never seen during training)
<img src='figs/pouring_robot.mov.gif' height='270'>

# End-to-End Self-Supervised Pose Imitation

### Self-supervised only (no labels)
<img src='figs/pose_atomic.mov.gif' height='270'>

### Complex non-linear mapping discovered unsupervised
<img src='figs/pose_squat.mov.gif' height='270'>

### Imitation Failures (shoulder joint)
<img src='figs/pose_failures.mov.gif' height='270'>

### Self-supervision + human supervision
<img src='figs/pose_jeff_long.mov.gif' height='270'>

# Citation

```
@article{TCN2017,
  title={Time-Contrastive Networks: Self-Supervised Learning from Multi-View Observation},
  author={Sermanet, Pierre and Lynch, Corey and Hsu, Jasmine and Levine, Sergey},
  journal={arXiv preprint arXiv:1704.06888},
  year={2017}
}
```

# Acknowledgments

We thank Jonathan Tompson, James Davidson and Vincent Vanhoucke for helpful discussions and feedback. We are also grateful to Eric Jang and Phing Lee for their repeated help and talent in robot imitation. Finally we thank everyone else who provided imitations for this project: Alexander Toshev, Anna Goldie, Deanna Chen, Deirdre Quillen, Dieterich Lawson, Eric Langlois, Ethan Holly, Irwan Bello, Jasmine Collins, Jeff Dean, Julian Ibarz, Ken Oslund, Laura Downs, Leslie Phillips, Luke Metz, Mike Schuster, Ryan Dahl, Sam Schoenholz and Yifei Feng.
