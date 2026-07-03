<script setup>
    import { reactive } from 'vue';

    const posts = reactive([
    {
        id: 1,
        title: "EcoCharge",
        description: "Estações de recarga para veículos elétricos abastecidas com energia solar.",
        image: null,
    },
    {
        id: 2,
        title: "FinWise",
        description: "Aplicativo de gestão financeira pessoal com análise de gastos e projeções automáticas.",
        image: "ph3.png",
    },
    {
        id: 3,
        title: "SmartAgro",
        description: "Sistema de monitoramento agrícola com sensores IoT para otimizar irrigação e produtividade.",
        image: null,
    },
    {
        id: 4,
        title: "PicSphere",
        description: "Rede social para compartilhamento de fotos com filtros e álbuns colaborativos.",
        image: "ph1.png",
    },
    {
        id: 5,
        title: "HealthTrack",
        description: "Aplicativo para acompanhamento de saúde e hábitos, integrando dados de wearables",
        image: null,
    },
    {
        id: 6,
        title: "MentorHub",
        description: "Plataforma de conexão entre mentores e mentorados com videochamadas integradas.",
        image: "ph2.png",
    },
    ]);
</script>

<template>
<section id="projects" class="page-section">
    <div class="container">
        <div class="split-hero-container">
            <h1>Projects</h1>
            <p>Explore a selection of my work, showcasing how I approach design challenges. Each project reflects my commitment to creating user-centered experiences that blend functionality with aesthetic appeal.</p>
        </div>
    </div>

    <div class="projects-list">
        <div class="content-box project-row-card" v-for="post in posts">
            <div class="project-simple-header">
                <h2>{{ post.title }}</h2>
                <p class="project-subtitle">{{ post.description }}</p>
            </div>
            <div class="main-project-image">
                <img :src="'/images/'+post.image" alt="">
            </div>
        </div>
    </div>
        </section>
</template>