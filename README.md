import matplotlib.pyplot as plt

# Data
bulan = ["Januari", "Februari", "Maret", "April", "Mei", "Juni", "Juli", "Agustus", "September", "Oktober", "November", "Desember"]
penjualan = [1000, 1200, 1500, 1800, 2000, 2200, 2500, 2700, 3000, 3200, 3500, 3800]
pendapatan = [50000000, 60000000, 75000000, 90000000, 100000000, 110000000, 125000000, 135000000, 150000000, 160000000, 175000000, 190000000]

# Membuat grafik
fig, ax1 = plt.subplots(figsize=(10, 6))

# Plot data penjualan
ax1.set_xlabel('Bulan')
ax1.set_ylabel('Penjualan (Unit)', color='tab:blue')
ax1.plot(bulan, penjualan, color='tab:blue', marker='o', label='Penjualan')
ax1.tick_params(axis='y', labelcolor='tab:blue')

# Membuat axis kedua untuk pendapatan
ax2 = ax1.twinx()
ax2.set_ylabel('Pendapatan (Rp)', color='tab:green')
ax2.plot(bulan, pendapatan, color='tab:green', marker='o', label='Pendapatan')
ax2.tick_params(axis='y', labelcolor='tab:green')

# Menambahkan judul dan grid
plt.title('Penjualan dan Pendapatan Bulanan Jamu Tradisional Mashacky')
fig.tight_layout()
plt.grid(True)

# Menampilkan grafik
plt.show()
