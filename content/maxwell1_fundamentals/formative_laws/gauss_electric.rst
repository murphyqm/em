.. _gauss_electric:

Gauss's Law for Electric Fields
===============================
 .. figure:: images/GaussElec.png
    :align: right
    :scale: 60%
    :name: GaussElec

    Charge enclosed

Gauss’s law for the electric field describes the static electric field
generated by a distribution of electric charges. It states that the electric
flux through any closed surface is proportional to the total electric charge
enclosed by this surface. By convention, a positive electric charge generates
a positive electric field. The law was published posthumously in 1867 as part
of a collection of work by the famous German mathematician Carl Friedrich
Gauss.

.. _gauss_electric_integral:

Integral Equation
-----------------

Gauss’s law in integral form is given below:

.. math::
	\int_V \boldsymbol{\nabla} \cdot \mathbf{e} \; ~dv =\oint_{S} \mathbf{e} \cdot \hat{\mathbf{n}} \; ~da = \frac{Q}{ \varepsilon_{0} }\;,
	:label: Gauss_e_int

where:

- :math:`\mathbf{e}` is the electric field
- :math:`Q` is the enclosed electric charge
- :math:`\varepsilon_0` is the electric permittivity of free space
- :math:`\hat{\mathbf{n}}` is the outward pointing unit-normal

Flux is a measure of the strength of a field passing through a surface.
Electric flux is defined in general as

.. math::
  \boldsymbol{\Phi} = \int_S \mathbf{e} \cdot \hat{\mathbf{n}} \, \mathrm{d}a.
  :label: e_flux

We can think of electric field as flux density. Gauss’s law tells us that the
net electric flux through any closed surface is zero unless the volume bounded
by that surface contains a net charge.


.. _gauss_electric_differential:

Differential Form
-----------------

When considering a spatially extended charged body, we can think of its charge
as being continously distributed throughout the body with density
:math:`\rho`. The total charge is then given by the integral of the charge
density over the volume of the body.

.. math::
	Q = \int_V \rho \; \mathrm{d}v\;.
	:label: charge_dens

Using this definition and applying the divergence theorem to the left hand
side of Gauss's law :eq:`Gauss_e_int`, we can rewrite the law as:

.. math::
	\int_V \boldsymbol{\nabla} \cdot \mathbf{e} \; \mathrm{d}v = \int_V \frac{\rho}{\varepsilon_0} \; \mathrm{d}v \;.
	:label:

Since this equation must hold for any volume :math:`V` , we can equate the
integrands, giving the differential form of Gauss's law:

.. math::
	\boldsymbol{\nabla} \cdot \mathbf{e} = \frac{\rho}{\varepsilon_0}.
	:label: Gauss_e_diff

It can be shown that Gauss' law for electric fields is equivalent to Coulomb's
law (see :ref:`gauss_electric_equivalence_to_coulombs_law`)

Gauss's Law in Matter
---------------------

Gauss's law for electric fields is most easily understood by neglecting :ref:`electric displacement<dielectric_permittivity_index>` (:math:`\mathbf{d}`). In matter, the :ref:`dielectric permittivity<dielectric_permittivity_index>` may not be equal to the permittivity of free-space (i.e. :math:`\varepsilon \neq \varepsilon_0`). In matter, the density of electric charges can be separated into a "free" charge density (:math:`\rho_f`) and a "bounded" charge density (:math:`\rho_b`), such that:

.. math::
	\rho = \rho_f + \rho_b
	:label: gauss_law_charge_decomp

The free-charge density refers to charges which flow freely under the application of an electric field; i.e. they produce a current which is divergence-free. The bounded-charge density refers to electrical charges attributed to electrical polarization (:math:`\mathbf{p}`). By combining Eqs. :eq:`Gauss_e_diff` and :eq:`gauss_law_charge_decomp` with our definition for :ref:`electrical polarization<dielectric_permittivity_index>`, we find that:

.. math::
	\nabla \cdot \mathbf{d} - \nabla \cdot \mathbf{p} = \rho_f + \rho_b
	:label:

By using the constitutive relationship :math:`\mathbf{d} = \varepsilon \mathbf{e}` and separating the previous equation into bounded and free contributions, we find that:

.. math::
	-\nabla \cdot \mathbf{p} = \rho_b
	:label:

and

.. math::
	\nabla \cdot \mathbf{d} = \rho_f
	:label:

The above equation is the **differential form of Gauss's equation in matter**. Meanwhile, the **integral form of Gauss's equations in matter** is given by:

.. math::
	\int_V \nabla \cdot \mathbf{d} \; dV = \oint_S \mathbf{d} \cdot \mathbf{\hat n} \; da = Q_f

where :math:`Q_f` is the total enclosed free charge.

Units
-----

+-----------------------+-----------------------------+---------------------+-------------------------+
|     Surface area      |  :math:`\text{S}`           | m :math:`\! ^{2}`   | Square meter            |
+-----------------------+-----------------------------+---------------------+-------------------------+
|     Volume            |  :math:`V`                  | m :math:`\! ^{3}`   |  Cubic meter            |
+-----------------------+-----------------------------+---------------------+-------------------------+
|     Electric charge   | :math:`q, Q, Q_f`           | C                   |  Coulomb                |
+-----------------------+-----------------------------+---------------------+-------------------------+
|Electric charge density| :math:`\rho, \rho_f, \rho_b`| C/m :math:`\! ^{3}` | Coulomb per cubic meter |
+-----------------------+-----------------------------+---------------------+-------------------------+
|     Electric field    | :math:`\mathbf{e}`          | V/m                 | Volt per meter          |
+-----------------------+-----------------------------+---------------------+-------------------------+
|Electric displacement  | :math:`\mathbf{d}`          | A/m :math:`\! ^{2}` | Volt per meter          |
+-----------------------+-----------------------------+---------------------+-------------------------+
|Dielectric permittivity|:math:`\varepsilon`          | F/m                 | Farad per meter         |
+-----------------------+-----------------------------+---------------------+-------------------------+

**Conversions**

.. math::
    \varepsilon_0 = \frac{\text{F}}{\text{m}} = \frac{\text{C}}{\text{V} \cdot \text{m}}.
