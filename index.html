import { useState, useEffect, useRef } from "react";

// ─── DESIGN TOKENS ─────────────────────────────────────────────────────────
// Palette: warm cream base, deep charcoal type, vivid coral accent, soft sage secondary
// Font: Fraunces (display) + DM Sans (body)

const COLORS = {
  bg: "#F7F5F0",
  card: "#FFFFFF",
  accent: "#FF5C3A",
  accentLight: "#FFF0ED",
  accentSoft: "#FFD6CE",
  sage: "#4CAF7D",
  sageLight: "#E8F5EE",
  ink: "#1A1A2E",
  muted: "#8A8A9A",
  border: "#EDEAE4",
  danger: "#FF3B5C",
  gold: "#F5A623",
  goldLight: "#FEF6E8",
};

// ─── GLOBAL STYLES ─────────────────────────────────────────────────────────
const GlobalStyles = () => (
  <style>{`
    @import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,400;0,600;0,700;1,400&family=DM+Sans:wght@300;400;500;600&display=swap');
    
    * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
    
    body {
      background: ${COLORS.bg};
      font-family: 'DM Sans', sans-serif;
      color: ${COLORS.ink};
      min-height: 100vh;
      overflow-x: hidden;
    }

    .app-shell {
      max-width: 430px;
      margin: 0 auto;
      min-height: 100vh;
      background: ${COLORS.bg};
      position: relative;
      overflow: hidden;
    }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 0; }

    /* Screen transitions */
    .screen {
      min-height: 100vh;
      padding-bottom: 100px;
      animation: slideUp 0.32s cubic-bezier(0.22, 1, 0.36, 1);
    }
    @keyframes slideUp {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* Cards */
    .card {
      background: ${COLORS.card};
      border-radius: 20px;
      padding: 18px;
      box-shadow: 0 2px 12px rgba(26,26,46,0.06);
    }

    /* Buttons */
    .btn-primary {
      background: ${COLORS.accent};
      color: #fff;
      border: none;
      border-radius: 16px;
      padding: 16px 24px;
      font-family: 'DM Sans', sans-serif;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      width: 100%;
      transition: transform 0.12s, opacity 0.12s;
      letter-spacing: 0.01em;
    }
    .btn-primary:active { transform: scale(0.97); opacity: 0.9; }

    .btn-secondary {
      background: ${COLORS.accentLight};
      color: ${COLORS.accent};
      border: none;
      border-radius: 16px;
      padding: 14px 24px;
      font-family: 'DM Sans', sans-serif;
      font-size: 15px;
      font-weight: 600;
      cursor: pointer;
      width: 100%;
      transition: transform 0.12s;
    }
    .btn-secondary:active { transform: scale(0.97); }

    .btn-ghost {
      background: transparent;
      color: ${COLORS.muted};
      border: 1.5px solid ${COLORS.border};
      border-radius: 14px;
      padding: 12px 20px;
      font-family: 'DM Sans', sans-serif;
      font-size: 14px;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.12s;
    }
    .btn-ghost:active { background: ${COLORS.border}; }

    /* Inputs */
    .input-field {
      width: 100%;
      background: ${COLORS.bg};
      border: 1.5px solid ${COLORS.border};
      border-radius: 14px;
      padding: 14px 16px;
      font-family: 'DM Sans', sans-serif;
      font-size: 16px;
      color: ${COLORS.ink};
      outline: none;
      transition: border-color 0.2s;
      -webkit-appearance: none;
    }
    .input-field:focus { border-color: ${COLORS.accent}; background: #fff; }
    .input-field::placeholder { color: ${COLORS.muted}; }

    /* Tags */
    .tag {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      padding: 6px 12px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 500;
    }

    /* Avatar */
    .avatar {
      width: 40px; height: 40px;
      border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      font-size: 15px;
      font-weight: 600;
      flex-shrink: 0;
    }

    /* Bottom Nav */
    .bottom-nav {
      position: fixed;
      bottom: 0; left: 50%;
      transform: translateX(-50%);
      width: 100%;
      max-width: 430px;
      background: rgba(255,255,255,0.92);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border-top: 1px solid ${COLORS.border};
      padding: 12px 0 24px;
      z-index: 100;
      display: flex;
      justify-content: space-around;
    }

    .nav-item {
      display: flex; flex-direction: column; align-items: center; gap: 3px;
      cursor: pointer; padding: 4px 16px;
      transition: transform 0.12s;
      border: none; background: none;
    }
    .nav-item:active { transform: scale(0.9); }
    .nav-icon { font-size: 22px; line-height: 1; }
    .nav-label { font-size: 10px; font-weight: 500; }

    /* Amount display */
    .amount-big {
      font-family: 'Fraunces', serif;
      font-size: 40px;
      font-weight: 700;
      letter-spacing: -1px;
      line-height: 1;
    }

    /* Progress bar */
    .progress-track {
      background: ${COLORS.border};
      border-radius: 100px;
      height: 8px;
      overflow: hidden;
    }
    .progress-fill {
      height: 100%;
      border-radius: 100px;
      background: ${COLORS.sage};
      transition: width 0.6s cubic-bezier(0.22, 1, 0.36, 1);
    }

    /* Pill selector */
    .pill-group {
      display: flex;
      background: ${COLORS.bg};
      border-radius: 14px;
      padding: 4px;
      gap: 2px;
    }
    .pill-option {
      flex: 1;
      padding: 10px 8px;
      border-radius: 11px;
      border: none;
      background: transparent;
      font-family: 'DM Sans', sans-serif;
      font-size: 13px;
      font-weight: 500;
      color: ${COLORS.muted};
      cursor: pointer;
      transition: all 0.18s;
      text-align: center;
    }
    .pill-option.active {
      background: ${COLORS.card};
      color: ${COLORS.accent};
      font-weight: 600;
      box-shadow: 0 2px 8px rgba(26,26,46,0.08);
    }

    /* Checkbox */
    .check-circle {
      width: 24px; height: 24px;
      border-radius: 50%;
      border: 2px solid ${COLORS.border};
      display: flex; align-items: center; justify-content: center;
      cursor: pointer;
      transition: all 0.15s;
      flex-shrink: 0;
    }
    .check-circle.checked {
      background: ${COLORS.sage};
      border-color: ${COLORS.sage};
      color: white;
    }

    /* Sheet overlay */
    .sheet-overlay {
      position: fixed; inset: 0;
      background: rgba(26,26,46,0.4);
      z-index: 200;
      display: flex; align-items: flex-end;
      animation: fadeIn 0.2s ease;
    }
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    .sheet {
      width: 100%;
      max-width: 430px;
      margin: 0 auto;
      background: ${COLORS.card};
      border-radius: 28px 28px 0 0;
      padding: 24px 24px 40px;
      animation: sheetUp 0.3s cubic-bezier(0.22, 1, 0.36, 1);
    }
    @keyframes sheetUp {
      from { transform: translateY(100%); }
      to   { transform: translateY(0); }
    }

    .sheet-handle {
      width: 36px; height: 4px;
      background: ${COLORS.border};
      border-radius: 100px;
      margin: 0 auto 20px;
    }

    /* Toast */
    .toast {
      position: fixed;
      top: 60px; left: 50%;
      transform: translateX(-50%);
      background: ${COLORS.ink};
      color: white;
      padding: 12px 20px;
      border-radius: 100px;
      font-size: 14px;
      font-weight: 500;
      z-index: 999;
      white-space: nowrap;
      animation: toastIn 0.3s cubic-bezier(0.22, 1, 0.36, 1);
      box-shadow: 0 4px 20px rgba(26,26,46,0.2);
    }
    @keyframes toastIn {
      from { opacity: 0; transform: translate(-50%, -8px); }
      to   { opacity: 1; transform: translate(-50%, 0); }
    }

    /* Divider */
    .divider { height: 1px; background: ${COLORS.border}; margin: 4px 0; }

    /* Label */
    .label {
      font-size: 12px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: ${COLORS.muted};
      margin-bottom: 8px;
    }

    /* Swipe hint */
    .swipe-row {
      display: flex; align-items: center;
      padding: 14px 16px;
      background: white;
      border-radius: 16px;
      gap: 12px;
      box-shadow: 0 1px 6px rgba(26,26,46,0.05);
      cursor: pointer;
      transition: transform 0.12s;
      margin-bottom: 8px;
    }
    .swipe-row:active { transform: scale(0.98); }
  `}</style>
);

// ─── AVATAR COLORS ─────────────────────────────────────────────────────────
const AVATAR_COLORS = [
  ["#FFD6CE", "#FF5C3A"], ["#D6E8FF", "#2563EB"], ["#D6F5E3", "#16A34A"],
  ["#FEF3C7", "#D97706"], ["#EDE9FE", "#7C3AED"], ["#FCE7F3", "#DB2777"],
  ["#CCFBF1", "#0D9488"], ["#FEE2E2", "#DC2626"],
];
const getAvatarColors = (i) => AVATAR_COLORS[i % AVATAR_COLORS.length];

// ─── HELPERS ────────────────────────────────────────────────────────────────
const fmt = (n) => `$${Math.abs(n).toFixed(2)}`;
const uid = () => Math.random().toString(36).slice(2, 9);

function computeBalances(members, expenses) {
  const bal = {};
  members.forEach((m) => (bal[m.id] = 0));

  expenses.forEach((exp) => {
    const amt = parseFloat(exp.amount) || 0;
    if (!amt) return;
    const involvedIds = exp.participants || members.map((m) => m.id);

    // Credit payer
    bal[exp.paidById] = (bal[exp.paidById] || 0) + amt;

    // Debit each participant their share
    if (exp.splitType === "equal") {
      const share = amt / involvedIds.length;
      involvedIds.forEach((id) => { bal[id] = (bal[id] || 0) - share; });
    } else if (exp.splitType === "percentage") {
      involvedIds.forEach((id) => {
        const pct = (exp.percentages?.[id] || 0) / 100;
        bal[id] = (bal[id] || 0) - amt * pct;
      });
    } else if (exp.splitType === "custom") {
      involvedIds.forEach((id) => {
        const share = parseFloat(exp.customAmounts?.[id]) || 0;
        bal[id] = (bal[id] || 0) - share;
      });
    }
  });
  return bal;
}

function simplifyDebts(balances) {
  // Greedy settlement algorithm
  const pos = [], neg = [];
  Object.entries(balances).forEach(([id, b]) => {
    if (b > 0.005) pos.push({ id, b });
    else if (b < -0.005) neg.push({ id, b: -b });
  });
  const txns = [];
  let pi = 0, ni = 0;
  while (pi < pos.length && ni < neg.length) {
    const p = pos[pi], n = neg[ni];
    const amt = Math.min(p.b, n.b);
    txns.push({ from: n.id, to: p.id, amount: amt });
    p.b -= amt; n.b -= amt;
    if (p.b < 0.005) pi++;
    if (n.b < 0.005) ni++;
  }
  return txns;
}

// ─── EMOJI CATEGORIES ───────────────────────────────────────────────────────
const EXPENSE_EMOJIS = [
  { e: "🍽️", l: "Food" }, { e: "🍕", l: "Pizza" }, { e: "🍺", l: "Drinks" },
  { e: "🛒", l: "Groceries" }, { e: "🚗", l: "Transport" }, { e: "🏠", l: "Rent" },
  { e: "✈️", l: "Travel" }, { e: "🎬", l: "Fun" }, { e: "💊", l: "Health" },
  { e: "🎁", l: "Gift" }, { e: "⚡", l: "Utilities" }, { e: "📦", l: "Other" },
];

// ═══════════════════════════════════════════════════════════════════════════
// SCREENS
// ═══════════════════════════════════════════════════════════════════════════

// ── HOME SCREEN ─────────────────────────────────────────────────────────────
function HomeScreen({ groups, onSelectGroup, onCreateGroup }) {
  const totalOwed = groups.reduce((acc, g) => {
    const bals = computeBalances(g.members, g.expenses);
    // "you" is always index 0
    return acc + (bals[g.members[0]?.id] || 0);
  }, 0);

  return (
    <div className="screen" style={{ padding: "0 0 80px" }}>
      {/* Hero header */}
      <div style={{
        background: `linear-gradient(145deg, ${COLORS.ink} 0%, #2D2D4E 100%)`,
        padding: "64px 24px 32px",
        position: "relative",
        overflow: "hidden",
      }}>
        {/* Decorative blobs */}
        <div style={{
          position: "absolute", top: -40, right: -40,
          width: 180, height: 180, borderRadius: "50%",
          background: `radial-gradient(circle, ${COLORS.accent}44, transparent 70%)`,
        }} />
        <div style={{
          position: "absolute", bottom: -20, left: 20,
          width: 120, height: 120, borderRadius: "50%",
          background: `radial-gradient(circle, ${COLORS.sage}33, transparent 70%)`,
        }} />

        <p style={{ color: "rgba(255,255,255,0.5)", fontSize: 13, fontWeight: 500, marginBottom: 4 }}>
          Good day 👋
        </p>
        <h1 style={{
          fontFamily: "'Fraunces', serif",
          color: "white", fontSize: 32, fontWeight: 700,
          lineHeight: 1.1, marginBottom: 24,
        }}>
          Split<span style={{ color: COLORS.accent }}>Easy</span>
        </h1>

        {/* Balance card */}
        <div style={{
          background: "rgba(255,255,255,0.1)",
          backdropFilter: "blur(10px)",
          borderRadius: 20,
          padding: "18px 20px",
          border: "1px solid rgba(255,255,255,0.12)",
        }}>
          <p style={{ color: "rgba(255,255,255,0.6)", fontSize: 12, fontWeight: 600, textTransform: "uppercase", letterSpacing: "0.08em", marginBottom: 6 }}>
            Your Net Balance
          </p>
          <div style={{ display: "flex", alignItems: "baseline", gap: 8 }}>
            <span style={{
              fontFamily: "'Fraunces', serif",
              fontSize: 38, fontWeight: 700,
              color: totalOwed >= 0 ? COLORS.sage : COLORS.danger,
              lineHeight: 1,
            }}>
              {totalOwed >= 0 ? "+" : "-"}{fmt(totalOwed)}
            </span>
            <span style={{ color: "rgba(255,255,255,0.5)", fontSize: 13 }}>
              {totalOwed >= 0 ? "you're owed" : "you owe"}
            </span>
          </div>
        </div>
      </div>

      <div style={{ padding: "24px 16px" }}>
        {/* Groups */}
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 16 }}>
          <h2 style={{ fontFamily: "'Fraunces', serif", fontSize: 22, fontWeight: 600 }}>
            Groups
          </h2>
          <button className="btn-ghost" style={{ width: "auto", padding: "8px 16px", fontSize: 13 }}
            onClick={onCreateGroup}>
            + New
          </button>
        </div>

        {groups.length === 0 && (
          <div style={{ textAlign: "center", padding: "48px 24px" }}>
            <div style={{ fontSize: 48, marginBottom: 12 }}>🤝</div>
            <p style={{ fontFamily: "'Fraunces', serif", fontSize: 20, fontWeight: 600, marginBottom: 8 }}>
              No groups yet
            </p>
            <p style={{ color: COLORS.muted, fontSize: 14, marginBottom: 24 }}>
              Create a group to start splitting expenses with friends.
            </p>
            <button className="btn-primary" onClick={onCreateGroup}>
              Create First Group
            </button>
          </div>
        )}

        <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
          {groups.map((g, gi) => {
            const bals = computeBalances(g.members, g.expenses);
            const myBal = bals[g.members[0]?.id] || 0;
            const total = g.expenses.reduce((a, e) => a + (parseFloat(e.amount) || 0), 0);
            return (
              <div key={g.id} className="swipe-row" onClick={() => onSelectGroup(g.id)}>
                <div style={{
                  width: 48, height: 48, borderRadius: 16,
                  background: `linear-gradient(135deg, ${COLORS.accent}22, ${COLORS.accent}44)`,
                  display: "flex", alignItems: "center", justifyContent: "center",
                  fontSize: 22, flexShrink: 0,
                }}>
                  {g.emoji || "👥"}
                </div>
                <div style={{ flex: 1, minWidth: 0 }}>
                  <p style={{ fontWeight: 600, fontSize: 15, marginBottom: 2 }}>{g.name}</p>
                  <p style={{ color: COLORS.muted, fontSize: 12 }}>
                    {g.members.length} people · {fmt(total)} total
                  </p>
                </div>
                <div style={{ textAlign: "right" }}>
                  <p style={{
                    fontFamily: "'Fraunces', serif",
                    fontSize: 16, fontWeight: 700,
                    color: myBal >= 0 ? COLORS.sage : COLORS.danger,
                  }}>
                    {myBal >= 0 ? "+" : ""}{fmt(myBal)}
                  </p>
                  <p style={{ color: COLORS.muted, fontSize: 11 }}>
                    {myBal >= 0 ? "owed to you" : "you owe"}
                  </p>
                </div>
              </div>
            );
          })}
        </div>
      </div>
    </div>
  );
}

// ── CREATE GROUP SCREEN ──────────────────────────────────────────────────────
function CreateGroupScreen({ onBack, onCreate }) {
  const [name, setName] = useState("");
  const [emoji, setEmoji] = useState("👥");
  const [friends, setFriends] = useState([{ id: uid(), name: "" }]);
  const EMOJIS = ["👥", "🍕", "✈️", "🏠", "🎉", "🎮", "🏋️", "🚗", "🎸", "🌴"];

  const addFriend = () => setFriends([...friends, { id: uid(), name: "" }]);
  const updateFriend = (i, val) => {
    const f = [...friends]; f[i].name = val; setFriends(f);
  };
  const removeFriend = (i) => {
    if (friends.length > 1) setFriends(friends.filter((_, idx) => idx !== i));
  };

  const handleCreate = () => {
    if (!name.trim()) return;
    const validFriends = friends.filter((f) => f.name.trim());
    const youMember = { id: uid(), name: "You", isMe: true };
    const members = [youMember, ...validFriends.map((f) => ({ ...f, name: f.name.trim() }))];
    onCreate({ id: uid(), name: name.trim(), emoji, members, expenses: [] });
  };

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      {/* Header */}
      <div style={{ padding: "56px 20px 20px", display: "flex", alignItems: "center", gap: 12 }}>
        <button onClick={onBack} style={{ background: COLORS.bg, border: "none", width: 40, height: 40, borderRadius: 12, cursor: "pointer", fontSize: 18, display: "flex", alignItems: "center", justifyContent: "center" }}>←</button>
        <h1 style={{ fontFamily: "'Fraunces', serif", fontSize: 26, fontWeight: 700 }}>New Group</h1>
      </div>

      <div style={{ padding: "0 20px", display: "flex", flexDirection: "column", gap: 20 }}>
        {/* Emoji picker */}
        <div className="card">
          <p className="label">Group Icon</p>
          <div style={{ display: "flex", flexWrap: "wrap", gap: 8 }}>
            {EMOJIS.map((e) => (
              <button key={e} onClick={() => setEmoji(e)} style={{
                width: 48, height: 48, borderRadius: 14, fontSize: 22,
                border: `2px solid ${emoji === e ? COLORS.accent : "transparent"}`,
                background: emoji === e ? COLORS.accentLight : COLORS.bg,
                cursor: "pointer", transition: "all 0.15s",
              }}>{e}</button>
            ))}
          </div>
        </div>

        {/* Name */}
        <div className="card">
          <p className="label">Group Name</p>
          <input className="input-field" placeholder="e.g. Bali Trip 2026"
            value={name} onChange={(e) => setName(e.target.value)} />
        </div>

        {/* Members */}
        <div className="card">
          <p className="label">Add Friends</p>
          <p style={{ fontSize: 13, color: COLORS.muted, marginBottom: 12 }}>
            You're already included automatically.
          </p>
          <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
            {friends.map((f, i) => (
              <div key={f.id} style={{ display: "flex", gap: 8 }}>
                <input className="input-field" placeholder={`Friend ${i + 1} name`}
                  value={f.name} onChange={(e) => updateFriend(i, e.target.value)}
                  style={{ flex: 1 }} />
                {friends.length > 1 && (
                  <button onClick={() => removeFriend(i)} style={{
                    background: COLORS.bg, border: "none", borderRadius: 12,
                    width: 48, height: 48, cursor: "pointer", color: COLORS.danger,
                    fontSize: 18, flexShrink: 0,
                  }}>×</button>
                )}
              </div>
            ))}
            <button className="btn-ghost" onClick={addFriend} style={{ marginTop: 4 }}>
              + Add another friend
            </button>
          </div>
        </div>

        <button className="btn-primary" onClick={handleCreate}
          disabled={!name.trim()}
          style={{ opacity: name.trim() ? 1 : 0.5 }}>
          Create Group 🎉
        </button>
      </div>
    </div>
  );
}

// ── GROUP DETAIL SCREEN ──────────────────────────────────────────────────────
function GroupScreen({ group, onBack, onAddExpense, onViewSummary, onUpdateGroup, onInstallments }) {
  const balances = computeBalances(group.members, group.expenses);
  const myId = group.members[0]?.id;
  const myBal = balances[myId] || 0;

  const deleteExpense = (eid) => {
    onUpdateGroup({ ...group, expenses: group.expenses.filter((e) => e.id !== eid) });
  };

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      {/* Header */}
      <div style={{
        background: `linear-gradient(135deg, ${COLORS.ink} 0%, #252545 100%)`,
        padding: "56px 20px 28px",
      }}>
        <div style={{ display: "flex", alignItems: "center", gap: 12, marginBottom: 20 }}>
          <button onClick={onBack} style={{ background: "rgba(255,255,255,0.12)", border: "none", width: 38, height: 38, borderRadius: 12, cursor: "pointer", fontSize: 16, color: "white", display: "flex", alignItems: "center", justifyContent: "center" }}>←</button>
          <div style={{ fontSize: 28 }}>{group.emoji}</div>
          <div>
            <h1 style={{ fontFamily: "'Fraunces', serif", color: "white", fontSize: 22, fontWeight: 700, lineHeight: 1 }}>{group.name}</h1>
            <p style={{ color: "rgba(255,255,255,0.5)", fontSize: 12, marginTop: 2 }}>{group.members.length} members</p>
          </div>
        </div>

        {/* Members row */}
        <div style={{ display: "flex", gap: 8, marginBottom: 20 }}>
          {group.members.map((m, i) => {
            const [bg, txt] = getAvatarColors(i);
            return (
              <div key={m.id} style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 4 }}>
                <div className="avatar" style={{ background: bg, color: txt, width: 36, height: 36, fontSize: 13 }}>
                  {m.isMe ? "You" : m.name.slice(0, 2).toUpperCase()}
                </div>
                <span style={{ color: "rgba(255,255,255,0.6)", fontSize: 10, fontWeight: 500 }}>
                  {m.isMe ? "You" : m.name.split(" ")[0]}
                </span>
              </div>
            );
          })}
        </div>

        {/* My balance */}
        <div style={{
          background: "rgba(255,255,255,0.08)", borderRadius: 16,
          padding: "14px 16px", border: "1px solid rgba(255,255,255,0.1)",
          display: "flex", justifyContent: "space-between", alignItems: "center",
        }}>
          <span style={{ color: "rgba(255,255,255,0.6)", fontSize: 13 }}>Your balance</span>
          <span style={{ fontFamily: "'Fraunces', serif", fontSize: 22, fontWeight: 700, color: myBal >= 0 ? COLORS.sage : COLORS.danger }}>
            {myBal >= 0 ? "+" : ""}{fmt(myBal)}
          </span>
        </div>
      </div>

      <div style={{ padding: "20px 16px", display: "flex", flexDirection: "column", gap: 10 }}>
        {/* Action buttons */}
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr 1fr", gap: 8 }}>
          {[
            { icon: "➕", label: "Add Expense", fn: onAddExpense },
            { icon: "📊", label: "Summary", fn: onViewSummary },
            { icon: "📅", label: "Installments", fn: onInstallments },
          ].map(({ icon, label, fn }) => (
            <button key={label} onClick={fn} style={{
              background: COLORS.card, border: "none", borderRadius: 16,
              padding: "14px 8px", cursor: "pointer",
              display: "flex", flexDirection: "column", alignItems: "center", gap: 6,
              boxShadow: "0 2px 10px rgba(26,26,46,0.06)",
              transition: "transform 0.12s",
            }}
              onMouseDown={(e) => e.currentTarget.style.transform = "scale(0.96)"}
              onMouseUp={(e) => e.currentTarget.style.transform = "scale(1)"}
              onTouchStart={(e) => e.currentTarget.style.transform = "scale(0.96)"}
              onTouchEnd={(e) => e.currentTarget.style.transform = "scale(1)"}
            >
              <span style={{ fontSize: 24 }}>{icon}</span>
              <span style={{ fontSize: 11, fontWeight: 600, color: COLORS.muted }}>{label}</span>
            </button>
          ))}
        </div>

        {/* Expenses list */}
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginTop: 8 }}>
          <h3 style={{ fontFamily: "'Fraunces', serif", fontSize: 18, fontWeight: 600 }}>Expenses</h3>
          <span style={{ color: COLORS.muted, fontSize: 13 }}>{group.expenses.length} items</span>
        </div>

        {group.expenses.length === 0 && (
          <div style={{ textAlign: "center", padding: "32px", color: COLORS.muted }}>
            <div style={{ fontSize: 36, marginBottom: 8 }}>🧾</div>
            <p style={{ fontSize: 14 }}>No expenses yet. Add one!</p>
          </div>
        )}

        {[...group.expenses].reverse().map((exp) => {
          const payer = group.members.find((m) => m.id === exp.paidById);
          const payerName = payer?.isMe ? "You" : payer?.name || "?";
          return (
            <div key={exp.id} className="swipe-row" style={{ position: "relative" }}>
              <div style={{
                width: 44, height: 44, borderRadius: 14,
                background: COLORS.accentLight,
                display: "flex", alignItems: "center", justifyContent: "center",
                fontSize: 20, flexShrink: 0,
              }}>
                {exp.emoji}
              </div>
              <div style={{ flex: 1, minWidth: 0 }}>
                <p style={{ fontWeight: 600, fontSize: 14, marginBottom: 1 }}>{exp.title}</p>
                <p style={{ color: COLORS.muted, fontSize: 12 }}>
                  {payerName} paid · {exp.splitType}
                </p>
              </div>
              <div style={{ textAlign: "right" }}>
                <p style={{ fontFamily: "'Fraunces', serif", fontSize: 17, fontWeight: 700 }}>
                  {fmt(exp.amount)}
                </p>
                <button onClick={(e) => { e.stopPropagation(); deleteExpense(exp.id); }}
                  style={{ background: "none", border: "none", color: COLORS.danger, fontSize: 11, cursor: "pointer", padding: "2px 0" }}>
                  Remove
                </button>
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
}

// ── ADD EXPENSE SCREEN ───────────────────────────────────────────────────────
function AddExpenseScreen({ group, onBack, onAdd }) {
  const [title, setTitle] = useState("");
  const [amount, setAmount] = useState("");
  const [emoji, setEmoji] = useState("🍽️");
  const [paidById, setPaidById] = useState(group.members[0]?.id);
  const [splitType, setSplitType] = useState("equal");
  const [participants, setParticipants] = useState(group.members.map((m) => m.id));
  const [customAmounts, setCustomAmounts] = useState({});
  const [percentages, setPercentages] = useState({});
  const [showEmojiPicker, setShowEmojiPicker] = useState(false);

  const toggleParticipant = (id) => {
    setParticipants((prev) =>
      prev.includes(id) ? prev.filter((x) => x !== id) : [...prev, id]
    );
  };

  const totalAmt = parseFloat(amount) || 0;
  const equalShare = participants.length ? totalAmt / participants.length : 0;
  const customTotal = Object.values(customAmounts).reduce((a, b) => a + (parseFloat(b) || 0), 0);
  const pctTotal = Object.values(percentages).reduce((a, b) => a + (parseFloat(b) || 0), 0);

  const isValid = title.trim() && totalAmt > 0 && participants.length > 0;

  const handleAdd = () => {
    if (!isValid) return;
    onAdd({
      id: uid(), title: title.trim(), amount: totalAmt, emoji,
      paidById, splitType, participants,
      customAmounts: splitType === "custom" ? customAmounts : {},
      percentages: splitType === "percentage" ? percentages : {},
      date: new Date().toISOString(),
    });
  };

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      <div style={{ padding: "56px 20px 16px", display: "flex", alignItems: "center", gap: 12 }}>
        <button onClick={onBack} style={{ background: COLORS.bg, border: "none", width: 40, height: 40, borderRadius: 12, cursor: "pointer", fontSize: 18, display: "flex", alignItems: "center", justifyContent: "center" }}>←</button>
        <h1 style={{ fontFamily: "'Fraunces', serif", fontSize: 24, fontWeight: 700 }}>Add Expense</h1>
      </div>

      <div style={{ padding: "0 20px", display: "flex", flexDirection: "column", gap: 16 }}>

        {/* Amount hero */}
        <div className="card" style={{ textAlign: "center", padding: "28px 20px" }}>
          <p className="label" style={{ marginBottom: 12 }}>Amount</p>
          <div style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 4 }}>
            <span style={{ fontFamily: "'Fraunces', serif", fontSize: 36, fontWeight: 700, color: COLORS.muted }}>$</span>
            <input
              type="number" inputMode="decimal" placeholder="0.00"
              value={amount} onChange={(e) => setAmount(e.target.value)}
              style={{
                fontFamily: "'Fraunces', serif", fontSize: 48, fontWeight: 700,
                border: "none", background: "transparent", outline: "none",
                width: "180px", color: COLORS.ink, textAlign: "center",
              }}
            />
          </div>
        </div>

        {/* Title + emoji */}
        <div className="card">
          <p className="label">Description</p>
          <div style={{ display: "flex", gap: 10 }}>
            <button onClick={() => setShowEmojiPicker(true)} style={{
              width: 52, height: 52, borderRadius: 14, fontSize: 24,
              background: COLORS.bg, border: `1.5px solid ${COLORS.border}`,
              cursor: "pointer", flexShrink: 0,
            }}>{emoji}</button>
            <input className="input-field" placeholder="What's this for?"
              value={title} onChange={(e) => setTitle(e.target.value)} />
          </div>
        </div>

        {/* Paid by */}
        <div className="card">
          <p className="label">Paid by</p>
          <div style={{ display: "flex", gap: 8, flexWrap: "wrap" }}>
            {group.members.map((m, i) => {
              const [bg, txt] = getAvatarColors(i);
              const selected = paidById === m.id;
              return (
                <button key={m.id} onClick={() => setPaidById(m.id)} style={{
                  display: "flex", alignItems: "center", gap: 8,
                  padding: "8px 14px", borderRadius: 100,
                  border: `2px solid ${selected ? COLORS.accent : COLORS.border}`,
                  background: selected ? COLORS.accentLight : "white",
                  cursor: "pointer", transition: "all 0.15s",
                }}>
                  <div className="avatar" style={{ width: 28, height: 28, fontSize: 11, background: bg, color: txt }}>
                    {m.isMe ? "Me" : m.name.slice(0, 2).toUpperCase()}
                  </div>
                  <span style={{ fontSize: 13, fontWeight: 600, color: selected ? COLORS.accent : COLORS.ink }}>
                    {m.isMe ? "You" : m.name}
                  </span>
                </button>
              );
            })}
          </div>
        </div>

        {/* Split type */}
        <div className="card">
          <p className="label">Split Method</p>
          <div className="pill-group">
            {["equal", "custom", "percentage"].map((type) => (
              <button key={type} className={`pill-option ${splitType === type ? "active" : ""}`}
                onClick={() => setSplitType(type)}>
                {type === "equal" ? "Equal" : type === "custom" ? "Custom $" : "By %"}
              </button>
            ))}
          </div>

          {/* Participants */}
          <div style={{ marginTop: 16, display: "flex", flexDirection: "column", gap: 8 }}>
            <p className="label">Include</p>
            {group.members.map((m, i) => {
              const [bg, txt] = getAvatarColors(i);
              const inc = participants.includes(m.id);
              return (
                <div key={m.id} style={{ display: "flex", alignItems: "center", gap: 10, padding: "8px 0" }}>
                  <div onClick={() => toggleParticipant(m.id)} className={`check-circle ${inc ? "checked" : ""}`}>
                    {inc && <span style={{ fontSize: 13 }}>✓</span>}
                  </div>
                  <div className="avatar" style={{ background: bg, color: txt }}>{m.isMe ? "Me" : m.name.slice(0, 2).toUpperCase()}</div>
                  <span style={{ flex: 1, fontWeight: 500 }}>{m.isMe ? "You" : m.name}</span>
                  {splitType === "equal" && inc && (
                    <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, color: COLORS.accent }}>
                      {fmt(equalShare)}
                    </span>
                  )}
                  {splitType === "custom" && inc && (
                    <input type="number" inputMode="decimal" placeholder="0.00"
                      value={customAmounts[m.id] || ""}
                      onChange={(e) => setCustomAmounts({ ...customAmounts, [m.id]: e.target.value })}
                      style={{ width: 80, textAlign: "right", fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 15, border: `1.5px solid ${COLORS.border}`, borderRadius: 10, padding: "6px 10px", outline: "none", background: COLORS.bg }}
                    />
                  )}
                  {splitType === "percentage" && inc && (
                    <div style={{ display: "flex", alignItems: "center", gap: 2 }}>
                      <input type="number" inputMode="decimal" placeholder="0"
                        value={percentages[m.id] || ""}
                        onChange={(e) => setPercentages({ ...percentages, [m.id]: e.target.value })}
                        style={{ width: 60, textAlign: "right", fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 15, border: `1.5px solid ${COLORS.border}`, borderRadius: 10, padding: "6px 8px", outline: "none", background: COLORS.bg }}
                      />
                      <span style={{ color: COLORS.muted, fontSize: 13 }}>%</span>
                    </div>
                  )}
                </div>
              );
            })}
          </div>

          {splitType === "custom" && (
            <div style={{ display: "flex", justifyContent: "space-between", marginTop: 8, padding: "10px 0 0", borderTop: `1px solid ${COLORS.border}` }}>
              <span style={{ color: COLORS.muted, fontSize: 13 }}>Assigned</span>
              <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, color: Math.abs(customTotal - totalAmt) < 0.01 ? COLORS.sage : COLORS.danger }}>
                {fmt(customTotal)} / {fmt(totalAmt)}
              </span>
            </div>
          )}
          {splitType === "percentage" && (
            <div style={{ display: "flex", justifyContent: "space-between", marginTop: 8, padding: "10px 0 0", borderTop: `1px solid ${COLORS.border}` }}>
              <span style={{ color: COLORS.muted, fontSize: 13 }}>Total %</span>
              <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, color: Math.abs(pctTotal - 100) < 0.5 ? COLORS.sage : COLORS.danger }}>
                {pctTotal.toFixed(0)}%
              </span>
            </div>
          )}
        </div>

        <button className="btn-primary" onClick={handleAdd}
          disabled={!isValid}
          style={{ opacity: isValid ? 1 : 0.5 }}>
          Add Expense ✓
        </button>
      </div>

      {/* Emoji picker sheet */}
      {showEmojiPicker && (
        <div className="sheet-overlay" onClick={() => setShowEmojiPicker(false)}>
          <div className="sheet" onClick={(e) => e.stopPropagation()}>
            <div className="sheet-handle" />
            <p style={{ fontFamily: "'Fraunces', serif", fontSize: 20, fontWeight: 700, marginBottom: 16 }}>Choose Emoji</p>
            <div style={{ display: "flex", flexWrap: "wrap", gap: 10 }}>
              {EXPENSE_EMOJIS.map(({ e, l }) => (
                <button key={e} onClick={() => { setEmoji(e); setShowEmojiPicker(false); }} style={{
                  background: COLORS.bg, border: "none", borderRadius: 14,
                  padding: "10px 14px", cursor: "pointer",
                  display: "flex", flexDirection: "column", alignItems: "center", gap: 4,
                }}>
                  <span style={{ fontSize: 26 }}>{e}</span>
                  <span style={{ fontSize: 10, color: COLORS.muted }}>{l}</span>
                </button>
              ))}
            </div>
          </div>
        </div>
      )}
    </div>
  );
}

// ── SUMMARY SCREEN ───────────────────────────────────────────────────────────
function SummaryScreen({ group, onBack, onSettle }) {
  const balances = computeBalances(group.members, group.expenses);
  const settlements = simplifyDebts(balances);
  const total = group.expenses.reduce((a, e) => a + (parseFloat(e.amount) || 0), 0);

  const getMember = (id) => group.members.find((m) => m.id === id);
  const getName = (id) => {
    const m = getMember(id);
    return m?.isMe ? "You" : m?.name || "?";
  };

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      <div style={{ padding: "56px 20px 20px", display: "flex", alignItems: "center", gap: 12 }}>
        <button onClick={onBack} style={{ background: COLORS.bg, border: "none", width: 40, height: 40, borderRadius: 12, cursor: "pointer", fontSize: 18, display: "flex", alignItems: "center", justifyContent: "center" }}>←</button>
        <h1 style={{ fontFamily: "'Fraunces', serif", fontSize: 24, fontWeight: 700 }}>Summary</h1>
      </div>

      <div style={{ padding: "0 20px", display: "flex", flexDirection: "column", gap: 16 }}>
        {/* Total */}
        <div className="card" style={{ background: `linear-gradient(135deg, ${COLORS.ink}, #2D2D4E)`, padding: "24px" }}>
          <p style={{ color: "rgba(255,255,255,0.6)", fontSize: 12, fontWeight: 600, textTransform: "uppercase", letterSpacing: "0.08em" }}>Total Spent</p>
          <p className="amount-big" style={{ color: "white", marginTop: 4 }}>{fmt(total)}</p>
          <p style={{ color: "rgba(255,255,255,0.5)", fontSize: 13, marginTop: 4 }}>
            {group.expenses.length} expenses · {group.members.length} people
          </p>
        </div>

        {/* Individual balances */}
        <div className="card">
          <p className="label">Individual Balances</p>
          {group.members.map((m, i) => {
            const [bg, txt] = getAvatarColors(i);
            const bal = balances[m.id] || 0;
            return (
              <div key={m.id} style={{ display: "flex", alignItems: "center", gap: 12, padding: "10px 0", borderBottom: `1px solid ${COLORS.border}` }}>
                <div className="avatar" style={{ background: bg, color: txt }}>{m.isMe ? "Me" : m.name.slice(0, 2).toUpperCase()}</div>
                <div style={{ flex: 1 }}>
                  <p style={{ fontWeight: 600, fontSize: 14 }}>{m.isMe ? "You" : m.name}</p>
                  <p style={{ fontSize: 12, color: COLORS.muted }}>
                    {bal >= 0 ? "gets back" : "owes"} overall
                  </p>
                </div>
                <span style={{
                  fontFamily: "'Fraunces', serif", fontSize: 18, fontWeight: 700,
                  color: bal >= 0 ? COLORS.sage : COLORS.danger,
                }}>
                  {bal >= 0 ? "+" : ""}{fmt(bal)}
                </span>
              </div>
            );
          })}
        </div>

        {/* Settlement plan */}
        <div className="card">
          <p className="label">Settlement Plan</p>
          <p style={{ fontSize: 12, color: COLORS.muted, marginBottom: 12 }}>Minimum transfers to settle all debts</p>
          {settlements.length === 0 && (
            <div style={{ textAlign: "center", padding: "20px", color: COLORS.sage }}>
              <span style={{ fontSize: 28 }}>✅</span>
              <p style={{ fontWeight: 600, marginTop: 8 }}>All settled up!</p>
            </div>
          )}
          {settlements.map((s, i) => {
            const fromName = getName(s.from);
            const toName = getName(s.to);
            const fi = group.members.findIndex((m) => m.id === s.from);
            const ti = group.members.findIndex((m) => m.id === s.to);
            const [fbg, ftxt] = getAvatarColors(fi);
            const [tbg, ttxt] = getAvatarColors(ti);
            return (
              <div key={i} style={{
                display: "flex", alignItems: "center", gap: 10,
                padding: "12px 0", borderBottom: `1px solid ${COLORS.border}`,
              }}>
                <div className="avatar" style={{ background: fbg, color: ftxt, width: 36, height: 36, fontSize: 12 }}>{fromName.slice(0, 2).toUpperCase()}</div>
                <div style={{ flex: 1 }}>
                  <p style={{ fontSize: 13, fontWeight: 500 }}>
                    <strong>{fromName}</strong> → <strong>{toName}</strong>
                  </p>
                </div>
                <div className="avatar" style={{ background: tbg, color: ttxt, width: 36, height: 36, fontSize: 12 }}>{toName.slice(0, 2).toUpperCase()}</div>
                <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 17, color: COLORS.accent, marginLeft: 4 }}>
                  {fmt(s.amount)}
                </span>
              </div>
            );
          })}
        </div>

        {settlements.length > 0 && (
          <button className="btn-primary" onClick={onSettle}>
            Mark All as Settled 🎉
          </button>
        )}
      </div>
    </div>
  );
}

// ── INSTALLMENT SCREEN ───────────────────────────────────────────────────────
function InstallmentScreen({ group, onBack }) {
  const [title, setTitle] = useState("");
  const [total, setTotal] = useState("");
  const [months, setMonths] = useState("6");
  const [paidMonths, setPaidMonths] = useState(0);
  const [saved, setSaved] = useState(null);
  const [installments, setInstallments] = useState(group.installments || []);

  const numMembers = group.members.length;
  const totalAmt = parseFloat(total) || 0;
  const numMonths = parseInt(months) || 1;
  const monthlyTotal = totalAmt / numMonths;
  const perPerson = monthlyTotal / numMembers;
  const totalPerPerson = totalAmt / numMembers;
  const paidAmount = paidMonths * monthlyTotal;
  const remaining = totalAmt - paidAmount;
  const progress = totalAmt > 0 ? (paidAmount / totalAmt) * 100 : 0;

  const addPlan = () => {
    if (!title.trim() || !totalAmt) return;
    const plan = {
      id: uid(), title: title.trim(), totalAmt, numMonths, numMembers,
      paidMonths: 0, createdAt: new Date().toISOString(),
    };
    setInstallments((prev) => [...prev, plan]);
    setTitle(""); setTotal(""); setMonths("6");
    setSaved("Plan added!");
    setTimeout(() => setSaved(null), 2000);
  };

  const updatePaid = (planId, delta) => {
    setInstallments((prev) => prev.map((p) =>
      p.id === planId ? { ...p, paidMonths: Math.max(0, Math.min(p.numMonths, p.paidMonths + delta)) } : p
    ));
  };

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      <div style={{ padding: "56px 20px 20px", display: "flex", alignItems: "center", gap: 12 }}>
        <button onClick={onBack} style={{ background: COLORS.bg, border: "none", width: 40, height: 40, borderRadius: 12, cursor: "pointer", fontSize: 18, display: "flex", alignItems: "center", justifyContent: "center" }}>←</button>
        <div>
          <h1 style={{ fontFamily: "'Fraunces', serif", fontSize: 24, fontWeight: 700 }}>Installments</h1>
          <p style={{ color: COLORS.muted, fontSize: 13 }}>{group.name}</p>
        </div>
      </div>

      <div style={{ padding: "0 20px", display: "flex", flexDirection: "column", gap: 16 }}>
        {/* New plan form */}
        <div className="card">
          <p className="label">New Installment Plan</p>
          <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
            <input className="input-field" placeholder="Item name (e.g. PS5, Sofa)"
              value={title} onChange={(e) => setTitle(e.target.value)} />
            <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
              <div>
                <p style={{ fontSize: 12, color: COLORS.muted, marginBottom: 4 }}>Total Price</p>
                <input className="input-field" type="number" inputMode="decimal" placeholder="$0.00"
                  value={total} onChange={(e) => setTotal(e.target.value)} />
              </div>
              <div>
                <p style={{ fontSize: 12, color: COLORS.muted, marginBottom: 4 }}>Months</p>
                <input className="input-field" type="number" inputMode="numeric" placeholder="6"
                  value={months} onChange={(e) => setMonths(e.target.value)} />
              </div>
            </div>

            {totalAmt > 0 && (
              <div style={{ background: COLORS.accentLight, borderRadius: 14, padding: 14 }}>
                <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
                  {[
                    { l: "Monthly (total)", v: fmt(monthlyTotal) },
                    { l: "Per person/mo", v: fmt(perPerson) },
                    { l: `Each pays (total)`, v: fmt(totalPerPerson) },
                    { l: "Split among", v: `${numMembers} people` },
                  ].map(({ l, v }) => (
                    <div key={l}>
                      <p style={{ fontSize: 11, color: COLORS.accent, fontWeight: 600, marginBottom: 2 }}>{l}</p>
                      <p style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 18, color: COLORS.ink }}>{v}</p>
                    </div>
                  ))}
                </div>
              </div>
            )}

            <button className="btn-primary" onClick={addPlan}
              disabled={!title.trim() || !totalAmt}
              style={{ opacity: title.trim() && totalAmt ? 1 : 0.5 }}>
              Add Plan
            </button>
          </div>
        </div>

        {/* Saved plans */}
        {installments.map((plan) => {
          const paidAmt = plan.paidMonths * (plan.totalAmt / plan.numMonths);
          const rem = plan.totalAmt - paidAmt;
          const prog = (paidAmt / plan.totalAmt) * 100;
          const ppMo = plan.totalAmt / plan.numMonths / plan.numMembers;
          return (
            <div key={plan.id} className="card">
              <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 12 }}>
                <div>
                  <p style={{ fontWeight: 700, fontSize: 16 }}>{plan.title}</p>
                  <p style={{ color: COLORS.muted, fontSize: 12 }}>{plan.numMembers} people · {plan.numMonths} months</p>
                </div>
                <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 20 }}>{fmt(plan.totalAmt)}</span>
              </div>

              <div className="progress-track" style={{ marginBottom: 8 }}>
                <div className="progress-fill" style={{ width: `${prog}%` }} />
              </div>
              <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 14 }}>
                <span style={{ fontSize: 12, color: COLORS.sage, fontWeight: 600 }}>{plan.paidMonths}/{plan.numMonths} months paid</span>
                <span style={{ fontSize: 12, color: COLORS.muted }}>{fmt(rem)} remaining</span>
              </div>

              <div style={{ background: COLORS.goldLight, borderRadius: 12, padding: "10px 14px", marginBottom: 12 }}>
                <p style={{ fontSize: 12, color: COLORS.gold, fontWeight: 600 }}>Each person pays {fmt(ppMo)}/month</p>
              </div>

              <div style={{ display: "flex", gap: 8 }}>
                <button onClick={() => updatePaid(plan.id, -1)} className="btn-ghost"
                  style={{ flex: 1, padding: "10px" }} disabled={plan.paidMonths === 0}>
                  − Month
                </button>
                <button onClick={() => updatePaid(plan.id, 1)} className="btn-secondary"
                  style={{ flex: 1 }} disabled={plan.paidMonths >= plan.numMonths}>
                  {plan.paidMonths >= plan.numMonths ? "✅ Done!" : "+ Mark Paid"}
                </button>
              </div>
            </div>
          );
        })}
      </div>

      {saved && <div className="toast">{saved}</div>}
    </div>
  );
}

// ─── BOTTOM NAV ─────────────────────────────────────────────────────────────
function BottomNav({ active, onNavigate }) {
  const items = [
    { key: "home", icon: "🏠", label: "Home" },
    { key: "activity", icon: "📋", label: "Activity" },
    { key: "add", icon: "➕", label: "Add" },
    { key: "settle", icon: "💸", label: "Settle" },
    { key: "profile", icon: "👤", label: "Profile" },
  ];
  return (
    <nav className="bottom-nav">
      {items.map(({ key, icon, label }) => (
        <button key={key} className="nav-item" onClick={() => onNavigate(key)}
          style={{ color: active === key ? COLORS.accent : COLORS.muted }}>
          <span className="nav-icon">{icon}</span>
          <span className="nav-label" style={{ fontWeight: active === key ? 700 : 500 }}>{label}</span>
        </button>
      ))}
    </nav>
  );
}

// ─── ACTIVITY SCREEN ────────────────────────────────────────────────────────
function ActivityScreen({ groups }) {
  const allExpenses = groups.flatMap((g) =>
    g.expenses.map((e) => ({ ...e, groupName: g.name, groupEmoji: g.emoji }))
  ).sort((a, b) => new Date(b.date) - new Date(a.date));

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      <div style={{ padding: "56px 20px 20px" }}>
        <h1 style={{ fontFamily: "'Fraunces', serif", fontSize: 28, fontWeight: 700 }}>Activity</h1>
        <p style={{ color: COLORS.muted, fontSize: 14, marginTop: 4 }}>All recent expenses</p>
      </div>
      <div style={{ padding: "0 16px", display: "flex", flexDirection: "column", gap: 8 }}>
        {allExpenses.length === 0 && (
          <div style={{ textAlign: "center", padding: "48px 24px", color: COLORS.muted }}>
            <div style={{ fontSize: 40, marginBottom: 8 }}>📭</div>
            <p>No expenses yet</p>
          </div>
        )}
        {allExpenses.map((exp) => (
          <div key={exp.id} className="swipe-row">
            <div style={{ width: 44, height: 44, background: COLORS.accentLight, borderRadius: 14, display: "flex", alignItems: "center", justifyContent: "center", fontSize: 20 }}>
              {exp.emoji}
            </div>
            <div style={{ flex: 1 }}>
              <p style={{ fontWeight: 600, fontSize: 14 }}>{exp.title}</p>
              <p style={{ color: COLORS.muted, fontSize: 12 }}>{exp.groupEmoji} {exp.groupName}</p>
            </div>
            <span style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 16 }}>{fmt(exp.amount)}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

// ─── PROFILE SCREEN ─────────────────────────────────────────────────────────
function ProfileScreen({ groups }) {
  const totalExpenses = groups.reduce((a, g) => a + g.expenses.length, 0);
  const totalSpent = groups.reduce((a, g) => a + g.expenses.reduce((b, e) => b + (parseFloat(e.amount) || 0), 0), 0);

  return (
    <div className="screen" style={{ padding: "0 0 100px" }}>
      <div style={{ background: `linear-gradient(145deg, ${COLORS.accent}, #FF8A70)`, padding: "56px 24px 36px", textAlign: "center" }}>
        <div style={{ width: 80, height: 80, borderRadius: "50%", background: "rgba(255,255,255,0.2)", margin: "0 auto 16px", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 36, border: "3px solid rgba(255,255,255,0.3)" }}>
          🙋
        </div>
        <h2 style={{ fontFamily: "'Fraunces', serif", color: "white", fontSize: 24, fontWeight: 700 }}>You</h2>
        <p style={{ color: "rgba(255,255,255,0.7)", fontSize: 14 }}>SplitEasy user</p>
      </div>

      <div style={{ padding: "20px 20px", display: "flex", flexDirection: "column", gap: 12 }}>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr 1fr", gap: 10 }}>
          {[
            { l: "Groups", v: groups.length, i: "👥" },
            { l: "Expenses", v: totalExpenses, i: "🧾" },
            { l: "Total Spent", v: fmt(totalSpent), i: "💰" },
          ].map(({ l, v, i }) => (
            <div key={l} className="card" style={{ textAlign: "center" }}>
              <div style={{ fontSize: 22, marginBottom: 6 }}>{i}</div>
              <p style={{ fontFamily: "'Fraunces', serif", fontWeight: 700, fontSize: 20 }}>{v}</p>
              <p style={{ color: COLORS.muted, fontSize: 11, fontWeight: 500 }}>{l}</p>
            </div>
          ))}
        </div>

        <div className="card">
          <p className="label">About SplitEasy</p>
          <p style={{ fontSize: 14, color: COLORS.muted, lineHeight: 1.6 }}>
            A fast, beautiful expense splitting app designed for everyday use. Equal splits, custom amounts, percentages — and installment tracking built in.
          </p>
        </div>

        <div className="card">
          <p className="label">Features</p>
          {["✅ Equal / Custom / % splits", "✅ Simplified debt settlement", "✅ Installment tracker", "✅ Group expense history", "✅ Mobile-first design"].map((f) => (
            <p key={f} style={{ fontSize: 14, padding: "6px 0", borderBottom: `1px solid ${COLORS.border}`, color: COLORS.ink }}>{f}</p>
          ))}
        </div>
      </div>
    </div>
  );
}

// ─── SEED DATA ───────────────────────────────────────────────────────────────
const SEED_GROUPS = () => {
  const you = { id: "u1", name: "You", isMe: true };
  const alex = { id: "u2", name: "Alex" };
  const mia = { id: "u3", name: "Mia" };
  const sam = { id: "u4", name: "Sam" };

  return [{
    id: "g1", name: "Bali Trip 🌴", emoji: "✈️",
    members: [you, alex, mia, sam],
    installments: [],
    expenses: [
      { id: "e1", title: "Hotel Night 1", amount: 240, emoji: "🏠", paidById: "u1", splitType: "equal", participants: ["u1","u2","u3","u4"], date: new Date(Date.now()-86400000*3).toISOString() },
      { id: "e2", title: "Dinner at Merah", amount: 88, emoji: "🍽️", paidById: "u2", splitType: "equal", participants: ["u1","u2","u3","u4"], date: new Date(Date.now()-86400000*2).toISOString() },
      { id: "e3", title: "Scooter Rental", amount: 60, emoji: "🚗", paidById: "u3", splitType: "equal", participants: ["u1","u2","u3"], date: new Date(Date.now()-86400000).toISOString() },
    ],
  }];
};

// ═══════════════════════════════════════════════════════════════════════════
// ROOT APP
// ═══════════════════════════════════════════════════════════════════════════
export default function App() {
  const [groups, setGroups] = useState(SEED_GROUPS);
  const [screen, setScreen] = useState("home");
  const [activeNav, setActiveNav] = useState("home");
  const [selectedGroupId, setSelectedGroupId] = useState(null);
  const [toast, setToast] = useState(null);

  const showToast = (msg) => {
    setToast(msg);
    setTimeout(() => setToast(null), 2200);
  };

  const selectedGroup = groups.find((g) => g.id === selectedGroupId);

  const updateGroup = (updated) => {
    setGroups((prev) => prev.map((g) => g.id === updated.id ? updated : g));
  };

  const handleNavigation = (key) => {
    setActiveNav(key);
    if (key === "home") { setScreen("home"); setSelectedGroupId(null); }
    else if (key === "activity") setScreen("activity");
    else if (key === "profile") setScreen("profile");
    else if (key === "settle") { setScreen("home"); setSelectedGroupId(null); }
    else if (key === "add") {
      if (groups.length > 0) {
        setSelectedGroupId(groups[0].id);
        setScreen("add-expense");
      } else {
        setScreen("create-group");
      }
    }
  };

  // ─── RENDER ────────────────────────────────────────────────────────────
  const renderScreen = () => {
    switch (screen) {
      case "home":
        return <HomeScreen groups={groups}
          onSelectGroup={(id) => { setSelectedGroupId(id); setScreen("group"); }}
          onCreateGroup={() => setScreen("create-group")} />;

      case "activity":
        return <ActivityScreen groups={groups} />;

      case "profile":
        return <ProfileScreen groups={groups} />;

      case "create-group":
        return <CreateGroupScreen
          onBack={() => { setScreen("home"); setActiveNav("home"); }}
          onCreate={(g) => {
            setGroups((prev) => [...prev, g]);
            setSelectedGroupId(g.id);
            setScreen("group");
            showToast(`"${g.name}" created! 🎉`);
          }} />;

      case "group":
        if (!selectedGroup) { setScreen("home"); return null; }
        return <GroupScreen group={selectedGroup}
          onBack={() => { setScreen("home"); setActiveNav("home"); }}
          onAddExpense={() => setScreen("add-expense")}
          onViewSummary={() => setScreen("summary")}
          onInstallments={() => setScreen("installments")}
          onUpdateGroup={updateGroup} />;

      case "add-expense":
        if (!selectedGroup) { setScreen("home"); return null; }
        return <AddExpenseScreen group={selectedGroup}
          onBack={() => setScreen("group")}
          onAdd={(exp) => {
            updateGroup({ ...selectedGroup, expenses: [...selectedGroup.expenses, exp] });
            setScreen("group");
            showToast("Expense added ✓");
          }} />;

      case "summary":
        if (!selectedGroup) { setScreen("home"); return null; }
        return <SummaryScreen group={selectedGroup}
          onBack={() => setScreen("group")}
          onSettle={() => {
            updateGroup({ ...selectedGroup, expenses: [] });
            setScreen("group");
            showToast("All settled up! 🎉");
          }} />;

      case "installments":
        if (!selectedGroup) { setScreen("home"); return null; }
        return <InstallmentScreen group={selectedGroup}
          onBack={() => setScreen("group")} />;

      default:
        return <HomeScreen groups={groups}
          onSelectGroup={(id) => { setSelectedGroupId(id); setScreen("group"); }}
          onCreateGroup={() => setScreen("create-group")} />;
    }
  };

  const showNav = !["create-group", "add-expense"].includes(screen);

  return (
    <>
      <GlobalStyles />
      <div className="app-shell">
        {renderScreen()}
        {showNav && <BottomNav active={activeNav} onNavigate={handleNavigation} />}
        {toast && <div className="toast">{toast}</div>}
      </div>
    </>
  );
}
