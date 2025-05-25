# Crypto-Clustering-II

I used  the StandardScaler() module from scikit-learn to normalize the data from the CSV file then I created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame. Once, I created rows of the scaled dataframe. I found the value using K for the Scaled dataframe.The elbow method was used for the K value.I created a list with the number of k values from 1 to 11. I created  an empty list to store the inertia values. Then I created a for loop to compute the inertia with each possible value of k. I created a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

I initialized the K-means model with the best value for k, then  I fitted  the K-means model using the scaled DataFrame. Then I did a prediction, of the clusters to group the cryptocurrencies using the scaled DataFrame. A copy was created of the scaled dataframe, then a scatterplot.

{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "f7964eae-a4f0-460a-9b89-bd35f4fce010",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<script type=\"esms-options\">{\"shimMode\": true}</script><style>*[data-root-id],\n",
       "*[data-root-id] > * {\n",
       "  box-sizing: border-box;\n",
       "  font-family: var(--jp-ui-font-family);\n",
       "  font-size: var(--jp-ui-font-size1);\n",
       "  color: var(--vscode-editor-foreground, var(--jp-ui-font-color1));\n",
       "}\n",
       "\n",
       "/* Override VSCode background color */\n",
       ".cell-output-ipywidget-background:has(\n",
       "    > .cell-output-ipywidget-background > .lm-Widget > *[data-root-id]\n",
       "  ),\n",
       ".cell-output-ipywidget-background:has(> .lm-Widget > *[data-root-id]) {\n",
       "  background-color: transparent !important;\n",
       "}\n",
       "</style>"
      ]
(A snippet look)
