# ================================
# Project: StrikeCore
# Description:
# A high-impact repository built for fast iteration, 
# strong architecture, and projects that strike with precision and power.
# ================================

# ---------- main.py ----------
"""
Main entry points for Strikecore
"""

from core.engine import RapidEngine
from core.analysis import PrecisionAnalyzer


def run():
    print("⚡ Welcome to StrikeCore")
    print("🚀 Fast Iteration | 🧱 Strong Architecture | 🎯 Precision & Power\n")

    engine = RapidEngine()
    analyzer = PrecisionAnalyzer()

    # Fast iteration demo
    print("🔁 Rapid Prototype:", engine.iterate(lambda x: x * 3, [2, 4, 6]))

    # Precision analysis demo
    dataset = [10, 20, 30, 40, 50]
    print("🎯 Precision Score:", analyzer.precision_score(dataset))

    # Power check
    print("💥 System Impact:", engine.impact_rating(dataset))


if __name__ == "__main__":
    run()


# ---------- core/engine.py ----------
"""
Core engine for high-speed iteration and powerful operations.
"""

class RapidEngine:
    """Engine optimized for fast iteration and scalable performance."""

    def iterate(self, func, items):
        """Apply a function to items with speed-focused iteration."""
        return [func(i) for i in items]

    def impact_rating(self, data):
        """Calculate a 'power score' for a given dataset."""
        if not data:
            return 0
        peak = max(data)
        load = sum(data)
        return round((peak * 2 + load * 0.5), 2)


# ---------- core/analysis.py ----------
"""
Module focused on precision, metrics, and analytical strength.
"""

import statistics

class PrecisionAnalyzer:
    """Analyzes data for accuracy, variance, and structural integrity."""

    def precision_score(self, values):
        """Compute a precision metric based on consistency and variance."""
        if not values:
            return 0
        mean = statistics.mean(values)
        stdev = statistics.pstdev(values)
        return round(mean / (1 + stdev), 3)


# ---------- tests/test_engine.py ----------
"""
Tests for engine module.
Run with: pytest
"""

from core.engine import RapidEngine

def test_iterate():
    engine = RapidEngine()
    assert engine.iterate(lambda x: x + 1, [1, 2, 3]) == [2, 3, 4]

def test_impact_rating():
    engine = RapidEngine()
    score = engine.impact_rating([1, 2, 3])
    assert score > 0


# ---------- tests/test_analysis.py ----------
"""
Tests for analysis module.
"""

from core.analysis import PrecisionAnalyzer

def test_precision_score():
    analyzer = PrecisionAnalyzer()
    assert analyzer.precision_score([10, 20, 30]) > 0
