**Project: Multimodal AI for Urban Heat Equity (SDG 11)**

**The Problem: Heat Inequity**

In many San Jose neighborhoods, extreme heat is more than just a weather issue. It affects daily life and limits community activity. We are addressing SDG 11: Sustainable Cities and Communities, specifically the Urban Heat Islands (UHI) effect.
The UHI effect disproportionately affects lower-income neighborhoods where there is a lack of vegetation and heat-trapping concrete is everywhere. For residents like Mateo, a father in East San Jose, the local playground is a "thermal red zone" where surfaces can exceed 140° degrees, making it unsafe for his children to play. 

**AI Capability: Gemini 2.5**

We used Gemini 2.5 Multimodal Recognition (Lab 3). Unlike traditional text-based 311 systems, this allows the AI to analyze and understand images. It identifies high-density materials and analyzes shade geometry from tree canopies or other structures. This turns a simple photo into a professional safety audit. In other words, in our Lab 3 testing, the AI consistently identified concrete, rubber, asphalt, and shade coverage from an uploaded image. This demonstrated that multimodal image recognition was appropriate for detecting visible Urban Heat Island risk factors. We also used Structured Data Extraction (Lab 2), which converts AI observations into structured JSON data, allowing results to be organized and easy to interpret for future applications.

**Workflow**

Our solution follows a resident-led reporting cycle:

  Input: Mateo takes a photo of a playground surface and uploads it to the audit tool for analysis
  
  AI Analysis: Gemini 2.5 uses multimodal image recognition to identify heat-retaining materials, estimate shade coverage, evaluate greenery levels, and calculate Urban Heat Island (UHI) risk conditions
  
  Output: The system generates a UHI Risk Score (1-10), structured JSON safety data, and SDG 11 cooling recommendations such as adding shade sails, trees, or reflective surfaces
  
  Action: The report is routed to city planners, prioritizing immediate cooling infrastructure improvements for dangerous thermal red zones

<img width="1658" height="948" alt="Screenshot 2026-05-10 at 3 31 36 PM" src="https://github.com/user-attachments/assets/2a6ccd18-3516-40e7-9733-7cb43098847b" />
<img width="1678" height="693" alt="Screenshot 2026-05-10 at 2 53 12 PM" src="https://github.com/user-attachments/assets/89a3a9a7-acd5-468c-a09a-7949045712ee" />
<img width="1710" height="1107" alt="Screenshot 2026-05-10 at 2 53 21 PM" src="https://github.com/user-attachments/assets/788dac05-e2ef-445e-964f-94373011996d" />


**Failure Case**

During our Lab 3 testing, we identified the "Albedo Gap." We noticed that AI may misinterpret lighter colored synthetic surfaces as cool because they look like low-heat materials, even though their high density allows them to retain extreme thermal energy. A real-world consequence involving this would be the AI giving a low UHI score to a playground that is hot enough to burn a child. This proves that visual data alone can be misleading without human intervention. In fact, in one of our runs, the AI initially described the light-colored rubber flooring as appearing “relatively safe” because of its lighter visual appearance. However, after fixing the code, the model acknowledged that the surface could still exceed burn-safe temperatures. This demonstrated that the AI relied too heavily on visual appearance without environmental context.

**Oversight and Tradeoff**

Oversight: Any report with a risk score above 7/10 or any surface identified as Synthetic Rubber must be held for mandatory human review by a city inspector before being cleared as safe.

Tradeoff: This reduces the speed of the instant audit and increases the operational cost for the city. However, this tradeoff is absolutely necessary because the cost of a delayed report is far lower than the cost of a serious child injury because of an AI mistake.
