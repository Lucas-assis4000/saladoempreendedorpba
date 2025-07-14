<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sala do Empreendedor - Paranaíba/MS</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #0d6efd;
            --secondary-color: #198754;
            --accent-color: #ffc107;
            --dark-color: #212529;
            --light-color: #f8f9fa;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
        }
        
        .top-bar {
            background-color: var(--dark-color);
            color: white;
            padding: 5px 0;
            font-size: 0.9rem;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 15px 0;
        }
        
        .logo-prefeitura {
            height: 80px;
        }
        
        .logo-sala {
            height: 70px;
        }
        
        .navbar {
            background-color: var(--primary-color);
        }
        
        .navbar .nav-link {
            color: white !important;
            font-weight: 500;
            padding: 10px 15px;
            transition: all 0.3s;
        }
        
        .navbar .nav-link:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .hero-section {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://source.unsplash.com/random/1200x600/?business');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero-section h1 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .hero-section p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .service-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 30px;
            margin-bottom: 30px;
            transition: transform 0.3s;
            height: 100%;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .quick-access {
            background-color: var(--light-color);
            padding: 50px 0;
        }
        
        .quick-access-button {
            display: block;
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            transition: all 0.3s;
            text-decoration: none;
            font-weight: 600;
        }
        
        .quick-access-button:hover {
            background-color: var(--secondary-color);
            transform: scale(1.05);
            color: white;
        }
        
        .about-section {
            padding: 80px 0;
        }
        
        .about-section h2 {
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .about-section h2:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100px;
            height: 3px;
            background-color: var(--primary-color);
        }
        
        .contact-section {
            background-color: var(--light-color);
            padding: 80px 0;
        }
        
        .contact-info {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .contact-info i {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-right: 10px;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 20px;
        }
        
        footer h5 {
            color: var(--accent-color);
            margin-bottom: 20px;
        }
        
        footer ul {
            list-style: none;
            padding-left: 0;
        }
        
        footer ul li {
            margin-bottom: 10px;
        }
        
        footer ul li a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: all 0.3s;
        }
        
        footer ul li a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .copyright {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .selo-section {
            padding: 50px 0;
            background-color: white;
        }
        
        .selo-img {
            max-width: 150px;
            margin: 0 auto;
            display: block;
        }
        
        .news-card {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }
        
        .news-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .news-card .card-body {
            padding: 20px;
        }
        
        .news-card .card-title {
            font-size: 1.2rem;
            font-weight: 600;
        }
        
        .news-card .card-text {
            color: #6c757d;
        }
        
        .news-card .card-footer {
            background-color: white;
            border-top: 1px solid rgba(0, 0, 0, 0.1);
            padding: 15px 20px;
        }
        
        .whatsapp-button {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            background-color: #25d366;
            color: white;
            border-radius: 50%;
            text-align: center;
            font-size: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .whatsapp-button:hover {
            transform: scale(1.1);
            color: white;
        }
        
        @media (max-width: 768px) {
            .hero-section {
                padding: 60px 0;
            }
            
            .hero-section h1 {
                font-size: 2rem;
            }
            
            .logo-prefeitura, .logo-sala {
                height: 60px;
            }
        }
    </style>
</head>
<body>
    <!-- Top Bar -->
    <div class="top-bar">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <i class="fas fa-phone-alt me-2"></i> (67) 3669-0088
                    <i class="fas fa-envelope ms-3 me-2"></i> sicat.pba@gmail.com
                </div>
                <div class="col-md-6 text-end">
                    <a href="#" class="text-white me-3"><i class="fab fa-facebook"></i></a>
                    <a href="#" class="text-white me-3"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="text-white"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
        </div>
    </div>

    <!-- Logo Section -->
    <div class="container logo-container">
        <img src="https://www.paranaiba.ms.gov.br/portal/img/logo.png" alt="Prefeitura de Paranaíba" class="logo-prefeitura">
        <img src="https://sebrae.com.br/Sebrae/Portal%20Sebrae/UFs/MS/Anexos/sala%20do%20empreendedor.png" alt="Sala do Empreendedor" class="logo-sala">
    </div>

    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark">
        <div class="container">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#"><i class="fas fa-home me-1"></i> Início</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#sobre"><i class="fas fa-info-circle me-1"></i> Sobre</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#servicos"><i class="fas fa-briefcase me-1"></i> Serviços</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#mei"><i class="fas fa-user-tie me-1"></i> Sobre o MEI</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#noticias"><i class="fas fa-newspaper me-1"></i> Notícias</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contato"><i class="fas fa-envelope me-1"></i> Contato</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="container">
            <h1>Sala do Empreendedor de Paranaíba</h1>
            <p>Apoio completo para quem quer empreender. Aqui você encontra orientação, formalização e capacitação para o seu negócio.</p>
            <a href="#servicos" class="btn btn-primary btn-lg">Conheça Nossos Serviços</a>
        </div>
    </section>

    <!-- Quick Access Section -->
    <section class="quick-access" id="servicos">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Acesso Rápido aos Serviços</h2>
                <p>Clique nos botões abaixo para acessar diretamente os serviços mais procurados</p>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-file-invoice-dollar mb-3"></i><br>
                        Emissão de Guia
                    </a>
                </div>
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-file-alt mb-3"></i><br>
                        Nota Fiscal de Serviço
                    </a>
                </div>
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-box mb-3"></i><br>
                        Nota Fiscal de Produto
                    </a>
                </div>
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-calendar-check mb-3"></i><br>
                        Declaração Anual
                    </a>
                </div>
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-user-plus mb-3"></i><br>
                        Abertura do MEI
                    </a>
                </div>
                <div class="col-md-4">
                    <a href="#" class="quick-access-button">
                        <i class="fas fa-sync-alt mb-3"></i><br>
                        Regularize
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="py-5">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Nossos Serviços</h2>
                <p>Conheça todos os serviços oferecidos pela Sala do Empreendedor de Paranaíba</p>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-user-plus"></i>
                        <h3>Formalização</h3>
                        <p>Orientação e auxílio para formalização de Microempreendedores Individuais (MEI).</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-file-alt"></i>
                        <h3>Emissão de Documentos</h3>
                        <p>Emissão de DAS, notas fiscais, certidões e outros documentos necessários.</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-chalkboard-teacher"></i>
                        <h3>Capacitação</h3>
                        <p>Cursos, palestras e workshops para desenvolvimento do seu negócio.</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-handshake"></i>
                        <h3>Orientação Empresarial</h3>
                        <p>Consultoria e orientação para gestão e crescimento do seu negócio.</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-money-bill-wave"></i>
                        <h3>Acesso a Crédito</h3>
                        <p>Informações sobre linhas de crédito disponíveis para pequenos negócios.</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="service-card">
                        <i class="fas fa-gavel"></i>
                        <h3>Compras Governamentais</h3>
                        <p>Orientação sobre como participar de licitações e vender para o governo.</p>
                        <a href="#" class="btn btn-outline-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section" id="sobre">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-md-6">
                    <h2>O que é a Sala do Empreendedor?</h2>
                    <p>A Sala do Empreendedor de Paranaíba é um espaço destinado ao acolhimento dos empreendedores. Um centro especializado para o atendimento e orientação empresarial.</p>
                    <p>No local são oferecidos serviços gratuitos que incluem a orientação e a formalização das empresas, além da capacitação, com o objetivo de prover mecanismos de sustentabilidade ajudando seu negócio a prosperar.</p>
                    <p>A Sala do Empreendedor é o ponto de referência para abertura, alteração e baixa de empresas de forma simplificada e sem excesso de burocracia.</p>
                    <p>Além disso, na Sala do Empreendedor, o Microempreendedor Individual (MEI) recebe apoio especial para a formalização e gestão de seu negócio.</p>
                </div>
                <div class="col-md-6">
                    <img src="https://source.unsplash.com/random/600x400/?entrepreneur" alt="Sala do Empreendedor" class="img-fluid rounded">
                </div>
            </div>
        </div>
    </section>

    <!-- MEI Section -->
    <section class="py-5 bg-light" id="mei">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Microempreendedor Individual (MEI)</h2>
                <p>Conheça as vantagens de se tornar um MEI</p>
            </div>
            <div class="row">
                <div class="col-md-6">
                    <img src="https://source.unsplash.com/random/600x400/?business" alt="MEI" class="img-fluid rounded">
                </div>
                <div class="col-md-6">
                    <h3>O que é o MEI?</h3>
                    <p>O MEI é o menor porte empresarial que existe. Individual, com faturamento máximo R$ 81 mil por ano e limitado à contratação de apenas um funcionário. Além disso o empresário MEI não pode participar como sócio, administrador ou titular, de outras atividades empresariais.</p>
                    
                    <h4 class="mt-4">Benefícios do MEI:</h4>
                    <ul>
                        <li>Aposentadoria por idade</li>
                        <li>Aposentadoria por invalidez</li>
                        <li>Auxílio-doença</li>
                        <li>Salário maternidade</li>
                        <li>Dispensa de Alvará e Licenças para iniciar sua atividade</li>
                        <li>Obtenção do CNPJ, sem custo e sem burocracias</li>
                        <li>Acesso ao mercado formal</li>
                        <li>Baixo custo mensal</li>
                    </ul>
                    
                    <a href="#" class="btn btn-primary mt-3">Quero me tornar um MEI</a>
                </div>
            </div>
        </div>
    </section>

    <!-- News Section -->
    <section class="py-5" id="noticias">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Notícias e Eventos</h2>
                <p>Fique por dentro das novidades e eventos da Sala do Empreendedor</p>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="news-card">
                        <img src="https://source.unsplash.com/random/600x400/?workshop" alt="Notícia 1">
                        <div class="card-body">
                            <h5 class="card-title">Workshop de Marketing Digital para MEI</h5>
                            <p class="card-text">Aprenda a divulgar seu negócio nas redes sociais e atrair mais clientes.</p>
                        </div>
                        <div class="card-footer">
                            <small class="text-muted">15 de Abril de 2025</small>
                            <a href="#" class="btn btn-sm btn-outline-primary float-end">Leia mais</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="news-card">
                        <img src="https://source.unsplash.com/random/600x400/?meeting" alt="Notícia 2">
                        <div class="card-body">
                            <h5 class="card-title">Sala do Empreendedor recebe Selo Diamante do Sebrae</h5>
                            <p class="card-text">Reconhecimento pela qualidade no atendimento aos pequenos negócios.</p>
                        </div>
                        <div class="card-footer">
                            <small class="text-muted">10 de Abril de 2025</small>
                            <a href="#" class="btn btn-sm btn-outline-primary float-end">Leia mais</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="news-card">
                        <img src="https://source.unsplash.com/random/600x400/?business-seminar" alt="Notícia 3">
                        <div class="card-body">
                            <h5 class="card-title">Semana do MEI acontece em maio</h5>
                            <p class="card-text">Programação especial com palestras, oficinas e atendimento personalizado.</p>
                        </div>
                        <div class="card-footer">
                            <small class="text-muted">5 de Abril de 2025</small>
                            <a href="#" class="btn btn-sm btn-outline-primary float-end">Leia mais</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="text-center mt-4">
                <a href="#" class="btn btn-outline-primary">Ver todas as notícias</a>
            </div>
        </div>
    </section>

    <!-- Selo Section -->
    <section class="selo-section">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-4 text-center">
                    <img src="https://sebrae.com.br/Sebrae/Portal%20Sebrae/UFs/MS/Anexos/selo%20diamante.png" alt="Selo Diamante" class="selo-img">
                    <h4 class="mt-3">Selo Diamante</h4>
                    <p>Reconhecimento do Sebrae pela excelência no atendimento</p>
                </div>
                <div class="col-md-4 text-center">
                    <img src="https://sebrae.com.br/Sebrae/Portal%20Sebrae/UFs/MS/Anexos/selo%20ouro.png" alt="Selo Ouro" class="selo-img">
                    <h4 class="mt-3">Selo Ouro</h4>
                    <p>Reconhecimento do Sebrae pela qualidade no atendimento</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section" id="contato">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Entre em Contato</h2>
                <p>Estamos à disposição para atender e orientar você</p>
            </div>
            <div class="row">
                <div class="col-md-6">
                    <div class="contact-info">
                        <h4 class="mb-4">Informações de Contato</h4>
                        <p><i class="fas fa-map-marker-alt"></i> Piso Superior do Shopping Center - R. Maria Antônia, Centro, Paranaíba - MS, 79500-000</p>
                        <p><i class="fas fa-phone-alt"></i> (67) 3669-0088</p>
                        <p><i class="fas fa-envelope"></i> sicat.pba@gmail.com</p>
                        <p><i class="fas fa-clock"></i> Segunda a Sexta: 7h às 13h</p>
                        
                        <h5 class="mt-4 mb-3">Redes Sociais</h5>
                        <a href="#" class="btn btn-outline-primary me-2"><i class="fab fa-facebook"></i></a>
                        <a href="#" class="btn btn-outline-primary me-2"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="btn btn-outline-primary"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="col-md-6">
                    <form class="bg-white p-4 rounded shadow-sm">
                        <h4 class="mb-4">Envie uma Mensagem</h4>
                        <div class="mb-3">
                            <label for="name" class="form-label">Nome</label>
                            <input type="text" class="form-control" id="name" required>
                        </div>
                        <div class="mb-3">
                            <label for="email" class="form-label">E-mail</label>
                            <input type="email" class="form-control" id="email" required>
                        </div>
                        <div class="mb-3">
                            <label for="subject" class="form-label">Assunto</label>
                            <input type="text" class="form-control" id="subject" required>
                        </div>
                        <div class="mb-3">
                            <label for="message" class="form-label">Mensagem</label>
                            <textarea class="form-control" id="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <section class="py-5">
        <div class="container">
            <div class="text-center mb-5">
                <h2>Localização</h2>
                <p>Venha nos visitar</p>
            </div>
            <div class="ratio ratio-16x9">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3773.7887421527166!2d-51.19123692394752!3d-19.67454293669204!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9490a8f7e9d94e8d%3A0x4b0b7fb0e5b8db0!2sShopping%20Center%20Parana%C3%ADba!5e0!3m2!1spt-BR!2sbr!4v1682182436123!5m2!1spt-BR!2sbr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <h5>Sala do Empreendedor</h5>
                    <p>Um espaço dedicado ao apoio e desenvolvimento dos empreendedores de Paranaíba.</p>
                    <p>Uma parceria entre a Prefeitura Municipal de Paranaíba e o Sebrae.</p>
                </div>
                <div class="col-md-4">
                    <h5>Links Rápidos</h5>
                    <ul>
                        <li><a href="#">Início</a></li>
                        <li><a href="#sobre">Sobre</a></li>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#mei">Sobre o MEI</a></li>
                        <li><a href="#noticias">Notícias</a></li>
                        <li><a href="#contato">Contato</a></li>
                    </ul>
                </div>
                <div class="col-md-4">
                    <h5>Links Úteis</h5>
                    <ul>
                        <li><a href="https://www.gov.br/empresas-e-negocios/pt-br/empreendedor" target="_blank">Portal do Empreendedor</a></li>
                        <li><a href="https://www.sebrae.com.br" target="_blank">Sebrae</a></li>
                        <li><a href="https://www.paranaiba.ms.gov.br" target="_blank">Prefeitura de Paranaíba</a></li>
                        <li><a href="https://www.gov.br/receitafederal" target="_blank">Receita Federal</a></li>
                        <li><a href="https://www.jucems.ms.gov.br" target="_blank">Junta Comercial de MS</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright text-center">
                <p>&copy; 2025 Sala do Empreendedor de Paranaíba. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- WhatsApp Button -->
    <a href="https://wa.me/556736690000" class="whatsapp-button" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
