.. role:: math(raw)
   :format: html latex
..

.. contents::

Statistical Physics
===================

What is information?
--------------------

1. | Information contained in a physical system = **the minimum number
     of yes/no question** you need to get answered to fully specify the
     system.

2. (Information theory) Information is **uncertainty of a probability
   distribution function**. (corresponding to negative information
   entropy)

   For continuous distributions (of which discrete case is a variant),
   information of distribution :math:`w` is

.. math:: I[w]=-H(w)=-\int_{-\infty}^{+\infty}w(x)\log(w(x))dx

 and relative information of :math:`w_2` compared to :math:`w_1` is

.. math:: I[w_2,w_1]=H(w_1)-H(w_2)=I(w_2)-I(w_1)

 or

.. math:: I[w_2,w_1]=\int_{-\infty}^{+\infty}\log \left(\frac{w_1(x)^{w_1(x)}}{w_2(x)^{w_2(x)}}\right)

 **Information as of a mathematical quantity is similar to angle.**

 Compared with the definition of norm:

.. math:: ||w||=\sqrt{\int_{-\infty}^{+\infty}w(x)^2dx}

 distance:

.. math:: D[w_1,w_2]=||w_1-w_2||=\sqrt{\int_{-\infty}^{+\infty}(w_1(x)-w_2(x))^2dx}

 angle:

.. math:: \Phi[w_1,w_2]=\arccos \frac{\int_{-\infty}^{+\infty}w_1(x)w_2(x)dx}{\sqrt{\int_{-\infty}^{+\infty}w_1(x)^2dx}\sqrt{\int_{-\infty}^{+\infty}w_2(x)^2dx}}

 referring to `Statistical distance and Hilbert
space <https://journals.aps.org/prd/pdf/10.1103/PhysRevD.23.357>`__ by
*W. K. Wootters Phys. Rev. D **23**, 357*

 **Extra materials:** `Why is information
indestructible? <https://physics.stackexchange.com/questions/29175/why-is-information-indestructible>`__

Liouville's theorem
-------------------

.. math:: {\partial \rho \over \partial t} =-\{\rho ,\mathcal{H}\} \\ or　　{d \rho \over dt}=0 \\ or　d\Gamma'=d\Gamma

The distribution function is constant along the phase trajectories of
the subsystem.

Prerequisite
~~~~~~~~~~~~

A conservative system: :math:`\mathcal H` does not depend explicitly on
time, and the system is not disturbed by external forces.

Derivations
~~~~~~~~~~~

1. The equation of continuity(the number of microstates):

.. math:: {\partial \rho \over \partial t}+\nabla(\rho \boldsymbol{v})=0

 Hamiltonian canonical equations:

.. math:: \frac{dp_i}{dt} = -\frac{\partial\mathcal{H}}{\partial q_i}\\ \frac{dq_i}{dt} = \frac{\partial\mathcal{H}}{\partial p_i}

1. The Jacobian of canonical transformation is unity.

Interpretations
~~~~~~~~~~~~~~~

1. The conservation of information:

.. math:: I(initial　 state)=I(final　 state)

1. The time evolution of Hamiltonian systems is **a canonical
   transformation** on phase space.

2. The time evolution of Hamiltonian systems **behaves as incompressible
   fluid**.

Consequences
~~~~~~~~~~~~

1. Time reversal symmetry：

   .. math:: \rho(\boldsymbol{p},\boldsymbol{q},t)=\rho(-\boldsymbol{p},\boldsymbol{q},-t)

2. The time evolution of the ensemble average:

   .. math:: {d\langle\mathcal{O}\rangle \over dt}=\langle\{\mathcal{O},\mathcal{H}\}\rangle

Discussion about phase space density and probability density
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**A priori probability** is here (in the case of a continuum)
proportional to the phase space volume element :math:`\Delta q\Delta p`,
and is the number of microstates therein.

Generalization of Liouville's theorem
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. math::

   \frac{ d \rho }{ dt } = \frac{ \partial \rho }{ \partial t } + \dot{\boldsymbol{\Gamma}} \cdot \frac{ \partial \rho }{ \partial \boldsymbol{\Gamma} } 
     = - \left[ \rho \frac{ \partial }{ \partial \boldsymbol{\Gamma} } \cdot \dot{\boldsymbol{\Gamma}} + \dot{\boldsymbol{\Gamma}} \cdot \frac{ \partial \rho }{ \partial \boldsymbol{\Gamma} } \right] + \dot{\boldsymbol{\Gamma}} \cdot \frac{ \partial \rho }{ \partial \boldsymbol{\Gamma} }  
     = - \rho \frac{ \partial }{ \partial \boldsymbol{\Gamma} } \cdot \dot{\boldsymbol{\Gamma}}  
     \equiv - \rho \Lambda\left( \boldsymbol{\Gamma} \right) \

.. math:: or　\frac{ d }{ dt } \ln \lvert \rho \rvert = - \Lambda\left( \boldsymbol{\Gamma} \right)

where :math:`\boldsymbol\Gamma=(\boldsymbol q ,\boldsymbol p)`, and
:math:`\Lambda\left( \boldsymbol{\Gamma} \right)` is the **phase space
compression factor**.

When the equations of motion can be generated from a Hamiltonian, then
:math:`\Lambda\left( \boldsymbol{\Gamma} \right)=0`.

BBGKY hierarchy
---------------

.. math:: {\partial f_{s}\over\partial t}-\{\mathcal{H}_s,f_s\}=\sum_{n=1}^{s} \int dV_{s+1}{\partial \mathcal{V}(\boldsymbol{q_n}-\boldsymbol{q_{s+1}})\over\partial\boldsymbol{q_n}}\cdot{\partial f_{s+1}\over\partial\boldsymbol{p_n}}

with Hamiltonian:

.. math:: \mathcal{H}(\boldsymbol{p},\boldsymbol{q})=\sum_{i=1}^N\left[{\boldsymbol{p_i}^2\over 2m}+U(\boldsymbol{q_i})\right]+{1\over2}\sum_{(i,j)=1}^N\mathcal{V}(\boldsymbol{q_i}-\boldsymbol{q_j})

.. math:: \mathcal{H}=\mathcal{H}_s+\mathcal{H}_{N-s}+\mathcal{H}'\\

.. math:: \mathcal{H}_s=\sum_{n=1}^s\left[{\boldsymbol{p_n}^2\over 2m}+U(\boldsymbol{q_n})\right]+{1\over2}\sum_{(n,m)=1}^s\mathcal{V}(\boldsymbol{q_n}-\boldsymbol{q_m})　(interior)\\ \mathcal{H}_{N-s}=\sum_{i=s+1}^N\left[{\boldsymbol{p_i}^2\over 2m}+U(\boldsymbol{q_i})\right]+{1\over2}\sum_{(i,j)=s+1}^N\mathcal{V}(\boldsymbol{q_i}-\boldsymbol{q_j})　(exterior)\\ \mathcal{H}'=\sum_{n=1}^s\sum_{i=s+1}^{N}\mathcal{V}(\boldsymbol{q_n}-\boldsymbol{q_i})　(interactive)

and with :math:`s`-particle density:

.. math:: f_s(\boldsymbol{p_1},\cdots,\boldsymbol{q_s},t)={N!\over(N-s)!}\int \prod_{i=s+1}^NdV_i\rho(\boldsymbol{p},\boldsymbol{q},t)={N!\over(N-s)!}\rho_s(\boldsymbol{p_1},\cdots,\boldsymbol{q_s},t)

Prerequisite
~~~~~~~~~~~~

A conservative system: :math:`\mathcal H` does not depend explicitly on
time, and the system is not disturbed by external forces.

However, BBGKY hierarchy itself is not closed, thus it needs truncating.

Derivation
~~~~~~~~~~

Using Liouville's theorem to obtain the time evolution of :math:`f_s`
(or :math:`\rho_s`):

.. math:: {\partial \rho_s\over\partial t}=\int\prod_{i=s+1}^{N}dV_i{\partial\rho\over\partial t}=-\int\prod_{i=s+1}^NdV_i\{\rho,\mathcal{H}_s+\mathcal{H}_{N-s}+\mathcal{H}'\}

where the first term:

.. math:: -\int \prod_{i=s+1}^NdV_i\{\rho,\mathcal{H}_s\}=-\left\{\int\prod_{i=s+1}^{N}dV_i\rho,\mathcal{H}_s\right\}=-\{\rho_s,\mathcal{H}_s\}

the second term:

.. math:: -\int\prod_{i=s+1}^NdV_i\{\rho, \mathcal{H}_{N-s}\}=\int\prod_{i=s+1}^{N}dV_i\sum_{j=s+1}^{N}\left[{\partial\rho\over\partial\boldsymbol{p_j}}\cdot\left({\partial U\over\partial\boldsymbol{q_j}}+{1\over2}\sum_{k=s+1}^{N}{\partial\mathcal{V}(\boldsymbol{q_j}-\boldsymbol{q_k})\over\partial\boldsymbol{q_j}}\right)-{\partial\rho\over\partial\boldsymbol{q_j}}\cdot{\boldsymbol{p_j}\over m}\right]=0　\\using 　integration　of　 part　and　the　fact　 that　\lim_{q\rightarrow\infty}\rho=0　to　obtain　the　last 　equality

the third term:

.. math:: -\int\prod_{i=s+1}^NdV_i\{\rho,\mathcal{H}'\}=\int\prod_{i=s+1}^NdV_i\left[\sum_{n=1}^s{\partial\rho\over\partial\boldsymbol{p_n}}\cdot\sum_{j=s+1}^N{\partial\mathcal{V}(\boldsymbol{q_n}-\boldsymbol{q_j})\over\partial\boldsymbol{q_n}}+\sum_{j=s+1}^N{\partial\rho\over\partial\boldsymbol{p_j}}\cdot\sum_{n=1}^s{\partial\mathcal{V}(\boldsymbol{q_j}-\boldsymbol{q_n})\over\partial \boldsymbol{q_j}}\right]\\=\int\prod_{i=s+1}^NdV_i\sum_{n=1}^s{\partial\rho\over\partial\boldsymbol{p_n}}\cdot\sum_{j=s+1}^N{\partial\mathcal{V}(\boldsymbol{q_n}-\boldsymbol{q_j})\over\partial\boldsymbol{q_n}}=(N-s)\int\prod_{i=s+1}^NdV_i\sum_{n=1}^s{\partial\mathcal{V}(\boldsymbol{q_{n}}-\boldsymbol{q_{s+1}})\over\partial \boldsymbol{q_n}}\cdot{\partial\rho\over\partial\boldsymbol{p_n}}\\ =(N-s)\sum_{n=1}^s\int dV_{s+1}{\partial\mathcal{V}(\boldsymbol{q_{n}}-\boldsymbol{q_{s+1}})\over\partial \boldsymbol{q_n}}\cdot{\partial\over\partial\boldsymbol{p_n}}\left[\int\prod_{i=s+2}^NdV_i\rho\right]=(N-s)\sum_{n=1}^s\int dV_{s+1}{\partial\mathcal{V}(\boldsymbol{q_{n}}-\boldsymbol{q_{s+1}})\over\partial \boldsymbol{q_n}}\cdot{\partial\rho_{s+1}\over\partial\boldsymbol{p_n}}

Relation to Liouville's theorem
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

An equation in the BBGKY hierarchy tells us that the time evolution for
such a :math:`f_{s}` is consequently given by a Liouville-like equation,
but with a correction term that represents force-influence of the
:math:`N-s` suppressed particles (collision).

Boltzmann equation
------------------

.. math::

   \left[{\partial\over\partial t}-{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\over\partial\boldsymbol p_1}+{p_1\over m}\cdot{\partial\over\partial\boldsymbol q_1}\right]f_1=
   　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　\\-\int d^3\boldsymbol p_2d^2\Omega\left\vert{d \sigma\over d\Omega}\right\vert\lvert\boldsymbol v_1-\boldsymbol v_2\rvert[f_1(\boldsymbol p_1,\boldsymbol q_1,t)f_1(\boldsymbol p_2,\boldsymbol q_1,t)-f_1(\boldsymbol p_1',\boldsymbol  q_1,t)f_1(\boldsymbol  p_1',\boldsymbol q_1,t)]

Assumptions/Conditions
~~~~~~~~~~~~~~~~~~~~~~

1. (Mehran Kardar)

   -  dilute gas (low density), neglecting the three- and higher-body
      interactions

   -  short-range interaction

   -  molecular chaos: neglecting the correlation between particles
      after collisions

   -  collisions are thought of as being localized in physical space

2. (Harold Grad)

   -  Boltzmann-Grad limit (BGL)

      .. math:: N\rightarrow\infty\\ m\rightarrow0\\ \sigma\rightarrow0\\N\sigma^2= constant\\Nm=constant

      where N is the number of molecules of the system, m is the mass of
      each molecule, and :math:`\sigma` :math:`(d)` is a parameter which
      characterizes the range of the interparticle forces.

      In the limit, the mean free path is finite.

   -  low density so that only binary collisions between the constituent
      molecules need be considered

   -  the spatial dependence of gas properties is sufficiently low so
      that collisions can be thought of as being localized in physical
      space

   -  | short-range interaction

   -  stosszahlansatz

Derivations
~~~~~~~~~~~

From the first two BBGKY hierarchy equations:

.. math:: \left[{\partial\over\partial t}-{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\over\partial\boldsymbol p_1}+{p_1\over m}\cdot{\partial\over\partial\boldsymbol q_1}\right]f_1=\int dV_2{\partial\mathcal{V}(\boldsymbol q_1-\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot{\partial f_2\over\partial\boldsymbol p_1}\tag{a}

and

.. math:: \left[{\partial\over\partial t}-{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\over\partial\boldsymbol p_1}-{\partial U\over\partial\boldsymbol q_2}\cdot{\partial\over\partial\boldsymbol p_2}+{\boldsymbol p_1\over m}\cdot{\partial\over\partial\boldsymbol q_1}+{\boldsymbol p_2\over m}\cdot{\partial\over\partial\boldsymbol q_2}-{\partial\mathcal{V}(\boldsymbol q_1 -\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot\left({\partial\over\partial\boldsymbol p_1}-{\partial\over\partial\boldsymbol p_2}\right)\right]f_1\\=\int dV_3\left[{\partial\mathcal{V}(\boldsymbol q_1-\boldsymbol q_3)\over\partial\boldsymbol q_1}\cdot{\partial \over\partial\boldsymbol p_1}+{\partial\mathcal{V}(\boldsymbol q_2-\boldsymbol q_3)\over\partial\boldsymbol q_2}\cdot{\partial \over\partial\boldsymbol p_2}\right]f_3\tag{b}

Two ways:

1. (Mehran Kardar) **Analyze time scales**: (with typical speed of a gas
   particle at room temperature :math:`v\approx10^2ms^ {-1}`)

   (a)

   .. math:: {1\over\tau_U}\sim{\partial U\over\partial \boldsymbol q}\cdot{\partial\over\partial\boldsymbol p}

   :math:`\tau_U` is an extrinsic time scale corresponding to
   macroscopic distances :math:`L` and it can be made arbitrary long by
   increasing system size. For a typical value of
   :math:`L\approx10^{-3}m`, :math:`\tau_U\approx L/v\approx10^{-5}s`.

   :math:`\tau_U` describes the evolution of the center of mass of the
   two particles.

   (b)

   .. math:: {1\over\tau_c}\sim{\partial \mathcal{V}\over\partial \boldsymbol q}\cdot{\partial\over\partial\boldsymbol p}

   :math:`\tau_c` (collision duration) is an intrinsic time scale
   corresponding to the effective range of interaction
   :math:`d\approx10^{-10}m` (**short-range interaction**, including van
   der Waals and Lennard-Jones), resulting in
   :math:`\tau_c\approx10^{-12}s`.

   :math:`\tau_c` describes the evolution of relative coordinates.

   (c)

   .. math:: {1\over\tau_\times}\sim\int dV{\partial\mathcal{V}\over\partial\boldsymbol q}\cdot{\partial\over\partial\boldsymbol p}{f_{s+1}\over f_s}\sim\int dV{\partial\mathcal{V}\over\partial\boldsymbol q}\cdot{\partial\over\partial\boldsymbol p}N{\rho_{s+1}\over\rho_s}

   :math:`\tau_\times` is the mean free time (the typical distance a
   particle travels between collisions), because :math:`f_{s+1}/f_s` is
   related to the probability of finding another particle per unit
   volume,which is roughly the particle density
   :math:`n=N/V\approx10^{26}m^{-3}`. Therefore

   .. math:: \tau_\times\approx{\tau_c\over nd^3}\approx{1\over nvd^3}\approx10^{-8}s

   Then, by exploiting :math:`\tau_c/\tau_\times\approx nd^3\ll1`
   (**dilute**), the RHS of the equation (b) can be set to zero
   (**neglecting the three-body interaction**)[still reversible]. At
   separations comparable to :math:`d`, equation (b) becomes:
   (neglecting the smaller terms)

   .. math:: \left[{\boldsymbol p_1\over m}\cdot{\partial\over\partial\boldsymbol q_1}+{\boldsymbol p_2\over m}\cdot{\partial\over\partial\boldsymbol q_2}-{\partial\mathcal{V}(\boldsymbol q_1 -\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot\left({\partial\over\partial\boldsymbol p_1}-{\partial\over\partial\boldsymbol p_2}\right)\right]f_2=0

   When we expect :math:`f_2(\boldsymbol q_1, \boldsymbol q_2)` to have
   slow variations over the center of mass coordinate
   :math:`\boldsymbol Q =(\boldsymbol q_1 +\boldsymbol q_2)/2`, and
   large variations over the relative coordinate
   :math:`\boldsymbol q=\boldsymbol q_2 - \boldsymbol q_1`. Therefore,
   :math:`\partial f_2/\partial\boldsymbol q\gg\partial f_2/\partial\boldsymbol Q`,
   and
   :math:`\partial f_2/\partial \boldsymbol q_2\approx-\partial f_2/\partial \boldsymbol q_1\approx\partial f_2/\partial \boldsymbol q`,
   leading to

   .. math:: {\partial\mathcal{V}(\boldsymbol q_1 -\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot\left({\partial\over\partial\boldsymbol p_1}-{\partial\over\partial\boldsymbol p_2}\right)f_2=-\left({\boldsymbol p_1-\boldsymbol p_2\over m}\right)\cdot{\partial\over\partial \boldsymbol q}f_2

   **This equation describes the collision of the two particles**.

   The collision term on the RHS of Equation (a) becomes

   .. math:: {df_1\over dt}\rvert_{coll.}=\int d^3\boldsymbol p_2d^3\boldsymbol q_2{\partial\mathcal{V}(\boldsymbol q_1-\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot\left({\partial\over\partial\boldsymbol p_1}-{\partial\over\partial\boldsymbol p_2}\right)f_2\approx\int d^3\boldsymbol p_2d^3\boldsymbol q\left({\boldsymbol p_2-\boldsymbol p_1\over m}\right)\cdot{\partial\over\partial\boldsymbol q}f_2(\boldsymbol p_1,\boldsymbol q_1,\boldsymbol p_2, \boldsymbol q;t)

   The first identity is obtained from Equation (a) by adding term
   proportional to :math:`\partial f_2/\partial\boldsymbol p_2` is a
   complete derivative and integrates to zero. The second approximation
   is valid in the relative coordinates as long as we examine events in
   time with a resolution longer than :math:`\tau_c`.

   To describe the scattering of particles, choose one axis to be
   parallel to the :math:`\boldsymbol p_2-\boldsymbol p_1`, with the
   corresponding coordinate :math:`a` that is negative before a
   collision, and positive afterwards. The other two coordinate of
   :math:`\boldsymbol q` are represented by an :math:`impact`
   :math:`vector` :math:`\boldsymbol b` that is :math:`\boldsymbol 0`
   for a head-o collision. Now integrate over :math:`a` to get

   .. math:: {df_1\over dt}\rvert_{coll.}=\int d^3\boldsymbol p_2d^2\boldsymbol b \lvert\boldsymbol v_1-\boldsymbol v_2\rvert\left[f_2(\boldsymbol p_1,\boldsymbol q_1,\boldsymbol p_2,\boldsymbol b,+;t)-f_2(\boldsymbol p_1,\boldsymbol q_1, \boldsymbol p_2,\boldsymbol b,-;t)\right]

   where
   :math:`\lvert\boldsymbol v_1-\boldsymbol v_2\rvert=\lvert\boldsymbol p_1-\boldsymbol p_2\rvert/m`
   is the relative speed of the two particles, with
   :math:`(\boldsymbol b,+)` and :math:`(\boldsymbol b,-)` referring to
   relative coordinates after and before the collision. Note that
   :math:`d^2\boldsymbol b\lvert\boldsymbol v_1-\boldsymbol v_2\rvert`
   is the flux of particles impinging on the element of area
   :math:`d^2\boldsymbol b`.

   **KEY**: the density :math:`f_2` for situations corresponding to
   before and after the collision have to be treated differently,
   otherwise the result will be meaningless.

   Because the :math:`f_2`\ s before and after collision are related to
   streaming,
   :math:`f_2(\boldsymbol p_1,\boldsymbol q_1,\boldsymbol p_2,\boldsymbol b,+;t)=f_2(\boldsymbol p_1',\boldsymbol q_1',\boldsymbol p_2',\boldsymbol b,-;t)`
   , where :math:`\boldsymbol p_1'` and :math:`\boldsymbol p_2'` are
   momenta whose collision at an impact vector :math:`\boldsymbol b`
   results in production of outgoing particles with momenta
   :math:`\boldsymbol p_1` and :math:`\boldsymbol p_2`.
   :math:`\boldsymbol p_1'` and :math:`\boldsymbol p_2'` can be obtained
   by using time reversal symmetry by integrating the equations of
   motion for incoming collision particles of momenta
   :math:`-\boldsymbol p_1` and :math:`-\boldsymbol p_2`. Thus

   .. math:: {df_1\over dt}\rvert_{coll.}=\int d^3\boldsymbol p_2d^2\boldsymbol b \lvert\boldsymbol v_1-\boldsymbol v_2\rvert\left[f_2(\boldsymbol p_1',\boldsymbol q_1',\boldsymbol p_2',\boldsymbol b,-;t)-f_2(\boldsymbol p_1,\boldsymbol q_1, \boldsymbol p_2,\boldsymbol b,-;t)\right]

   Introduce the relative momenta
   :math:`\boldsymbol p=\boldsymbol p_1-\boldsymbol p_2` and
   :math:`\boldsymbol p'=\boldsymbol p_1' -\boldsymbol p_2'`.

   In elastic collisions, the magnitude of :math:`\boldsymbol p` is
   preserved and it merely rotates to a final direction indicated by the
   angles :math:`(\theta,\phi)\equiv\hat\Omega(\boldsymbol b)` in
   spherical coordinates. Since there is a one -to-one correspondence
   between the impact vector :math:`\boldsymbol b` and the *solid angle*
   :math:`\Omega`, then

   .. math:: {df_1\over dt}\rvert_{coll.}=\int d^3\boldsymbol p_2d^2\Omega\left\vert{d\sigma\over d\Omega}\right\vert \lvert\boldsymbol v_1-\boldsymbol v_2\rvert\left[f_2(\boldsymbol p_1',\boldsymbol q_1',\boldsymbol p_2',\boldsymbol b,-;t)-f_2(\boldsymbol p_1,\boldsymbol q_1, \boldsymbol p_2,\boldsymbol b,-;t)\right]\tag c

   where :math:`\vert{d\sigma/d\Omega}\vert` is the *differential
   cross-section*. It is equal to the area presented to an incoming beam
   that scatters into the solid angle :math:`\Omega`.

   According to
   :math:`\boldsymbol p_1+\boldsymbol p_2=\boldsymbol p_1'+\boldsymbol p_2'`
   (conservation of momentum), and
   :math:`\boldsymbol p_1'-\boldsymbol p_2'=\lvert\boldsymbol p_1-\boldsymbol p_2\rvert\hat\Omega(\boldsymbol b)`
   (conservation of energy)

   .. math:: \boldsymbol p_1'=(\boldsymbol p_1+\boldsymbol p_2+\lvert\boldsymbol p_1-\boldsymbol p_2\rvert\hat\Omega(\boldsymbol b))/2\\ \boldsymbol p_2'=(\boldsymbol p_1+\boldsymbol p_2-\lvert\boldsymbol p_1-\boldsymbol p_2\rvert\hat\Omega(\boldsymbol b))/2

   Make the substitution in Equation (c)

   .. math:: f_2(\boldsymbol p_1,\boldsymbol q_1,\boldsymbol p_2,\boldsymbol b,-;t)=f_1(\boldsymbol p_1,\boldsymbol q_1,t)\cdot f_1(\boldsymbol p_2,\boldsymbol q_1,t)

   which is known as the ***assumption of molecular chaos***.

   Then we come to the Boltzmann equation:

   .. math::

      \left[{\partial\over\partial t}-{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\over\partial\boldsymbol p_1}+{p_1\over m}\cdot{\partial\over\partial\boldsymbol q_1}\right]f_1=
      　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　\\-\int d^3\boldsymbol p_2d^2\Omega\left\vert{d \sigma\over d\Omega}\right\vert\lvert\boldsymbol v_1-\boldsymbol v_2\rvert[f_1(\boldsymbol p_1,\boldsymbol q_1,t)f_1(\boldsymbol p_2,\boldsymbol q_1,t)-f_1(\boldsymbol p_1',\boldsymbol  q_1,t)f_1(\boldsymbol  p_1',\boldsymbol q_1,t)]

2. (Harold Grad)

   Using :math:`\boldsymbol v` instead of :math:`\boldsymbol  p`, define
   :math:`\rho_1^{\sigma}\equiv\int_{D_1}\prod_{i=2}^N(d^3\boldsymbol q_id^3\boldsymbol v_i)\rho_N`,
   :math:`\rho_2^{\sigma}\equiv\int_{D_2}\prod_{i=3}^N(d^3\boldsymbol q_id^3\boldsymbol v_i)\rho_N`,
   where :math:`D_1` is the part of the physical space such that no
   particle is within :math:`\sigma` of particle 1, that is,
   :math:`\lvert\boldsymbol q_i-\boldsymbol q_1\rvert\geqslant\sigma`,
   :math:`i=2,3,\cdots,N`, and :math:`D_2` is the part of the physical
   space such that
   :math:`\lvert\boldsymbol q_i-\boldsymbol q_1\rvert\geqslant\sigma`,
   :math:`i=3,4,\cdots,N`. In the BGL, :math:`\rho_1` and :math:`\rho_2`
   can be replaced by :math:`\rho_1^{\sigma}` and
   :math:`\rho_2^{\sigma}`. Integrating the Liouville equation over
   :math:`D_1`, we obtain

   .. math:: {\partial \rho_1^{\sigma}\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol q_1}+(N-1)\oint_{S_2}d\boldsymbol v_2 d\boldsymbol S_2(\boldsymbol v_1-\boldsymbol v_2)\rho_2^{\sigma}=(N-1){\partial\over\partial\boldsymbol v_1}\int_{\lvert\boldsymbol q_1-\boldsymbol q_2\rvert\geqslant\sigma}d\boldsymbol  v_2d\boldsymbol q_2{\partial\mathcal{V(\boldsymbol q_1-\boldsymbol q_2)}\over\partial\boldsymbol q_1}\rho_2^{\sigma}

   where :math:`S_i` is the surface of the sphere
   :math:`\lvert\boldsymbol q_i-\boldsymbol q_1\rvert=\sigma`. Note that
   one more term appears because the fact that the limits of integration
   depend on :math:`\boldsymbol q_1`.

   | For the part of the physical space in which
     :math:`\lvert\boldsymbol q_i-\boldsymbol q_1\rvert\geqslant\sigma`
     we have
     :math:`\mathcal{V}(\boldsymbol q_1-\boldsymbol q_2)={\partial\mathcal{V}(\boldsymbol q_1-\boldsymbol q_2)\over\partial\boldsymbol q_1}=0`,
     so that the RHS of above equation is zero.

   .. math:: {\partial \rho_1^{\sigma}\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol q_1}+(N-1)\oint_{S_2}d\boldsymbol v_2 d\boldsymbol S_2(\boldsymbol v_1-\boldsymbol v_2)\rho_2^{\sigma}=0\tag d

   Introducing a coordinate system in the plane perpendicular to the
   vector :math:`\boldsymbol V=\boldsymbol v_2-\boldsymbol v_1` with
   origin at :math:`\boldsymbol q_1` and defining the polar coordinate
   system :math:`r`, :math:`\epsilon` in this plane, each point on
   :math:`S_2` corresponds to a point on the disk
   :math:`0\leqslant r\leqslant \sigma`,
   :math:`0\leqslant \epsilon< 2\pi`. The disk is covered twice, once by
   projecting :math:`S_2^+`, on which
   :math:`\boldsymbol V\cdot d \boldsymbol S_2>0`, and once by
   projecting :math:`\boldsymbol S_2^{-}`, on which
   :math:`\boldsymbol V\cdot d\boldsymbol S_2<0`. The points on
   :math:`\boldsymbol S_2^\pm` are thus in a one-to-one correspondence
   with the points on the disk, and can thus be written as functions of
   :math:`r`, and :math:`\epsilon`. Calling the element of area in the
   disk :math:`d\omega=rdrd\epsilon`
   (:math:`d^2\boldsymbol b=bdbd\phi`), and writing
   :math:`\boldsymbol q^{\pm}=\boldsymbol q^\pm(r,\epsilon)`, we can
   transform the surface integration which appears in Equation (d) to an
   integration over the disk, giving

   .. math:: {\partial \rho_1^{\sigma}\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol q_1}=(N-1)\int d\omega d\boldsymbol v_2 V[\rho_2^{\sigma}(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^+,t)-\rho_2^\sigma(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^-,t)]

   In the BGL

   .. math:: {\partial \rho_1^{\sigma}\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial\rho_1^{\sigma}\over\partial \boldsymbol q_1}=N\int d\omega d\boldsymbol v_2 V[\rho_2^{\sigma}(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^+,t)-\rho_2^\sigma(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^-,t)]\tag e

   According to Equation (b) and we **only consider the binary
   collision**. Also the binary collision term is not zero, that is
   :math:`\lvert\boldsymbol q_1-\boldsymbol q_2\rvert<\sigma`, for times
   of order :math:`\sigma`.

   .. math:: {\partial\rho_2\over\partial t}-{\partial U\over\partial\boldsymbol q_1}\cdot{\partial\rho_2\over\partial\boldsymbol p_1}-{\partial U\over\partial\boldsymbol q_2}\cdot{\partial\rho_2\over\partial\boldsymbol p_2}+{\boldsymbol p_1\over m}\cdot{\partial\rho_2\over\partial\boldsymbol q_1}+{\boldsymbol p_2\over m}\cdot{\partial\rho_2\over\partial\boldsymbol q_2}-{\partial\mathcal{V}(\boldsymbol q_1 -\boldsymbol q_2)\over\partial\boldsymbol q_1}\cdot\left({\partial\rho_2\over\partial\boldsymbol p_1}-{\partial\rho_2\over\partial\boldsymbol p_2}\right)=\mathcal{L}[\rho_2]=0 \tag f

   which means :math:`\rho_2=constant`, and therefore we can replace the
   term
   :math:`\rho_2^{\sigma}(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^+,t)`
   by
   :math:`\rho_2^{\sigma}(\boldsymbol V_1,\boldsymbol Q_1,\boldsymbol V_2,\boldsymbol Q_2,\tau)`,
   where the :math:`(\boldsymbol V_i,\boldsymbol Q_i)` are the phases
   which are transformed into the phases
   :math:`(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^+)`
   in a time :math:`t-\tau` by the motion described by the Equation (f).
   We specially choose the smallest possible value of :math:`\tau` for
   which the phase
   :math:`(\boldsymbol V_1,\boldsymbol Q_1,\boldsymbol V_2,\boldsymbol Q_2)`
   represents a pre-collisional phase which produces the
   post-collisional phase
   :math:`(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^+)`.

   Make the assumption ***stosszahlansatz*** (molecular chaos
   assumption):
   :math:`\rho_2(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2,t)=\rho_1(\boldsymbol v_1,\boldsymbol q_1)\rho_1(\boldsymbol v_2,\boldsymbol q_2)`
   when
   :math:`(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2)`
   are phases which represent molecules which have not yet collided.

   The RHS of Equation (e) can be written as
   :math:`N\int d\omega d\boldsymbol v_2V[\rho_2(\boldsymbol V_1,\boldsymbol Q_1,\boldsymbol V_2,\boldsymbol Q_2,\tau)-\rho_2(\boldsymbol v_1,\boldsymbol q_1,\boldsymbol v_2,\boldsymbol q_2^-,t)]`
   and since both of the phases which appear in the argument of
   :math:`\rho_2` are pre-collisional phases, we can correctly apply the
   ***stosszahlansatz***. Note that in the BGL
   :math:`\tau\rightarrow t`, and
   :math:`\boldsymbol q_2^-\rightarrow\boldsymbol q_1`, this replacement
   being strictly valid only if **the spatial variation of**
   :math:`\rho_1` **is not appreciable over distances of order**
   :math:`\sigma`. Thus

   .. math:: {\partial f_1\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial f_1\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial f_1\over\partial \boldsymbol q_1}=\int d\omega d\boldsymbol v_2 V[f_1(\boldsymbol {\bar v_1},\boldsymbol q_1,t)f_1(\boldsymbol {\bar v_2},\boldsymbol q_1,t)-f_1(\boldsymbol v_1,\boldsymbol q_1,t)f_1(\boldsymbol v_2,\boldsymbol q_1,t)]

   where :math:`\boldsymbol{\bar v_1}`, :math:`\boldsymbol{\bar v_2}`
   are the velocities which become :math:`\boldsymbol{v_1}`,
   :math:`\boldsymbol{v_2}` following a binary collision.

Interpretations
~~~~~~~~~~~~~~~

1. (Mehran Kardar)

   The streaming terms on the LHS of the Boltzmann equation describe the
   motion of a single particle in the external potential :math:`U`. The
   collision terms on the RHS of the Boltzmann equation mean the
   probability of finding a particle of :math:`\boldsymbol p_1'` at
   :math:`\boldsymbol q_1'` is suddenly altered if it undergoes a
   collision with another particle of momentum :math:`\boldsymbol p_2`.
   The probability of such a collision is the product of kinematic
   factors described by the differential cross-section
   :math:`\vert{d\sigma/d\Omega}\vert`, the flux of incident particles
   proportional to :math:`\lvert \boldsymbol v_2-\boldsymbol v_1\rvert`,
   and the joint probability of finding the two particles, approximated
   by :math:`f_1(\boldsymbol p_1)f_1(\boldsymbol p_2)`. The first term
   on the RHS of the Boltzmann equation subtracts this probability and
   integrates over all possible momenta and solid angles describing the
   collision. The second term represents an addition to the probability
   that results from the inverse process: a particle can suddenly appear
   with coordinates :math:`(\boldsymbol p_1,\boldsymbol q_1)` as a
   result of a collision between two particles initially with momenta
   :math:`\boldsymbol  p_1'` and :math:`\boldsymbol  p_2'`. The
   cross-section, and the momenta
   :math:`(\boldsymbol p_1',\boldsymbol p_2')`, may have a complicated
   dependence on :math:`(\boldsymbol p_1,\boldsymbol p_2)` and
   :math:`\Omega`, determined by the specific form of the potential
   :math:`\mathcal{V}`.

2. (Harold Grad)

   :math:`[(\boldsymbol v_2-\boldsymbol v_1)\cdot d\boldsymbol S_2>0]` :
   particles completing a collision;
   :math:`[(\boldsymbol v_2-\boldsymbol v_1)\cdot d\boldsymbol S_2<0]` :
   particles initiating a collision

The resources of irreversibility of the Boltzmann equation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. stosszahlansatz (molecular chaos assumption)

2. collisions are thought of as being localized in physical space

Equation (c) is still reversible.

Consequences/Applications
~~~~~~~~~~~~~~~~~~~~~~~~~

The mass density :math:`F`, which is defined such that
:math:`Fd\boldsymbol q_1d\boldsymbol v_1` is the expected mass in the
phase space volume element :math:`d\boldsymbol q_1d\boldsymbol v_1`, and
the Boltzmann equation becomes

.. math:: {\partial F\over\partial t}-{1\over m}{\partial U\over\partial\boldsymbol q_1}\cdot{\partial F\over\partial \boldsymbol v_1}+\boldsymbol v_1\cdot{\partial F\over\partial \boldsymbol q_1}={1\over m}\int d\omega d\boldsymbol v_2 V[F(\boldsymbol {\bar v_1},\boldsymbol q_1,t)F(\boldsymbol {\bar v_2},\boldsymbol q_1,t)-F(\boldsymbol v_1,\boldsymbol q_1,t)F(\boldsymbol v_2,\boldsymbol q_1,t)]

Integrating :math:`F` over its velocity argument will then give an
expression for the expected mass in the volume :math:`d\boldsymbol q_1`.
Writing :math:`\boldsymbol q` for :math:`\boldsymbol q_1`, we have

.. math:: f(\boldsymbol q,t)=\int d\boldsymbol v_1 F(\boldsymbol q,\boldsymbol v_1,t)

The function :math:`f` is the macroscopic fluid mass density which is
used in the fluid mechanical description.

Defining the :math:`\nu th` moments of :math:`F`:

.. math:: M_{\alpha\beta\cdots\nu}=\int d\boldsymbol v_1\boldsymbol v_{1\alpha}\boldsymbol v_{1\beta}\cdots\boldsymbol v_{1\nu}F(\boldsymbol q,\boldsymbol v_1,t)

Collision term of the Boltzmann equation
----------------------------------------

Hard sphere model
~~~~~~~~~~~~~~~~~

Consider the scattering of two hard spheres of diameter :math:`D`, the
scattering angle is related to the impact parameter :math:`b` by
:math:`cos(\theta/2)=b/D` for all :math:`\phi`. Thus the differential
cross-section is obtained

.. math:: d^2\sigma=bdbd\phi=Dcos\left({\theta\over2}\right)Dsin\left({\theta\over2}\right){d\theta\over2}d\phi={D^2\over4}sin\theta d\theta d\phi={D^2\over4}d^2\Omega

or

.. math:: \left\vert{d\sigma\over d\Omega}\right\vert={D^2\over 4}

(Note that the solid angle in three dimensions is given by
:math:`d^2\Omega=sin\theta d\theta d\phi`, there is almost no difference
between :math:`d\sigma` and :math:`d^2\sigma`, :math:`d\Omega` and
:math:`d^2\Omega`) Integrating over all angles leads to the total
cross-section of :math:`\sigma=\pi D^2`.

Central force field
~~~~~~~~~~~~~~~~~~~

.. math:: \Theta=\int_0^{\nu_0}{d\nu\over\left[1-\nu^2-{4\phi_{12}(b\nu^{-1})\over mV^2}\right]^{{1\over2}}}\\1-\nu_0^2-{4\phi_{12}(b\nu_0^{-1})\over mV^2}=0\tag g

where :math:`\Theta={(\pi-\theta)/2}`, :math:`\nu=b/R_r`,
:math:`\boldsymbol R_r=\boldsymbol q_1-\boldsymbol q_2` and
:math:`V=\lvert\boldsymbol v_1-\boldsymbol v_2\rvert`. (Note that the
motion is in a plane)

For the power law potential (**particles are identical**:
:math:`m_1=m_2=m`)

.. math:: \phi_{12}(R_r)\varpropto{1\over R_r^{s-1}}

that is

.. math:: \phi_{12}(R_r)={K\over R_r^{s-1}}

where :math:`K` is the proportionality constant.

**The hard sphere potential is the limiting case of the power law
potential for** :math:`s\rightarrow\infty`,
:math:`K^{1/\left(s-1\right)}\rightarrow d`.

Equation (g) becomes

.. math:: \Theta=\int_0^{\nu_0}{d\nu\over\left[1-\nu^2-{4K\nu^{s-1}\over mV^2b^{s-1}}\right]^{{1\over2}}}

or

.. math:: \Theta({\beta})=\int_0^{\nu_0}{d\nu\over\left[1-\nu^2-\left({\nu\over\beta}\right)^{s-1}\right]^{{1\over2}}}

where :math:`\beta=(mV^2/4K)^{1/\left(s-1\right)}b`.

Thus

.. math:: \left\vert{d\sigma\over d\Omega}\right\vert={bdb\over sin\theta d\theta}=\left({mV^2\over4K}\right)^{-{2\over s-1}}{\beta\over sin\theta}{d\beta\over d\theta}=\left({mV^2\over4K}\right)^{-{2\over s-1}}{\beta(\Theta)\over 2sin2\Theta}{d\beta\over d\Theta}

When we meet **electron-nuclear model** (:math:`m_Z\gg m_e`)

.. math:: \left\vert{d\sigma\over d\Omega}\right\vert={bdb\over sin\theta d\theta}=\left({m_eV^2\over2K}\right)^{-{2\over s-1}}{\beta\over sin\theta}{d\beta\over d\theta}=\left({m_eV^2\over2K}\right)^{-{2\over s-1}}{\beta(\Theta)\over 2sin2\Theta}{d\beta\over d\Theta}

When :math:`s=2`, that is it is a Coulomb potential, it is consistent
with *Rutherford scattering formula*

.. math:: \left\vert{d\sigma\over d\Omega}\right\vert=\left({1\over4\pi\varepsilon_0}{Ze^2\over2m_eV^2sin^2\left({\theta\over2}\right)}\right)^2

Consider the asymptotic behavior of :math:`\Theta(\beta)` and explicitly
show why **the potential must be generally cut off**.

First small :math:`\beta`

.. math:: \Theta_{\beta\rightarrow0}\approx\int_0^\beta{d\nu\over\left[1-\left({\nu\over\beta}\right)^{s-1}\right]^{{1\over2}}}=\beta\int_0^1{du\over\left[1-u^{s-1}\right]^{{1\over2}}}

that is :math:`\Theta` is linear in :math:`\beta`.

For large :math:`\beta`

.. math:: \Theta_{\beta\rightarrow\infty}=\int_0^{\nu_0}{d\nu\over\left[\nu_0^2-\nu^2+\left({\nu_0\over\beta}\right)^{s-1}-\left({\nu\over\beta}\right)^{s-1}\right]^{{1\over2}}}\approx\int_0^1{du\over\left(1-u^2\right)^{{1\over2}}}\left(1-{1\over2\beta^{s-1}}{1-u^{s-1}\over1-u^2}\right)={\pi\over2}-{A(s)\over\beta^{s-1}}

Thus, for :math:`\beta\rightarrow\infty`,

.. math:: \beta\varpropto\left({\pi\over2}-\Theta\right)^{-{1\over s-1}}

or

.. math:: \beta^2\varpropto\left({\pi\over2}-\Theta\right)^{-{2\over s-1}}

so that

.. math:: \beta{d\beta\over d\Theta}\varpropto\left({\pi\over2}-\Theta\right)^{-{s+1\over s-1}}

which shows that :math:`\vert{d\sigma/d\Omega}\vert` contains a
nonintegrable singularity at :math:`\Theta={\pi/2}`. This can be avoided
either by cutting off :math:`\beta`, so that the potential
:math:`\phi_{12}` is zero for :math:`\beta>\beta_{max}\ll\infty`, or by
the less physical, but mathematically more tractable, method of directly
cutting off :math:`\Theta` near :math:`\pi/2`, that is, eliminating
grazing collisions from the collision term (a grazing collision is one
in which there is little change in the direction of the relative
velocity).
