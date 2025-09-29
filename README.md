import matplotlib.pyplot as plt
import numpy as np

# Data
months = ["07/2019", "08/2019", "09/2019", "10/2019", "11/2019"]
searches = [50, 53, 58, 66, 62]
direct = [39, 47, 42, 51, 51]
social_media = [70, 80, 90, 87, 92]

# Bar width
bar_width = 0.25
x = np.arange(len(months))

# Plot bars
plt.bar(x - bar_width, searches, width=bar_width, label='Searches')
plt.bar(x, direct, width=bar_width, label='Direct')
plt.bar(x + bar_width, social_media, width=bar_width, label='Social Media')

# Labels & Title
plt.xlabel("months")
plt.ylabel("visitors in thousands")
plt.title("Visitors by web traffic sources")
plt.xticks(x, months)
plt.legend()

# Show the plot
plt.show()
