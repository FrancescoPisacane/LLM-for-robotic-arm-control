#vLLM-Based High-Level Robot Control

This project explores the integration of **Large Language Models (LLMs)** into robotic high-level planning systems. By combining natural language understanding with action feasibility checks, visual perception, and spatial reasoning, it enables intuitive, zero-shot robot control using plain English instructions.

## Key Features

- **Say-Can Framework**: Combines LLM-based reasoning ("Say") with affordance evaluation ("Can") to select feasible and meaningful robot actions.
- **Prompt Engineering**: Carefully designed prompts and examples guide the LLM to output structured robot commands.
- **Visual Grounding**: The LLM receives scene descriptions generated from object detection, improving action relevance and filtering out impossible commands.
- **User Feedback Loop**: Users can accept, reject, or modify plans dynamically, with the LLM replanning accordingly—enabling adaptive behavior.
- **Spatial Reasoning**: Interprets phrases like "between top left and middle" and maps them to interpolated coordinates for precise placement.
- **Simulation Environment**: All experiments are run in a **PyBullet** environment, simulating a pick-and-place robot working with blocks and bowls.

## Technologies Used

- Python  
- OpenAI GPT (via API)  
- PyBullet  
- NumPy  
- Prompt Engineering / Zero-Shot Learning  

## Project Structure

```
── LLM_project.ipynb       # Main notebook with full implementation
── README.md               # Project overview
── LLM_report.pdf          # Full report with methodology and results
```

## Example Task

**User Input**:  
> "Put the blue block on the red block, then the green one on top of that."

**LLM Output**:  
```python
robot.pick_and_place(blue block, red block)  
robot.pick_and_place(green block, blue block)  
done()
```
