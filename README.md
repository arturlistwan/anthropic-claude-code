# 🦠 Bacteria Competition Simulator

An interactive visualization of two bacterial species competing for dominance in a 100x100 grid environment. Watch as different colored bacteria colonies grow, spread, and battle for territory in real-time!

## 🎯 Features

- **Real-time Simulation**: Watch bacteria colonies grow and compete dynamically
- **100x100 Grid**: 10,000 cells of competitive space
- **Two Species**: Red (Species A) and Cyan (Species B) bacteria with identical growth characteristics
- **Interactive Controls**: Start, pause, reset, and step through generations
- **Adjustable Parameters**:
  - Simulation speed (1-60 generations per second)
  - Initial population size (10-500 cells per species)
  - Growth rate (10-100% probability)
- **Live Statistics**: Real-time tracking of population counts
- **Beautiful UI**: Modern, responsive design with gradient backgrounds

## 🚀 How to Run

1. Simply open `index.html` in any modern web browser
2. No installation or dependencies required!

Alternatively, you can use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (if you have http-server installed)
npx http-server
```

Then navigate to `http://localhost:8000` in your browser.

## 🎮 How to Use

### Controls

- **Start**: Begin or resume the simulation
- **Pause**: Pause the simulation at any time
- **Reset**: Clear the grid and generate new random initial populations
- **Step**: Advance the simulation by exactly one generation (useful for detailed observation)

### Parameters

- **Speed**: Control how fast generations pass (1-60 generations per second)
- **Initial Population**: Set how many bacteria of each species start on the grid (10-500)
- **Growth Rate**: Adjust the probability that a bacterium will reproduce into an adjacent empty cell (10-100%)

### Statistics

The simulation displays real-time statistics:
- **Species A (Red)**: Current population count
- **Species B (Cyan)**: Current population count
- **Empty Cells**: Number of unoccupied spaces

## 🧬 Simulation Rules

1. **Initial Seeding**: Both species are randomly placed on the grid at the start
2. **Growth Phase**: Each generation, every bacterium has a chance to reproduce
3. **Reproduction**: Bacteria can only grow into adjacent empty cells (8 neighbors: N, S, E, W, NE, NW, SE, SW)
4. **Random Selection**: Each bacterium randomly selects from available empty neighbors
5. **No Conflict**: Bacteria cannot overwrite or kill other bacteria directly
6. **Competition**: Species compete by occupying space first, limiting opponents' growth

## 🎨 Visual Design

- **Species A**: Bright red (#ff6b6b) - Visually striking warm color
- **Species B**: Cyan (#4ecdc4) - Cool, contrasting color
- **Empty Cells**: Light gray (#f0f0f0) - Neutral background

## 🔬 Scientific Concepts

This simulation demonstrates several key concepts in microbiology and ecology:

- **Resource Competition**: Limited space forces species to compete
- **Stochastic Growth**: Random elements make each simulation unique
- **Spatial Dynamics**: Growth patterns emerge from local interactions
- **Population Dynamics**: Observe exponential growth, saturation, and equilibrium
- **Edge Effects**: Bacteria at boundaries have fewer growth opportunities

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript**: No external libraries or frameworks
- **Canvas API**: Efficient rendering of 10,000 cells
- **RequestAnimationFrame**: Smooth, optimized animation
- **Responsive Design**: Works on desktop and mobile devices

## 📊 Interesting Patterns to Observe

1. **Initial Advantage**: Species that starts near the center may dominate
2. **Clustering**: Bacteria tend to form dense colonies
3. **Competition Fronts**: Watch where the two species meet
4. **Stalemates**: Sometimes species reach equilibrium with no empty space between them
5. **Rare Comebacks**: Occasionally, a nearly-extinct species can recover

## 🎯 Suggested Experiments

1. **High Growth Rate**: Set growth to 100% and watch explosive expansion
2. **Low Growth Rate**: Set to 10-20% for slow, deliberate growth
3. **Asymmetric Start**: Reset until one species has a clear advantage
4. **Speed Variations**: Try both very slow (1 gen/s) and very fast (60 gen/s)
5. **Population Impact**: Compare outcomes with 10 vs 500 initial population

## 📝 Future Enhancement Ideas

- Add mutation mechanics
- Implement death/decay over time
- Add more species (3-5 different colors)
- Allow manual placement of bacteria
- Add heat maps showing colony age
- Implement different growth strategies per species
- Add export capabilities for data analysis

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Feel free to fork, modify, and enhance this simulation! Some areas for improvement:
- More sophisticated growth algorithms
- Additional species
- Data export features
- Performance optimizations for larger grids

---

**Enjoy watching the microscopic battle unfold!** 🔬
