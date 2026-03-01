import { useState, useEffect, useRef, useCallback } from "react";

/* ═══════════════════════════════════════════════════════════════════════════
   AGENTS — SVG portraits + role definitions
═══════════════════════════════════════════════════════════════════════════ */
const AGENTS = [
  {
    id: "arch", seat: 0,
    name: "Rex Architectus", title: "Strategic Lead",
    color: "#C9932A", accent: "#FFD17A",
    systemPrompt: `You are REX ARCHITECTUS, the Strategic Lead of the Council of Kings.
Your ONLY job: define project structure, folder layout, milestones, and high-level component boundaries.
NEVER write implementation code. NEVER write SQL. NEVER write config files.
Respond in this exact format — two sections, nothing else:

[NARRATIVE]: <1-3 sentences of in-character dialogue. You are a commanding general mapping territory. Speak with authority.>

[TECHNICAL]:
<A clean folder tree or milestone list. Use ASCII box-drawing characters. Be precise.>`,
    face: `<circle cx="50" cy="42" r="22" fill="#C8956C"/>
<ellipse cx="50" cy="70" rx="26" ry="14" fill="#8B6914"/>
<rect x="30" y="55" width="40" height="20" rx="4" fill="#7A5C10"/>
<line x1="50" y1="62" x2="50" y2="78" stroke="#C9932A" stroke-width="1.5"/>
<ellipse cx="42" cy="40" rx="4" ry="4.5" fill="#1a0f00"/>
<ellipse cx="58" cy="40" rx="4" ry="4.5" fill="#1a0f00"/>
<ellipse cx="42" cy="39" rx="1.5" ry="2" fill="#fff" opacity="0.6"/>
<ellipse cx="58" cy="39" rx="1.5" ry="2" fill="#fff" opacity="0.6"/>
<path d="M44 48 Q50 52 56 48" stroke="#8B5E3C" stroke-width="1.5" fill="none"/>
<path d="M38 35 Q42 32 46 34" stroke="#5C3D1E" stroke-width="2" fill="none"/>
<path d="M54 34 Q58 32 62 35" stroke="#5C3D1E" stroke-width="2" fill="none"/>
<path d="M32 28 Q34 20 38 22 Q40 15 44 18 Q46 11 50 13 Q54 11 56 18 Q60 15 62 22 Q66 20 68 28" stroke="#C9932A" stroke-width="2.5" fill="none"/>
<circle cx="50" cy="13" r="3" fill="#C9932A"/>
<path d="M36 50 Q38 58 40 62 Q50 66 60 62 Q62 58 64 50" fill="#5C3D1E" opacity="0.6"/>`,
  },
  {
    id: "expo", seat: 1,
    name: "Rex Explorator", title: "Intelligence Scout",
    color: "#2A7FC9", accent: "#7AC5FF",
    systemPrompt: `You are REX EXPLORATOR, the Intelligence Scout of the Council of Kings.
Your ONLY job: research requirements, identify the right libraries/frameworks/APIs, surface gotchas and version-specific warnings.
NEVER write application code. Speak like a field agent reporting verified intelligence.
Respond in this exact format:

[NARRATIVE]: <1-3 sentences. You are a scout returning from dangerous territory with critical intel. Precise and urgent.>

[TECHNICAL]:
<Verified findings: library names + versions, key API signatures, critical warnings, dependency requirements. Use # comments for warnings.>`,
    face: `<circle cx="50" cy="42" r="22" fill="#B8855A"/>
<ellipse cx="50" cy="70" rx="26" ry="14" fill="#1A3A6B"/>
<rect x="28" y="60" width="44" height="18" rx="3" fill="#1A3A6B"/>
<path d="M26 72 Q28 62 34 60 L66 60 Q72 62 74 72" fill="#152D55"/>
<ellipse cx="42" cy="40" rx="4" ry="4.5" fill="#0d2137"/>
<ellipse cx="58" cy="40" rx="4" ry="4.5" fill="#0d2137"/>
<ellipse cx="42.5" cy="39" rx="1.5" ry="2" fill="#fff" opacity="0.7"/>
<ellipse cx="58.5" cy="39" rx="1.5" ry="2" fill="#fff" opacity="0.7"/>
<path d="M44 49 Q50 53 56 49" stroke="#8B5E3C" stroke-width="1.5" fill="none"/>
<path d="M38 34 Q42 31 46 33" stroke="#3D2410" stroke-width="1.8" fill="none"/>
<path d="M54 33 Q58 31 62 34" stroke="#3D2410" stroke-width="1.8" fill="none"/>
<path d="M28 35 Q29 18 50 16 Q71 18 72 35" stroke="#2A7FC9" stroke-width="2" fill="none" opacity="0.7"/>
<circle cx="28" cy="44" r="2.5" fill="#2A7FC9" opacity="0.8"/>
<rect x="43" y="61" width="14" height="5" rx="1" fill="#D4B483" opacity="0.8"/>`,
  },
  {
    id: "fabr", seat: 2,
    name: "Rex Fabricator", title: "Master Builder",
    color: "#1F9E6A", accent: "#6BFFB8",
    systemPrompt: `You are REX FABRICATOR, the Master Builder of the Council of Kings.
Your job: write the actual production code based on the Architect's structure and Explorator's intelligence.
Write complete, runnable code. No pseudocode. No placeholders. Real implementations only.
Speak like a master craftsman who takes pride in precise, hardened work.
Respond in this exact format:

[NARRATIVE]: <1-3 sentences. You are a blacksmith forging steel. Confident, direct, workmanlike.>

[TECHNICAL]:
<Complete production code with proper error handling. Include filename as a comment at the top.>`,
    face: `<circle cx="50" cy="42" r="22" fill="#A0724A"/>
<ellipse cx="50" cy="70" rx="26" ry="14" fill="#2D4A2D"/>
<rect x="28" y="59" width="44" height="19" rx="3" fill="#2D4A2D"/>
<path d="M34 62 L34 78 Q50 82 66 78 L66 62" fill="#1A2E1A"/>
<ellipse cx="42" cy="40" rx="4.5" ry="4.5" fill="#1a1200"/>
<ellipse cx="58" cy="40" rx="4.5" ry="4.5" fill="#1a1200"/>
<ellipse cx="42.5" cy="39" rx="1.8" ry="2" fill="#fff" opacity="0.6"/>
<ellipse cx="58.5" cy="39" rx="1.8" ry="2" fill="#fff" opacity="0.6"/>
<path d="M43 49 Q50 54 57 49" stroke="#7A4A2A" stroke-width="2" fill="none"/>
<path d="M37 34 Q42 30 47 33" stroke="#2A1A08" stroke-width="3" fill="none"/>
<path d="M53 33 Q58 30 63 34" stroke="#2A1A08" stroke-width="3" fill="none"/>
<path d="M33 47 Q35 62 42 68 Q50 72 58 68 Q65 62 67 47 Q60 53 50 54 Q40 53 33 47" fill="#3D2410" opacity="0.85"/>
<rect x="66" y="54" width="6" height="14" rx="2" fill="#8B7355" opacity="0.9"/>
<rect x="63" y="52" width="12" height="5" rx="2" fill="#5C4A2A" opacity="0.9"/>
<line x1="44" y1="37" x2="46" y2="43" stroke="#8B5E3C" stroke-width="1" opacity="0.6"/>`,
  },
  {
    id: "cens", seat: 3,
    name: "Rex Censor", title: "Security Auditor",
    color: "#C92A2A", accent: "#FF7A7A",
    systemPrompt: `You are REX CENSOR, the Security Auditor of the Council of Kings.
Your job: audit the Fabricator's code for security vulnerabilities, logic flaws, missing validation, hardcoded secrets, SQL injection, improper error handling, missing rate limits, and anything that would fail a production security review.
You are a MANDATORY BLOCKING GATE. Be thorough. Never rubber-stamp.
Speak like a stern inquisitor who has seen systems fail catastrophically.
Respond in this exact format:

[NARRATIVE]: <1-3 sentences. You are an iron wall. Grave, precise, uncompromising.>

[TECHNICAL]:
<Numbered audit findings using PASS/WARN/FAIL prefixes with bracketed codes like [SEC-001].
End with a STATUS line: ✅ ALL CLEAR / ⚠ CONDITIONAL PASS (N warnings) / 🚫 BLOCKED (N failures)>`,
    face: `<circle cx="50" cy="42" r="22" fill="#9E7055"/>
<ellipse cx="50" cy="70" rx="26" ry="14" fill="#3A1A1A"/>
<rect x="28" y="59" width="44" height="19" rx="3" fill="#3A1A1A"/>
<path d="M28 66 Q30 58 36 60 L64 60 Q70 58 72 66 L72 80 Q50 84 28 80Z" fill="#2A0A0A"/>
<path d="M44 63 Q50 60 56 63 L56 72 Q50 76 44 72Z" fill="#C92A2A" opacity="0.7"/>
<ellipse cx="42" cy="40" rx="4" ry="4.5" fill="#0d0000"/>
<ellipse cx="58" cy="40" rx="4" ry="4.5" fill="#0d0000"/>
<ellipse cx="42" cy="38.5" rx="1.5" ry="2" fill="#fff" opacity="0.7"/>
<ellipse cx="58" cy="38.5" rx="1.5" ry="2" fill="#fff" opacity="0.7"/>
<path d="M44 49 Q50 51 56 49" stroke="#7A3A3A" stroke-width="1.5" fill="none"/>
<path d="M37 33 Q41 29 46 32" stroke="#1A0A0A" stroke-width="2.5" fill="none"/>
<path d="M54 32 Q59 29 63 33" stroke="#1A0A0A" stroke-width="2.5" fill="none"/>
<path d="M28 38 Q30 32 34 30" stroke="#C0C0C0" stroke-width="2" fill="none" opacity="0.7"/>
<path d="M72 38 Q70 32 66 30" stroke="#C0C0C0" stroke-width="2" fill="none" opacity="0.7"/>
<circle cx="58" cy="40" r="7" fill="none" stroke="#C92A2A" stroke-width="1.5" opacity="0.8"/>
<line x1="65" y1="43" x2="68" y2="47" stroke="#C92A2A" stroke-width="1.2" opacity="0.8"/>`,
  },
];

/* ═══════════════════════════════════════════════════════════════════════════
   COUNCIL SEQUENCE — defines which King speaks in which order and what context they receive
═══════════════════════════════════════════════════════════════════════════ */
const COUNCIL_SEQUENCE = [
  { agentId: "arch", toId: null,   mode: "broadcast", label: "Mapping Territory" },
  { agentId: "expo", toId: "arch", mode: "peer",      label: "Scouting Intel"    },
  { agentId: "fabr", toId: null,   mode: "broadcast", label: "Forging Core"      },
  { agentId: "cens", toId: "fabr", mode: "peer",      label: "Security Audit"    },
  { agentId: "fabr", toId: "cens", mode: "peer",      label: "Resolving Findings"},
  { agentId: "cens", toId: null,   mode: "broadcast", label: "Final Seal"        },
];

/* ═══════════════════════════════════════════════════════════════════════════
   GEOMETRY HELPERS
═══════════════════════════════════════════════════════════════════════════ */
const seatAngle = (seat) => (seat * 90 - 90) * (Math.PI / 180);
const seatPos   = (seat, r) => ({
  x: Math.cos(seatAngle(seat)) * r,
  y: Math.sin(seatAngle(seat)) * r,
});

/* ═══════════════════════════════════════════════════════════════════════════
   PARSE Claude response into narrative + technical blocks
   — tolerates variations like "NARRATIVE:" without brackets,
     missing TECHNICAL section, or extra whitespace
═══════════════════════════════════════════════════════════════════════════ */
function parseResponse(text) {
  if (!text || !text.trim()) return { narrative: "…", technical: "" };

  // Support both [NARRATIVE]: and NARRATIVE: formats
  const narrativeMatch = text.match(/\[?NARRATIVE\]?:\s*([\s\S]*?)(?=\[?TECHNICAL\]?:|$)/i);
  const technicalMatch = text.match(/\[?TECHNICAL\]?:\s*([\s\S]*?)$/i);

  const narrative = narrativeMatch?.[1]?.trim();
  const technical = technicalMatch?.[1]?.trim();

  // If neither tag found, treat the whole response as narrative
  if (!narrative && !technical) {
    return { narrative: text.trim(), technical: "" };
  }

  return {
    narrative: narrative || text.trim(),
    technical: technical || "",
  };
}

/* ═══════════════════════════════════════════════════════════════════════════
   CALL CLAUDE API — uses the artifact's built-in API bridge
   The artifact sandbox cannot fetch api.anthropic.com directly (CORS).
   Claude.ai injects the API through the parent window message channel.
═══════════════════════════════════════════════════════════════════════════ */
function callClaudeViaArtifact(system, userContent) {
  return new Promise((resolve, reject) => {
    const requestId = `req_${Date.now()}_${Math.random().toString(36).slice(2)}`;
    const timeout = setTimeout(() => {
      window.removeEventListener("message", handler);
      reject(new Error("Request timed out after 30s — API bridge not responding"));
    }, 30000);

    function handler(event) {
      const msg = event.data;
      if (!msg || msg.requestId !== requestId) return;
      clearTimeout(timeout);
      window.removeEventListener("message", handler);
      if (msg.error) return reject(new Error(msg.error));
      resolve(msg.response || "");
    }

    window.addEventListener("message", handler);
    window.parent.postMessage({
      type: "claude_api_request",
      requestId,
      system,
      messages: [{ role: "user", content: userContent }],
      max_tokens: 1000,
    }, "*");
  });
}

async function callKing(agent, userTask, priorTransmissions) {
  const contextSummary = priorTransmissions.length > 0
    ? `\n\nPRIOR COUNCIL TRANSMISSIONS:\n${priorTransmissions.map(t =>
        `${t.agentName} said:\n${t.narrative}\n${t.technical}`
      ).join("\n\n---\n\n")}`
    : "";

  const userMessage = `THE COUNCIL HAS BEEN CONVENED FOR THIS TASK:\n${userTask}${contextSummary}\n\nNow speak, ${agent.name}. Fulfill your mandate.`;

  let raw = "";
  try {
    raw = await callClaudeViaArtifact(agent.systemPrompt, userMessage);
  } catch (err) {
    throw new Error(err.message);
  }

  if (!raw || !raw.trim()) {
    throw new Error("Empty response — the API bridge returned nothing");
  }

  return parseResponse(raw);
}

/* ═══════════════════════════════════════════════════════════════════════════
   TRANSMISSION BEAM SVG
═══════════════════════════════════════════════════════════════════════════ */
function TransmissionBeam({ fromSeat, toSeat, mode, color }) {
  const R = 175;
  const from = seatPos(fromSeat, R);
  const to   = toSeat != null ? seatPos(toSeat, R) : { x: 0, y: 0 };
  const cx = 280, cy = 280;

  return (
    <g>
      <line
        x1={cx + from.x} y1={cy + from.y}
        x2={cx + to.x}   y2={cy + to.y}
        stroke={color} strokeWidth={10} opacity={0.08}
        style={{ filter: "blur(8px)" }}
      />
      <line
        x1={cx + from.x} y1={cy + from.y}
        x2={cx + to.x}   y2={cy + to.y}
        stroke={color}
        strokeWidth={mode === "broadcast" ? 2 : 1.5}
        strokeDasharray={mode === "peer" ? "7 4" : "none"}
        opacity={0.9}
        style={{ animation: "beampulse 1.8s ease-in-out infinite" }}
      />
      <circle r={5} fill={color} opacity={0.95}
        style={{ filter: `drop-shadow(0 0 8px ${color})` }}>
        <animateMotion dur="1.4s" repeatCount="indefinite"
          path={`M${cx+from.x},${cy+from.y} L${cx+to.x},${cy+to.y}`} />
      </circle>
    </g>
  );
}

/* ═══════════════════════════════════════════════════════════════════════════
   ROUND TABLE SVG
═══════════════════════════════════════════════════════════════════════════ */
function RoundTable({ activeAgentId, toAgentId, transmissions }) {
  const fromAgent = AGENTS.find(a => a.id === activeAgentId);
  const toAgent   = AGENTS.find(a => a.id === toAgentId);

  return (
    <svg width={560} height={560} viewBox="0 0 560 560"
      style={{ position: "absolute", inset: 0, pointerEvents: "none" }}>
      <defs>
        <radialGradient id="tg" cx="50%" cy="42%">
          <stop offset="0%"   stopColor="#2C1810"/>
          <stop offset="65%"  stopColor="#180D08"/>
          <stop offset="100%" stopColor="#0D0604"/>
        </radialGradient>
        <radialGradient id="sheen" cx="30%" cy="28%">
          <stop offset="0%"   stopColor="#ffffff" stopOpacity="0.07"/>
          <stop offset="100%" stopColor="#ffffff" stopOpacity="0"/>
        </radialGradient>
        <radialGradient id="cglow" cx="50%" cy="50%">
          <stop offset="0%"   stopColor={fromAgent?.color || "#C9932A"} stopOpacity="0.3"/>
          <stop offset="100%" stopColor="transparent" stopOpacity="0"/>
        </radialGradient>
        <filter id="tshadow">
          <feDropShadow dx="0" dy="12" stdDeviation="18" floodOpacity="0.8" floodColor="#000"/>
        </filter>
      </defs>

      {/* Drop shadow */}
      <ellipse cx="280" cy="310" rx="178" ry="36"
        fill="#000" opacity="0.55" style={{ filter: "blur(22px)" }}/>

      {/* Table body */}
      <ellipse cx="280" cy="280" rx="175" ry="172"
        fill="url(#tg)" filter="url(#tshadow)"/>

      {/* Edge rings */}
      <ellipse cx="280" cy="280" rx="175" ry="172" fill="none" stroke="#5C3010" strokeWidth="7"/>
      <ellipse cx="280" cy="280" rx="170" ry="167" fill="none" stroke="#8B4A18" strokeWidth="2" opacity="0.5"/>
      <ellipse cx="280" cy="280" rx="167" ry="164" fill="none" stroke="#C9932A" strokeWidth="0.8" opacity="0.35"/>

      {/* Sheen */}
      <ellipse cx="280" cy="280" rx="175" ry="172" fill="url(#sheen)"/>

      {/* Wood grain */}
      {[-55,-35,-15,5,25,45,65].map(o => (
        <ellipse key={o} cx="280" cy={280 + o * 0.28}
          rx={175 - Math.abs(o) * 0.7} ry={14}
          fill="none" stroke="#3A1808" strokeWidth="0.5" opacity="0.28"/>
      ))}

      {/* Compass rose */}
      {[0,45,90,135,180,225,270,315].map(deg => {
        const r = deg * Math.PI / 180;
        return (
          <line key={deg}
            x1={280} y1={280}
            x2={280 + Math.cos(r) * 128} y2={280 + Math.sin(r) * 125}
            stroke="#C9932A"
            strokeWidth={deg % 90 === 0 ? 1.2 : 0.5}
            opacity={deg % 90 === 0 ? 0.3 : 0.12}/>
        );
      })}

      {/* Seat markers */}
      {AGENTS.map(ag => {
        const p = seatPos(ag.seat, 178);
        const isActive = ag.id === activeAgentId;
        return (
          <g key={ag.id}>
            <circle cx={280+p.x} cy={280+p.y} r={11}
              fill="#0a0806"
              stroke={ag.color}
              strokeWidth={isActive ? 3 : 1}
              opacity={0.95}/>
            <circle cx={280+p.x} cy={280+p.y} r={4.5}
              fill={ag.color}
              opacity={isActive ? 1 : 0.35}/>
          </g>
        );
      })}

      {/* Active center glow */}
      {fromAgent && (
        <ellipse cx="280" cy="280" rx="90" ry="88"
          fill="url(#cglow)"
          style={{ animation: "centerpulse 2.2s ease-in-out infinite" }}/>
      )}

      {/* Beam */}
      {fromAgent && (
        <TransmissionBeam
          fromSeat={fromAgent.seat}
          toSeat={toAgent ? toAgent.seat : null}
          mode={toAgent ? "peer" : "broadcast"}
          color={fromAgent.color}
        />
      )}

      {/* Center crown */}
      <g transform="translate(280,280)">
        <circle r={36} fill="#0D0604" stroke="#C9932A" strokeWidth={1.5} opacity={0.95}/>
        <circle r={32} fill="none" stroke="#5C3010" strokeWidth={0.8}/>
        <path d="M-13 7 L-13 -4 L-6 2 L0 -10 L6 2 L13 -4 L13 7 Z"
          fill="#C9932A" opacity={0.9}/>
        <rect x="-13" y="7" width="26" height="4" rx="1" fill="#C9932A" opacity={0.8}/>
        {fromAgent && (
          <circle r={5} cy={20} fill={fromAgent.color}
            style={{ filter: `drop-shadow(0 0 6px ${fromAgent.color})`, animation: "centerpulse 1s infinite" }}/>
        )}
      </g>
    </svg>
  );
}

/* ═══════════════════════════════════════════════════════════════════════════
   AVATAR NODE
═══════════════════════════════════════════════════════════════════════════ */
function AgentNode({ agent, isActive, isPeer, isThinking, transmissionCount }) {
  const pulse = isActive || isPeer;
  return (
    <div style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 7 }}>
      <div style={{ position: "relative", width: 90, height: 90 }}>
        {pulse && <div style={{
          position: "absolute", inset: -9, borderRadius: "50%",
          border: `2px solid ${agent.color}`,
          animation: "ringout 1.8s ease-out infinite", opacity: 0.6,
        }}/>}
        {pulse && <div style={{
          position: "absolute", inset: -18, borderRadius: "50%",
          border: `1px solid ${agent.color}`,
          animation: "ringout 1.8s ease-out 0.5s infinite", opacity: 0.3,
        }}/>}
        <div style={{
          width: 90, height: 90, borderRadius: "50%", overflow: "hidden",
          border: `3px solid ${pulse ? agent.color : agent.color + "44"}`,
          boxShadow: pulse ? `0 0 22px ${agent.color}55, 0 0 44px ${agent.color}22` : "none",
          background: "radial-gradient(circle at 40% 35%, #2a1a0a, #080604)",
          transition: "all 0.5s ease", position: "relative",
        }}>
          <svg width={90} height={90} viewBox="0 0 100 84"
            dangerouslySetInnerHTML={{ __html: agent.face }}/>
          {isThinking && (
            <div style={{
              position: "absolute", inset: 0,
              background: `${agent.color}22`,
              display: "flex", alignItems: "center", justifyContent: "center",
            }}>
              <div style={{ display: "flex", gap: 4 }}>
                {[0,1,2].map(i => (
                  <div key={i} style={{
                    width: 6, height: 6, borderRadius: "50%",
                    background: agent.color,
                    animation: `thinking 1.2s ease-in-out ${i*0.2}s infinite`,
                  }}/>
                ))}
              </div>
            </div>
          )}
          {isActive && !isThinking && (
            <div style={{
              position: "absolute", bottom: 7, right: 7,
              width: 13, height: 13, borderRadius: "50%",
              background: agent.color,
              boxShadow: `0 0 8px ${agent.color}`,
              animation: "speakdot 0.9s ease-in-out infinite",
            }}/>
          )}
        </div>
        {transmissionCount > 0 && (
          <div style={{
            position: "absolute", top: -4, right: -4,
            width: 22, height: 22, borderRadius: "50%",
            background: "#0a0c12", border: `2px solid ${agent.color}`,
            display: "flex", alignItems: "center", justifyContent: "center",
            fontSize: 9, color: agent.color, fontWeight: 700,
            fontFamily: "monospace",
          }}>{transmissionCount}</div>
        )}
      </div>
      <div style={{ textAlign: "center" }}>
        <div style={{
          fontSize: 9.5, fontWeight: 700, letterSpacing: 1.5,
          color: pulse ? agent.accent : "#5a6a7a",
          fontFamily: "monospace", textTransform: "uppercase",
          transition: "color 0.4s",
        }}>{agent.name.replace("Rex ", "")}</div>
        <div style={{
          fontSize: 8, color: pulse ? agent.color + "bb" : "#2a3444",
          letterSpacing: 1, fontFamily: "monospace", marginTop: 1,
          transition: "color 0.4s",
        }}>{agent.title}</div>
      </div>
    </div>
  );
}

/* ═══════════════════════════════════════════════════════════════════════════
   MAIN WAR ROOM
═══════════════════════════════════════════════════════════════════════════ */
export default function WarRoomLive() {
  const [task, setTask]               = useState("");
  const [phase, setPhase]             = useState("idle"); // idle | running | done | error
  const [transmissions, setTransmissions] = useState([]);
  const [activeSeqIdx, setActiveSeqIdx]   = useState(-1);
  const [thinkingId, setThinkingId]       = useState(null);
  const [viewMode, setViewMode]           = useState("narrative");
  const [errorMsg, setErrorMsg]           = useState("");
  const logRef = useRef(null);

  // Scroll log to bottom on new entry
  useEffect(() => {
    if (logRef.current) logRef.current.scrollTop = logRef.current.scrollHeight;
  }, [transmissions]);

  const activeSeq   = COUNCIL_SEQUENCE[activeSeqIdx] || null;
  const activeAgent = activeSeq ? AGENTS.find(a => a.id === activeSeq.agentId) : null;
  const toAgent     = activeSeq?.toId ? AGENTS.find(a => a.id === activeSeq.toId) : null;

  /* ── Run the full council sequence ─────────────────────────────────────── */
  const conveneCouncil = useCallback(async () => {
    if (!task.trim() || phase === "running") return;
    setTransmissions([]);
    setActiveSeqIdx(-1);
    setThinkingId(null);
    setErrorMsg("");
    setPhase("running");

    const priorContext = [];

    for (let i = 0; i < COUNCIL_SEQUENCE.length; i++) {
      const seq   = COUNCIL_SEQUENCE[i];
      const agent = AGENTS.find(a => a.id === seq.agentId);

      setActiveSeqIdx(i);
      setThinkingId(agent.id);

      // small pause so UI registers the active state before API call
      await new Promise(r => setTimeout(r, 400));

      try {
        const result = await callKing(agent, task, priorContext);

        const entry = {
          id: Date.now() + i,
          agent,
          toAgent: seq.toId ? AGENTS.find(a => a.id === seq.toId) : null,
          mode: seq.mode,
          label: seq.label,
          narrative: result.narrative,
          technical: result.technical,
          status: agent.id === "cens"
            ? (result.technical.includes("🚫") ? "fail"
               : result.technical.includes("⚠")  ? "warn" : "pass")
            : "active",
        };

        setTransmissions(prev => [...prev, entry]);
        priorContext.push({
          agentName: agent.name,
          narrative: result.narrative,
          technical: result.technical,
        });

        setThinkingId(null);

        // brief pause between Kings
        await new Promise(r => setTimeout(r, 600));

      } catch (err) {
        setThinkingId(null);
        setErrorMsg(`${agent.name} failed: ${err.message}`);
        setPhase("error");
        return;
      }
    }

    setActiveSeqIdx(-1);
    setPhase("done");
  }, [task, phase]);

  const reset = () => {
    setTask(""); setPhase("idle"); setTransmissions([]);
    setActiveSeqIdx(-1); setThinkingId(null); setErrorMsg("");
  };

  // transmission count per agent for badge
  const txCount = (agentId) => transmissions.filter(t => t.agent.id === agentId).length;

  return (
    <div style={{
      width: "100%", minHeight: "100vh",
      background: "#060810",
      display: "flex", flexDirection: "column",
      fontFamily: "'Courier New', monospace",
      color: "#c8d0de",
      overflow: "hidden",
    }}>
      <style>{`
        @keyframes ringout    { 0%{transform:scale(1);opacity:0.7} 100%{transform:scale(1.7);opacity:0} }
        @keyframes speakdot   { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.3;transform:scale(0.6)} }
        @keyframes beampulse  { 0%,100%{opacity:0.9} 50%{opacity:0.45} }
        @keyframes centerpulse{ 0%,100%{opacity:0.85} 50%{opacity:0.35} }
        @keyframes thinking   { 0%,100%{transform:translateY(0);opacity:0.4} 50%{transform:translateY(-6px);opacity:1} }
        @keyframes slidein    { from{opacity:0;transform:translateX(14px)} to{opacity:1;transform:translateX(0)} }
        @keyframes flicker    { 0%,100%{opacity:1} 93%{opacity:1} 94%{opacity:0.88} 95%{opacity:1} }
        @keyframes shimmer    { 0%,100%{opacity:0.6} 50%{opacity:1} }
        .tx-entry { animation: slidein 0.3s ease-out; }
        .btn:hover { filter:brightness(1.25); transform:translateY(-1px); }
        .btn { transition:all 0.2s ease; cursor:pointer; }
        ::-webkit-scrollbar{width:4px} ::-webkit-scrollbar-track{background:#080a10} ::-webkit-scrollbar-thumb{background:#2a3040;border-radius:2px}
        textarea:focus { outline:none; border-color:#C9932A !important; box-shadow:0 0 0 2px #C9932A22 !important; }
      `}</style>

      {/* Scanlines */}
      <div style={{
        position: "fixed", inset: 0, pointerEvents: "none", zIndex: 1,
        background: "repeating-linear-gradient(0deg,transparent,transparent 2px,rgba(0,0,0,0.025) 2px,rgba(0,0,0,0.025) 4px)",
        animation: "flicker 10s infinite",
      }}/>

      {/* ── HEADER ──────────────────────────────────────────────────────── */}
      <div style={{
        position: "relative", zIndex: 10,
        borderBottom: "1px solid #1a1208",
        padding: "11px 24px",
        display: "flex", alignItems: "center", justifyContent: "space-between",
        background: "linear-gradient(90deg,#0a0806,#0c0a07,#0a0806)",
        boxShadow: "0 1px 24px #00000099",
      }}>
        <div style={{ display: "flex", alignItems: "center", gap: 14 }}>
          <div style={{
            width: 30, height: 30, flexShrink: 0,
            background: "linear-gradient(135deg,#C9932A,#7A5010)",
            clipPath: "polygon(50% 0%,100% 25%,100% 75%,50% 100%,0% 75%,0% 25%)",
            display: "flex", alignItems: "center", justifyContent: "center",
          }}>
            <span style={{ fontSize: 13 }}>♔</span>
          </div>
          <div>
            <div style={{ fontSize: 12, letterSpacing: 4, color: "#C9932A", fontWeight: 700 }}>
              PROJECT REGALIS
            </div>
            <div style={{ fontSize: 8, color: "#3a2410", letterSpacing: 2, marginTop: 1 }}>
              LIVE WAR ROOM · COUNCIL OF KINGS · CLAUDE-POWERED
            </div>
          </div>
        </div>
        <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
          <div style={{ display: "flex", alignItems: "center", gap: 6, fontSize: 9, letterSpacing: 2 }}>
            <div style={{
              width: 7, height: 7, borderRadius: "50%",
              background: phase === "running" ? "#1F9E6A"
                : phase === "done" ? "#C9932A"
                : phase === "error" ? "#C92A2A" : "#2a3444",
              boxShadow: phase === "running" ? "0 0 10px #1F9E6A" : "none",
              animation: phase === "running" ? "speakdot 1s infinite" : "none",
            }}/>
            <span style={{ color: phase === "running" ? "#1F9E6A" : phase === "done" ? "#C9932A" : phase === "error" ? "#C92A2A" : "#2a3444" }}>
              {phase === "idle" ? "AWAITING COMMAND" : phase === "running" ? "COUNCIL IN SESSION" : phase === "done" ? "MISSION SEALED" : "TRANSMISSION FAILED"}
            </span>
          </div>
          {phase !== "idle" && (
            <button className="btn" onClick={reset} style={{
              background: "#100c08", border: "1px solid #2a1a08",
              color: "#6a5a4a", padding: "5px 12px",
              fontSize: 8, letterSpacing: 2, borderRadius: 2,
            }}>↺ NEW SESSION</button>
          )}
        </div>
      </div>

      {/* ── MAIN LAYOUT ─────────────────────────────────────────────────── */}
      <div style={{ display: "flex", flex: 1, overflow: "hidden", position: "relative", zIndex: 5 }}>

        {/* LEFT — War Room */}
        <div style={{
          width: 580, flexShrink: 0,
          display: "flex", flexDirection: "column",
          borderRight: "1px solid #1a1208",
        }}>
          {/* Active transmission status bar */}
          <div style={{
            padding: "7px 18px", fontSize: 8, letterSpacing: 2.5,
            borderBottom: "1px solid #1a1208",
            display: "flex", justifyContent: "space-between", alignItems: "center",
            background: "#08060A", minHeight: 32,
          }}>
            <span style={{ color: "#2a1a10" }}>COUNCIL CHAMBER</span>
            {activeSeq && activeAgent && (
              <span style={{
                color: activeAgent.color, fontSize: 8, letterSpacing: 2,
                animation: "shimmer 1s infinite",
              }}>
                ⟶ {activeSeq.label.toUpperCase()}
              </span>
            )}
            {phase === "done" && (
              <span style={{ color: "#C9932A", fontSize: 8, letterSpacing: 2 }}>
                ♔ THE COUNCIL HAS SPOKEN
              </span>
            )}
          </div>

          {/* Table + Avatars */}
          <div style={{
            flex: 1, display: "flex", alignItems: "center", justifyContent: "center",
            position: "relative",
          }}>
            <div style={{ position: "relative", width: 560, height: 560 }}>

              {/* Ambient floor glow */}
              <div style={{
                position: "absolute",
                bottom: 0, left: "50%", transform: "translateX(-50%)",
                width: 480, height: 60,
                background: activeAgent
                  ? `radial-gradient(ellipse, ${activeAgent.color}1a, transparent 70%)`
                  : "transparent",
                filter: "blur(24px)",
                transition: "background 0.9s ease",
              }}/>

              <RoundTable
                activeAgentId={activeAgent?.id}
                toAgentId={toAgent?.id}
                transmissions={transmissions}
              />

              {/* Avatar nodes */}
              {AGENTS.map(agent => {
                const angle = seatAngle(agent.seat);
                const r = 242;
                const ax = 280 + Math.cos(angle) * r;
                const ay = 280 + Math.sin(angle) * r;
                return (
                  <div key={agent.id} style={{
                    position: "absolute",
                    left: ax, top: ay,
                    transform: "translate(-50%,-50%)",
                    zIndex: activeAgent?.id === agent.id ? 20 : 10,
                  }}>
                    {/* Chair shadow */}
                    <div style={{
                      position: "absolute", bottom: -14, left: "50%",
                      transform: "translateX(-50%)",
                      width: 72, height: 18,
                      background: `radial-gradient(ellipse, ${agent.color}28, transparent 70%)`,
                      filter: "blur(8px)",
                    }}/>
                    <AgentNode
                      agent={agent}
                      isActive={activeAgent?.id === agent.id}
                      isPeer={toAgent?.id === agent.id}
                      isThinking={thinkingId === agent.id}
                      transmissionCount={txCount(agent.id)}
                    />
                  </div>
                );
              })}
            </div>
          </div>

          {/* Task input */}
          <div style={{
            borderTop: "1px solid #1a1208",
            padding: "14px 18px",
            background: "#08060A",
          }}>
            {phase === "idle" || phase === "error" ? (
              <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
                {phase === "error" && (
                  <div style={{
                    padding: "10px 12px", border: "1px solid #C92A2A44",
                    borderRadius: 2, background: "#1a0808",
                  }}>
                    <div style={{ fontSize: 9, color: "#C92A2A", letterSpacing: 1, marginBottom: 4 }}>
                      ⚠ TRANSMISSION FAILED
                    </div>
                    <div style={{
                      fontSize: 10, color: "#ff9999", fontFamily: "monospace",
                      wordBreak: "break-word", lineHeight: 1.6,
                    }}>{errorMsg}</div>
                    <div style={{ fontSize: 8, color: "#5a3a3a", marginTop: 6, letterSpacing: 1 }}>
                      If you see "timed out" — the Claude.ai API bridge is unavailable. This requires claude.ai with artifacts enabled.
                    </div>
                  </div>
                )}
                <textarea
                  value={task}
                  onChange={e => setTask(e.target.value)}
                  placeholder="Describe what you want the Council to build or solve..."
                  rows={3}
                  style={{
                    width: "100%", background: "#0c0a0e",
                    border: "1px solid #2a1a08", borderRadius: 3,
                    color: "#c8d0de", fontSize: 11, lineHeight: 1.6,
                    padding: "10px 12px", resize: "none",
                    fontFamily: "monospace", letterSpacing: 0.5,
                    boxSizing: "border-box",
                  }}
                  onKeyDown={e => { if (e.key === "Enter" && e.metaKey) conveneCouncil(); }}
                />
                <div style={{ display: "flex", gap: 8, alignItems: "center" }}>
                  <button className="btn" onClick={conveneCouncil}
                    disabled={!task.trim()}
                    style={{
                      background: task.trim() ? "linear-gradient(135deg,#C9932A,#8B5E10)" : "#1a1208",
                      border: `1px solid ${task.trim() ? "#C9932A" : "#2a1a08"}`,
                      color: task.trim() ? "#fff" : "#2a1a08",
                      padding: "9px 22px", fontSize: 9, letterSpacing: 3,
                      borderRadius: 2, fontFamily: "monospace",
                      boxShadow: task.trim() ? "0 0 16px #C9932A44" : "none",
                    }}>
                    ♔ CONVENE THE COUNCIL
                  </button>
                  <span style={{ fontSize: 8, color: "#2a1a08", letterSpacing: 1 }}>
                    {task.trim() ? "⌘↵ to submit" : ""}
                  </span>
                  {/* Example tasks */}
                  <div style={{ marginLeft: "auto", display: "flex", gap: 6 }}>
                    {["REST API in Go", "React auth flow", "Python scraper"].map(ex => (
                      <button key={ex} className="btn" onClick={() => setTask(`Build a ${ex} with proper error handling and security best practices`)}
                        style={{
                          background: "transparent", border: "1px solid #2a1a08",
                          color: "#4a3a2a", padding: "4px 8px",
                          fontSize: 7.5, letterSpacing: 1, borderRadius: 2,
                        }}>{ex}</button>
                    ))}
                  </div>
                </div>
              </div>
            ) : phase === "running" ? (
              <div style={{ display: "flex", alignItems: "center", gap: 12, padding: "4px 0" }}>
                <div style={{ display: "flex", gap: 5 }}>
                  {COUNCIL_SEQUENCE.map((seq, i) => {
                    const ag = AGENTS.find(a => a.id === seq.agentId);
                    const done = i < activeSeqIdx;
                    const active = i === activeSeqIdx;
                    return (
                      <div key={i} style={{
                        width: active ? 32 : done ? 10 : 6,
                        height: 6, borderRadius: 3,
                        background: done ? ag.color : active ? ag.color : "#1a2030",
                        boxShadow: active ? `0 0 8px ${ag.color}` : "none",
                        transition: "all 0.4s ease",
                      }}/>
                    );
                  })}
                </div>
                <span style={{ fontSize: 9, color: "#6a5a4a", letterSpacing: 2 }}>
                  {activeSeq?.label.toUpperCase() || "PREPARING..."}
                </span>
              </div>
            ) : (
              <div style={{
                display: "flex", alignItems: "center", justifyContent: "space-between",
                padding: "4px 0",
              }}>
                <span style={{ fontSize: 9, color: "#C9932A", letterSpacing: 2 }}>
                  ♔ SESSION COMPLETE — {transmissions.length} TRANSMISSIONS LOGGED
                </span>
                <div style={{ display: "flex", gap: 6 }}>
                  {["narrative","technical"].map(m => (
                    <button key={m} className="btn" onClick={() => setViewMode(m)} style={{
                      background: viewMode===m ? "#C9932A22" : "transparent",
                      border: "1px solid #2a1a08",
                      color: viewMode===m ? "#C9932A" : "#3a2410",
                      padding: "5px 10px", fontSize: 8, letterSpacing: 1.5, borderRadius: 2,
                    }}>{m === "narrative" ? "⚔ NARR" : "⌨ TECH"}</button>
                  ))}
                </div>
              </div>
            )}
          </div>
        </div>

        {/* RIGHT — Dispatch Log */}
        <div style={{ flex: 1, display: "flex", flexDirection: "column", overflow: "hidden", minWidth: 0 }}>
          <div style={{
            padding: "7px 18px", fontSize: 8, letterSpacing: 3, color: "#2a1a10",
            borderBottom: "1px solid #1a1208",
            display: "flex", justifyContent: "space-between", alignItems: "center",
            background: "#08060A",
          }}>
            <span>LIVE DISPATCH LOG</span>
            <div style={{ display: "flex", gap: 6 }}>
              {phase === "done" && ["narrative","technical"].map(m => (
                <button key={m} className="btn" onClick={() => setViewMode(m)} style={{
                  background: viewMode===m ? "#C9932A22" : "transparent",
                  border: "1px solid #2a1a08",
                  color: viewMode===m ? "#C9932A" : "#3a2410",
                  padding: "4px 8px", fontSize: 7.5, letterSpacing: 1.5, borderRadius: 2,
                }}>{m === "narrative" ? "⚔ NARR" : "⌨ TECH"}</button>
              ))}
            </div>
          </div>

          <div ref={logRef} style={{
            flex: 1, overflowY: "auto",
            padding: "14px 16px",
            display: "flex", flexDirection: "column", gap: 10,
          }}>

            {/* Empty / idle state */}
            {transmissions.length === 0 && phase === "idle" && (
              <div style={{
                flex: 1, display: "flex", flexDirection: "column",
                alignItems: "center", justifyContent: "center",
                gap: 18, color: "#1a2030",
              }}>
                <div style={{ fontSize: 38, opacity: 0.4 }}>♔</div>
                <div style={{ textAlign: "center" }}>
                  <div style={{ fontSize: 10, letterSpacing: 3, marginBottom: 8 }}>
                    THE CHAMBER AWAITS YOUR COMMAND
                  </div>
                  <div style={{ fontSize: 8, color: "#111820", letterSpacing: 2, lineHeight: 2 }}>
                    DESCRIBE YOUR TASK ←<br/>
                    THE COUNCIL WILL ASSEMBLE<br/>
                    FOUR KINGS · REAL CLAUDE API · LIVE OUTPUT
                  </div>
                </div>
                <div style={{ display: "flex", gap: 8, flexWrap: "wrap", justifyContent: "center", maxWidth: 320 }}>
                  {AGENTS.map(ag => (
                    <div key={ag.id} style={{
                      display: "flex", alignItems: "center", gap: 6,
                      padding: "5px 10px", border: `1px solid ${ag.color}33`,
                      borderRadius: 2, fontSize: 8, color: ag.color + "88",
                      letterSpacing: 1,
                    }}>
                      <div style={{ width: 6, height: 6, borderRadius: "50%", background: ag.color, opacity: 0.5 }}/>
                      {ag.name}
                    </div>
                  ))}
                </div>
              </div>
            )}

            {/* Thinking indicator */}
            {thinkingId && (
              <div className="tx-entry" style={{
                border: `1px solid ${AGENTS.find(a=>a.id===thinkingId)?.color}44`,
                borderLeft: `3px solid ${AGENTS.find(a=>a.id===thinkingId)?.color}`,
                borderRadius: 3, padding: "12px 14px",
                background: "#0a0c12",
                display: "flex", alignItems: "center", gap: 12,
              }}>
                <div style={{
                  width: 32, height: 32, borderRadius: "50%", flexShrink: 0,
                  overflow: "hidden",
                  border: `2px solid ${AGENTS.find(a=>a.id===thinkingId)?.color}`,
                  background: "#0a0806",
                }}>
                  <svg width={32} height={32} viewBox="0 0 100 84"
                    dangerouslySetInnerHTML={{ __html: AGENTS.find(a=>a.id===thinkingId)?.face }}/>
                </div>
                <div>
                  <div style={{ fontSize: 9, color: AGENTS.find(a=>a.id===thinkingId)?.accent, letterSpacing: 1.5, marginBottom: 4 }}>
                    {AGENTS.find(a=>a.id===thinkingId)?.name.toUpperCase()}
                  </div>
                  <div style={{ display: "flex", gap: 5, alignItems: "center" }}>
                    {[0,1,2,3].map(i => (
                      <div key={i} style={{
                        width: 5, height: 5, borderRadius: "50%",
                        background: AGENTS.find(a=>a.id===thinkingId)?.color,
                        animation: `thinking 1.2s ease-in-out ${i*0.18}s infinite`,
                      }}/>
                    ))}
                    <span style={{ fontSize: 8, color: "#3a4454", letterSpacing: 1.5, marginLeft: 4 }}>
                      DELIBERATING...
                    </span>
                  </div>
                </div>
              </div>
            )}

            {/* Transmission entries */}
            {transmissions.map((tx) => {
              const statusColor = tx.status === "fail" ? "#C92A2A"
                : tx.status === "warn" ? "#C9932A"
                : tx.status === "pass" ? "#1F9E6A"
                : tx.agent.color;
              return (
                <div key={tx.id} className="tx-entry" style={{
                  border: `1px solid ${statusColor}33`,
                  borderLeft: `3px solid ${tx.agent.color}`,
                  borderRadius: 3,
                  background: tx.status === "fail" ? "#150808"
                    : tx.status === "warn" ? "#14100A"
                    : tx.status === "pass" ? "#08140C" : "#0a0c12",
                  padding: "12px 14px", position: "relative", overflow: "hidden",
                }}>
                  {/* Color wash */}
                  <div style={{
                    position: "absolute", inset: 0,
                    background: `radial-gradient(circle at 0% 50%, ${tx.agent.color}07, transparent 55%)`,
                    pointerEvents: "none",
                  }}/>

                  {/* Header */}
                  <div style={{
                    display: "flex", alignItems: "center", gap: 10,
                    marginBottom: 10, position: "relative",
                  }}>
                    <div style={{
                      width: 34, height: 34, borderRadius: "50%", flexShrink: 0,
                      overflow: "hidden",
                      border: `2px solid ${tx.agent.color}`,
                      background: "#0a0806",
                      boxShadow: `0 0 10px ${tx.agent.color}44`,
                    }}>
                      <svg width={34} height={34} viewBox="0 0 100 84"
                        dangerouslySetInnerHTML={{ __html: tx.agent.face }}/>
                    </div>
                    <div style={{ flex: 1 }}>
                      <div style={{ fontSize: 9, fontWeight: 700, letterSpacing: 1.5, color: tx.agent.accent }}>
                        {tx.agent.name.toUpperCase()}
                      </div>
                      <div style={{ fontSize: 7.5, color: "#3a4454", letterSpacing: 1, marginTop: 2 }}>
                        {tx.mode === "broadcast"
                          ? "⟶ ALL KINGS · BROADCAST"
                          : `⇢ ${tx.toAgent?.name.replace("Rex ","").toUpperCase()} · PEER`}
                      </div>
                    </div>
                    <div style={{ textAlign: "right" }}>
                      <div style={{
                        fontSize: 8, color: tx.agent.color,
                        border: `1px solid ${tx.agent.color}33`,
                        padding: "2px 8px", borderRadius: 2, letterSpacing: 1,
                        marginBottom: 3,
                      }}>{tx.label}</div>
                      {tx.status === "pass" && <div style={{ fontSize: 7.5, color: "#1F9E6A", letterSpacing: 1 }}>✓ CLEAR</div>}
                      {tx.status === "warn" && <div style={{ fontSize: 7.5, color: "#C9932A", letterSpacing: 1 }}>⚠ CONDITIONAL</div>}
                      {tx.status === "fail" && <div style={{ fontSize: 7.5, color: "#C92A2A", letterSpacing: 1 }}>🚫 BLOCKED</div>}
                    </div>
                  </div>

                  {/* Content */}
                  {viewMode === "narrative" ? (
                    <p style={{
                      margin: 0, fontSize: 12, lineHeight: 1.75,
                      color: "#9aa4b4", fontStyle: "italic",
                      fontFamily: "Georgia,'Times New Roman',serif",
                      position: "relative",
                    }}>
                      <span style={{ color: tx.agent.color, fontSize: 18, marginRight: 5, verticalAlign: "top", lineHeight: 1.2 }}>"</span>
                      {tx.narrative}
                      <span style={{ color: tx.agent.color, fontSize: 18, marginLeft: 4, verticalAlign: "bottom", lineHeight: 0 }}>"</span>
                    </p>
                  ) : (
                    tx.technical ? (
                      <pre style={{
                        margin: 0, fontSize: 9.5, lineHeight: 1.8,
                        color: "#7ab8e8", whiteSpace: "pre-wrap", wordBreak: "break-word",
                        fontFamily: "monospace",
                        background: "#05080D", padding: "10px 12px",
                        borderRadius: 2, border: "1px solid #1a2030",
                        position: "relative",
                      }}>{tx.technical}</pre>
                    ) : (
                      <p style={{ margin: 0, fontSize: 11, color: "#5a6a7a", fontStyle: "italic", fontFamily: "Georgia,serif" }}>
                        {tx.narrative}
                      </p>
                    )
                  )}
                </div>
              );
            })}

            {/* Mission complete banner */}
            {phase === "done" && (
              <div className="tx-entry" style={{
                border: "1px solid #C9932A44",
                borderRadius: 3, padding: "20px", textAlign: "center",
                background: "linear-gradient(135deg,#1a0d08,#0c0806)",
              }}>
                <div style={{ fontSize: 28, marginBottom: 8 }}>♔</div>
                <div style={{ fontSize: 11, letterSpacing: 4, color: "#C9932A", marginBottom: 6 }}>
                  THE COUNCIL HAS SPOKEN
                </div>
                <div style={{ fontSize: 8, color: "#6a5a4a", letterSpacing: 2, marginBottom: 12 }}>
                  {transmissions.length} TRANSMISSIONS · MISSION SEALED
                </div>
                <div style={{
                  display: "flex", gap: 8, justifyContent: "center", flexWrap: "wrap"
                }}>
                  {transmissions.filter(t => t.agent.id === "cens").map((t, i) => (
                    <div key={i} style={{
                      fontSize: 8, letterSpacing: 1.5,
                      color: t.status === "pass" ? "#1F9E6A" : t.status === "warn" ? "#C9932A" : "#C92A2A",
                      border: `1px solid ${t.status === "pass" ? "#1F9E6A44" : t.status === "warn" ? "#C9932A44" : "#C92A2A44"}`,
                      padding: "3px 10px", borderRadius: 2,
                    }}>
                      {t.status === "pass" ? "✓ AUDIT CLEAR" : t.status === "warn" ? "⚠ CONDITIONAL PASS" : "🚫 AUDIT BLOCKED"}
                    </div>
                  ))}
                </div>
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}
