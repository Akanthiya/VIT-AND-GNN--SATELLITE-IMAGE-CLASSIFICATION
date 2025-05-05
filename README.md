# VIT-AND-GNN--SATELLITE-IMAGE-CLASSIFICATIONThe model uses a Vision Transformer (ViT) to extract rich global features from satellite images by dividing each image into fixed-size patches.

Each patch is embedded and processed using self-attention to capture contextual dependencies across the image.

The output of the ViT model (CLS token or patch embeddings) is used as a feature vector for each image.

These image-level features become nodes in a graph, where each node represents a satellite image.

A Graph Neural Network (GNN) models the relationships between images by connecting similar or geographically nearby nodes.

Edges between nodes are defined based on metadata like spatial proximity or visual similarity.

The GNN propagates information across nodes, helping the model learn inter-image relationships.

A classifier on top of the GNN outputs the final land cover class for each image (e.g., forest, water, urban).

This hybrid ViT-GNN model combines local pixel details and global spatial relationships, improving classification accuracy.

The system is evaluated using metrics like accuracy, precision, recall, and F1-score, providing robust performance on satellite imagery tasks.
