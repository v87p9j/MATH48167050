java c
MATH4816/7050 HOMEWORK 2 (2024-2025 SEMESTER 2)
1. Consider the inequality constrained optimization problem

Is this a convex programming? Also, write down the Lagrangian function for this problem, and find its minimizers and associated Lagrange multipliers.
2. Consider the inequality constrained optimization problem

Is this a convex programming? Also, write down the Lagrangian function for this problem, and find its minimizers and associated Lagrange multipliers.
3. Consider the optimization problem

Let x* be a local minimizer where the LICQ is satisfied, let (λ, µ) be the associated pair of Lagrange multipliers and let Ax∗ be the set of active constraints. Show that the matrix M is PSD, where
M = ZT ∇2xxL(x* , λ, µ)Z,
and Z is the space whose columns span the subspace ker(∇h(x*)T)∩ker(∇gAx∗ (x*)T). In addition, how can we restate the SOSC using the matrix M? (The matrix M is usually called the projected Hessian.)
4. Let v be a vector in Rn and let A ∈ Rm×n with m ≤ n such that rankA = m. Show that the projection of v to the subspace given by Ax = 0 is
v − AT(AAT)−1Av.
(Hint: Consider formulating the problem of finding the projection to an optimization problem.)
5. (This question gives an example showing that in Slater’s condition, you must require that h is linear and g is concave, instead of the feasible set is convex.) Consider the constrained optimization problem

Does the feasible set convex? Is this a convex programming? Does the feasible set have an interior point? Is it true that all minimizers are KKT points?
6. Show that if x* is a KKT point at which the LICQ holds, then the Lagrange multiplier at x* must be unique.
7. (not required for MATH4816 students, but carefully reading the questions is strongly recommended) We use another approach to show the KKT condition in this question. For simplicity, we consider the optimization problem with inequality constraints only:
(1)

For a given feasible point x of (1), we say a sequence {zk} a feasible sequence if zk ≠ x, limk→∞ xk = x, and zk is feasible for all k big enough. Moreover, we call d a limiting direction of {zk} if there exists a subsequence zk1, zk2, zk3, . . . , such that

(i) Let x* be a local minimizer of (1), and let {zk} be a feasible sequence approaching x*. Show dT ∇f(x∗) ≥ 0 holds for any limiting direction d.
By (i), one gets a necessary condition for x* being a minimizer, that代 写MATH4816/7050 HOMEWORK 2 (2024-2025 SEMESTER 2)Python
代做程序编程语言 all limiting direction of any feasible sequence approaching x* must satisfies dT ∇f(x*) ≥ 0. However, this is useless as there is no way in general to characterize all limiting directions. Fortunately, when LICQ holds, we have d being a limiting direction if and only if (this is why we need LICQ in the KKT system)
(2)
∥d∥ = 1, dT ∇gi(x∗) ≥ 0, ∀ i ∈ Ax∗.
This is shown in [1, Lemma 12.3]. Besides that, we have the following result, which is called Farka’s Lemma:
Lemma 0.1. Let A ∈ Rm×n and let b ∈ Rn. Then bT x ≥ 0 for all x ∈ Rn satisfying Ax ≥ 0 if and only if there exists λ ∈ Rm such that
AT λ = b, λ ≥ 0.
(ii) Now you are ready to show the KKT condition using item (i), equation (2) and Farka’s Lemma. (You don’t need to show (2) and Farka’s Lemma)
8. Let f be a C2function such that ∇2f(x∗) is PD at x∗ ∈ Rn. Show that there exists δ such that for all x ∈ B(x* , δ), ∇2f(x) is PD and ∥(∇2f(x))−1∥ ≤ 2∥(∇2f(x*))−1∥.
9. Implement the Newton’s method, by your hands, to minimize f(x) = 4x21 +x22 − x21x2 with the initial point (1, 1).
10. (coding) Use MATLAB to write a function Netwon method.m that implements the Newton’s method.
Requirements:
1. Your function should have four inputs: the objective function in MATLAB function handle, the initial point x0, the maximum number of iterations max iter, and the accuracy tol.
2. Your function should have three outputs: the computed minimizer x opt, the computed minimum value f opt, the norm of ∇f at the last iterate norm g, and the number of total iterates k.
3. Last, use the command
[x_opt, f_opt, k] = Newton_method(@obj_fun, x_0, max_iter, tol)
to apply your function to minimize the Rosenbrock function f(x) = (1 − x1)2 + 100(x2 − x21)2, with initial points (0, 0),(1, 10),(−100, −100) and the required accu-racy 10−6.
* @obj fun is the function handle for the objective such that for the given input x, it gives three outputs: the function value f at x, the evaluation of gradient g at x, and the evaluation of Hessian H at x. The file obj_fun.m is attached on Moodle and ready to use. You must place it in your directory or add it to your MATLAB path to make it work.
4. You should have your lines of Netwon method.m and the command line for im-plementing Newton’s method submitted. If you really don’t want to use MATLAB, python or julia are also acceptable, given that all requirements above are met.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
