## Knowledge Distillation : A detailed survey mainly focusing on knowledge transfer in different scenarios



### 《Privileged Features Distillation at Taobao Recommendation》

The basic idea of distillation: bridge the capacity gap between big teacher model and small student model. Why? Originally for model compression.

Here is a scheme: ==You can train a teacher with extra knowledge, which can not be used by student, and transfer knowledge==(response/feature/relation) to student. Thus, input to teacher/student can be different, teacher gets more input and "digest" rich info then turn into useful info to guide student.

Teacher's model should be stronger, but not that strong. 

Co training tricks. It belongs to ==online distillation==. At early steps teacher may generate info which is not that useful or even false. Force $\lambda$ set to 0 and recover afterwards。

Both coarse-grained ranking(CTR prediction) and fine-grained ranking(CVR prediction) use distillation but they use different extra knowledge for teacher: interaction && post-click.

It's still a binary-classification task，so logits in the last layer is used to force student generate similar logits distribution.



收集整理paper list

哪些数据是knowledge transfer有用。该设计怎样的self-supervised task。

对噪声稳定（
        设计什么样的知识是有效的，普遍的。distance损失的设计。不同层的knowledge设计。如何定义knowledge transfer的效率，以及先验判断哪些知识对应用是有用的。

t/s的：模型不同 输入数据不同 任务甚至不同 怎么知识抽取和关联知识。

pre-train/finetune和distillation

