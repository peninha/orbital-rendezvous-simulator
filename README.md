# Orbital Rendezvous Simulator

For the Portuguese version, scroll down to [Versao em portugues](#versao-em-portugues).

A tool for exploring and simulating 2D orbital rendezvous between a **Target** and a **Chaser**.

Orbital rendezvous is the set of maneuvers used to approach a target in space, usually with the goal of docking with it. It is not as simple as "point at the target and fire the engines". Far from it. It involves a sequence of maneuvers to match not only the target's trajectory, but also the exact same point in space at the right time, which is called orbital phase. This simulator makes that behavior visible: you configure the initial orbits, apply phasing burns, and watch the result both in a top-down orbital view and in the Target-relative frame.

## How To Open

Open `orbital_rendezvous_simulator.html` directly in a browser.

The simulator is a single HTML file. It uses Plotly from a CDN to render the plots, so it needs internet access to load the plotting library.

## Concepts

**Target** is the reference vehicle.

**Chaser** is the vehicle trying to approach the Target.

**NC** means **Nominal Catchup**. In this simulator, an NC is a tangential phasing burn used to change the Chaser's orbital period and phase relative to the Target. After an NC, the relative trajectory can change both the height of its peaks and valleys and the spacing between the waves.

**Circular orbit** uses orbit altitude and initial true longitude.

**Non-circular orbit** uses conventional orbital parameters: perigee altitude, apogee altitude, argument of perigee, and true anomaly from perigee.

## Plots

**Top-down orbital view** shows Earth, the orbits, and the Chaser trajectory. When an orbit is elliptical, the line of apsides shows the perigee-apogee direction.

**Target-relative frame** shows the Chaser motion as seen from the Target. In LVC (Local Vertical Curvilinear) mode, vertical dashed lines indicate later radial passes by the Target along the simulated trajectory.

## Presets

Presets are stored in the browser. You can save, remove, export, and import preset lists as JSON.

The **Terry Burlison's Example** preset is inspired by figures 8 and 9 of the excellent article [Rendezvous and Docking: A User's Guide for Non Rocket Scientists](https://www.baen.com/rendezvous), where Terry Burlison explains how orbital rendezvous works. I recommend reading it to get more out of this tool.

One important note: the fig. 9 example does not fully match the text description, and it also does not represent very well what happens in reality. When phasing burns (NC) occur, the oscillating trajectory does not only change the height of the peaks and valleys; the spacing between the waves changes too. This effect appears in the simulator.

## Model Limits

This is a simplified, coplanar, 2D simulator. It is useful for building intuition about phase, orbital period, and relative trajectory, but it is not a complete mission design tool.

Important simplifications:

- no orbital inclination or plane changes;
- no perturbations such as J2, atmospheric drag, or third bodies;
- burns are impulsive and tangential;
- the goal is education and intuition, not real mission certification.

## Tips

- Use LVC (Local Vertical Curvilinear) mode to understand the relation between orbital phase and radial distance.
- Adjust an NC burn and watch how the relative trajectory changes after it.
- Increase total simulation time to see future passes by the Target.
- Double-click sliders to return to zero or to the minimum allowed value.

---

# Versao em portugues

Uma ferramenta para explorar e simular o rendezvous orbital em 2D entre um **Target** e um **Chaser**.

Rendezvous orbital e o conjunto de manobras realizado para se aproximar de um alvo (Target) no espaco, normalmente com o intuito de acoplar com ele. Nao e algo simples como "apontar para o alvo e acionar os motores". Longe disso. Envolve uma serie de manobras para conseguir igualar nao so a trajetoria do alvo, mas tambem o mesmo ponto exato no espaco no momento certo, o que chamamos de fase orbital. Este simulador deixa esse comportamento visivel: voce configura as orbitas iniciais, aplica queimas de fase e acompanha o resultado tanto na vista orbital superior quanto no frame relativo do Target.

## Como Abrir

Abra o arquivo `orbital_rendezvous_simulator.html` diretamente no navegador.

O simulador e um unico HTML. Ele usa Plotly via CDN para renderizar os graficos, entao precisa de internet para carregar a biblioteca.

## Conceitos

**Target** e o veiculo de referencia.

**Chaser** e o veiculo que tenta se aproximar do Target.

**NC** significa **Nominal Catchup**. No simulador, uma NC e uma queima tangencial usada para alterar o periodo orbital do Chaser e mudar sua fase em relacao ao Target. Depois de uma NC, a trajetoria relativa pode mudar tanto a altura dos picos e vales quanto o espacamento entre as ondas.

**Orbita circular** usa altitude da orbita e longitude verdadeira inicial.

**Orbita nao circular** usa parametros orbitais mais convencionais: altitude do perigeu, altitude do apogeu, argumento do perigeu e anomalia verdadeira a partir do perigeu.

## Graficos

**Vista orbital superior** mostra a Terra, as orbitas e a trajetoria do Chaser. Quando a orbita e eliptica, a linha das apsides indica a direcao perigeu-apogeu.

**Frame relativo do Target** mostra o movimento do Chaser visto a partir do Target. No modo LVC (Local Vertical Curvilinear), linhas verticais tracejadas indicam novas passagens radiais pelo Target ao longo da trajetoria simulada.

## Presets

Os presets ficam salvos no navegador. Voce pode salvar, remover, exportar e importar listas em JSON.

O preset **Terry Burlison's Example** e inspirado nas figuras 8 e 9 do excelente artigo [Rendezvous and Docking: A User's Guide for Non Rocket Scientists](https://www.baen.com/rendezvous), em que Terry Burlison explica como funciona o rendezvous orbital. Recomendo ler o artigo para usar melhor esta ferramenta.

Uma observacao importante: o exemplo da fig. 9 nao bate totalmente com a descricao do texto e tambem nao representa bem o que acontece na realidade. Quando ocorrem queimas de fase (NC), a trajetoria oscilante nao muda apenas a altura dos picos e vales; o espacamento entre as ondas tambem muda. Esse efeito aparece no simulador.

## Limites Do Modelo

Este e um simulador 2D, coplanar e simplificado. Ele e otimo para intuicao de fase, periodo orbital e trajetoria relativa, mas nao substitui uma ferramenta de missao completa.

Algumas simplificacoes importantes:

- nao ha inclinacao orbital nem diferenca de plano;
- nao ha perturbacoes como J2, arrasto atmosferico ou terceiro corpo;
- as queimas sao impulsivas e tangenciais;
- o foco e didatico, nao certificacao de manobras reais.

## Dicas

- Use o modo LVC (Local Vertical Curvilinear) para entender melhor a relacao entre fase orbital e distancia radial.
- Ajuste uma queima NC e observe como a trajetoria relativa muda depois dela.
- Aumente o tempo total de simulacao para ver passagens futuras pelo Target.
- De duplo clique em sliders para voltar ao zero ou ao menor valor permitido.
