# Publication figure style


Very basic repository with the figure style I use for publications. This repository also includes example code to create this figures

Usage 

```python
plt.style.use('https://raw.githubusercontent.com/RAHXION/Resources/main/Publication_figure_style.mplstyle')

x = np.random.uniform(0, 10, 30)
x.sort()
yt = 2 * x + 1
y = yt + np.random.normal(loc=0, scale=2, size=yt.size)

fig, ax = plt.subplots()
ax.plot(x, yt, label="Modelo",color='r')
ax.scatter(x, y,marker='o',color='k',label = 'Measured points')
ax.set_xlabel('x values ($m^3$)')
ax.set_ylabel("y values ($\\frac{m^{3}}{kg}$)")
ax.set_title("Ejemplo de un gráfico")
ax.legend()
ax.legend(loc='lower right', shadow=True) 

plt.savefig('Figure_example.png',dpi=300)

```