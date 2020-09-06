This is where LTSpice Simulations are stored.

archiv
In diesem Punkt soll die Kleinsignal-Spannungsverstärkung für die zwei verschiedenen Werte $R_E = \SI{0}{\ohm}$ und $R_E = \SI{33}{\ohm}$ berechnet werden. Am Arbeitspunkt, also am Wert von $r_{BE}$ sollte die Änderung des Emitterwiderstandes nichts verändern, da der Kollektorstrom in dieser Schaltung von einer Stromquelle getrieben wird und unabhängig vom Kollektorwiderstand ist.

Zur Berechung der gesuchten Größe $A_{ed} = \frac{u_a}{u_p - u_n}$ wird das Kleinsignalersatzschaltbild analysiert:

FALSCHER ANSATZ: Werd das Thema morgen (Samstag) vormittag ausbessern

\subsubsection{$u_a$ zufolge $u_p$}

\begin{align}
    u_p =& I_{B,1} r_{BE} + I_E 2 R_E + I_{B,2} r_{BE} \\
    I_{B,1} (B+1) =& I_E \\
    I_{B,2} (B+1) =& I_E \\
    u_a = r_{BE} I_{B,2}
\end{align}

Aus den beiden Knotengleichungen folgt, dass $I_{B,1} = I_{B,2} = I_B$ gelten muss:

\begin{align}
    u_p =& I_{B} \left( 2 r_{BE} + (B+1) 2 R_E \right) \rightarrow I_B = \frac{u_p}{2 \left( r_{BE} + (B+1) R_E \right)}\\
    u_a =& r_{BE} I_{B} = u_p \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)}
\end{align}

\subsubsection{$u_a$ zufolge $u_n$}

\begin{align}
    u_n =& I_{B,2} r_{BE} + I_E 2 R_E + I_{B,1} r_{BE} \\
    I_{B,2} (B+1) =& I_E \\
    I_{B,1} (B+1) =& I_E \\
    u_a = - r_{BE} I_{B,2} + u_n
\end{align}

Aus den beiden Knotengleichungen folgt, dass $I_{B,1} = I_{B,2} = I_B$ gelten muss:

\begin{align}
    u_n =& I_{B} \left( 2 r_{BE} + (B+1) 2 R_E \right) \rightarrow I_B = \frac{u_n}{2 \left( r_{BE} + (B+1) R_E \right)}\\
    u_a =& - r_{BE} I_{B} + u_n = u_n \left( 1 - \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)} \right)
\end{align}

\subsubsection{$u_a$ zufolge beider Quellen}

\begin{equation}
    u_a = u_p \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)} + u_n \left( 1 - \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)} \right)
\end{equation}

Mit $u_n = - u_p$ eingesetzt:

\begin{align}
    u_a &= u_p \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)} + u_p \left( - 1 + \frac{r_{BE}}{2 \left( r_{BE} + (B+1) R_E \right)} \right)\\
    u_a &= u_p \left(\frac{r_{BE}}{\left( r_{BE} + (B+1) R_E \right)} - 1 \right) \\
    \frac{u_a}{u_p - u_n} = 
\end{align}