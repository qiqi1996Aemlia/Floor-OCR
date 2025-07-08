📌 Project: Floor Plan Segmentation and Symbol-Based Equipment Counting (for Startup Engineering Quotation)

🗂️ Inputs:
	•	A list of legend table images (containing symbols and names)
	•	A list of floor plan images (showing actual placement of symbols)

🎯 Output:
	•	A list of equipment counts, each item includes:
	•	Custom ID
	•	Name
	•	Quantity detected across the floor plans

🛠️ Tools Allowed:
	•	Open-source libraries and public APIs may be used

⏱️ Timeline:
	•	Delivery deadline: within 3 days

⸻

🔧 Implementation Plan

1. Legend Table Recognition
	•	Table line detection: Use Surya-API to extract table boundaries
	•	Text recognition: Use PaddleOCR to extract names or labels
	•	Symbol detection: Use color-based + contour extraction to isolate icon patches

2. Symbol Recognition in Floor Plans
	•	Symbol detection: Again use color filtering + contour detection
	•	Symbol classification: Use vector-based similarity, such as:
	•	CLIP (Contrastive Language–Image Pretraining)
	•	ViT (Vision Transformer) for robust visual encoding

3. Current Challenges
	•	Visually similar components:
	•	Need fine-grained classification (e.g., rectangular vs circular symbols)
	•	Overlapping symbols:
	•	Hard to distinguish with basic matching

4. Proposed Solutions
	•	Synthetic data generation based on legend symbols
	•	Render synthetic floor plan patches with known symbol placements
	•	Train a detection or segmentation model (e.g., YOLO, Mask R-CNN) on this synthetic dataset for fine-grained recognition and counting
