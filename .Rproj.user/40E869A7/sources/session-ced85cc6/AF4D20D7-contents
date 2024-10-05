# Load necessary libraries
library(ggplot2)

# Create the data frame
data <- data.frame(
  Department = c("Biotechnology", "Human Genetics", "BMS"),
  Publications = c(25, 33, 23),
  Citations = c(3773, 6111, 304),
  Faculties = c(9, 10, 11)
)

# Create the plot with dual axes and different colors for publications and citations
ggplot(data, aes(x = Department)) +
  geom_bar(aes(y = Publications, fill = "Publications"), stat = "identity", width = 0.3, position = position_nudge(x = -0.2)) +
  geom_bar(aes(y = Citations / 100, fill = "Citations"), stat = "identity", width = 0.3, position = position_nudge(x = 0)) +
  geom_bar(aes(y = Faculties * 3, fill = "Faculties"), stat = "identity", width = 0.3, position = position_nudge(x = 0.2)) +
  scale_y_continuous(
    name = "Number of Publications",
    sec.axis = sec_axis(~.*100, name = "Number of Citations")
  ) +
  scale_fill_manual(values = c("Publications" = "skyblue", "Citations" = "salmon", "Faculties" = "lightgreen")) +
  labs(title = "Publications, Citations, and Faculties by Department",
       fill = "Metric") +
  theme_minimal() +
  theme(legend.position = "top")
