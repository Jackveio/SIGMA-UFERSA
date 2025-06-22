<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SIGMA - Sistema de Gestão de Materiais UFERSA</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }
        .bottom-nav {
            box-shadow: 0 -2px 15px rgba(0, 0, 0, 0.05);
        }
        .bottom-nav-item {
            transition: all 0.2s ease-in-out;
            border-radius: 9999px;
             padding: 4px 12px;
        }
        .bottom-nav-item.active {
            background-color: #e6f2ef; /* A very light green */
        }
        .bottom-nav-item.active i, .bottom-nav-item.active span {
            color: #007A4D; /* UFERSA Green */
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 250px;
            max-height: 350px;
        }
        .toast {
            transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
            transform: translateY(-100%);
            opacity: 0;
        }
        .toast.show {
            transform: translateY(20px);
            opacity: 1;
        }
        .main-view, .auth-view {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .btn-primary-shine {
            position: relative;
            overflow: hidden;
        }
        .btn-primary-shine::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.4) 0%, rgba(255,255,255,0) 70%);
            transform: rotate(45deg);
            transition: transform 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            opacity: 0;
        }
        .btn-primary-shine:hover::after {
            transform: scale(2) rotate(45deg);
            opacity: 1;
            transition: opacity 0.8s ease;
        }
        .material-card, .btn-secondary, .btn-action, .quick-panel-card {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .material-card:hover, .btn-action:hover, .quick-panel-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        }
        .chart-filter-btn, .category-filter-btn {
            transition: all 0.2s ease-in-out;
        }
        .chart-filter-btn.active, .category-filter-btn.active {
            background-color: #007A4D;
            color: white;
            box-shadow: 0 2px 10px rgba(0, 122, 77, 0.3);
        }
        .gemini-btn .fa-spinner {
            display: none;
        }
        .gemini-btn.loading .fa-spinner {
            display: inline-block;
        }
        .gemini-btn.loading .btn-text {
            display: none;
        }
        .materials-carousel {
            display: flex;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            gap: 1rem;
            padding-bottom: 1rem;
        }
        .materials-carousel::-webkit-scrollbar {
            height: 8px;
        }
        .materials-carousel::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        .materials-carousel::-webkit-scrollbar-thumb {
            background: #ccc;
            border-radius: 10px;
        }
        .materials-carousel::-webkit-scrollbar-thumb:hover {
            background: #aaa;
        }
        .material-carousel-card {
            scroll-snap-align: start;
            flex: 0 0 160px;
        }
    </style>
</head>
<body class="bg-gray-100 text-gray-800">

    <div id="app-container" class="max-w-lg mx-auto bg-white min-h-screen shadow-lg">
        
        <!-- ===================================================================== -->
        <!-- AUTHENTICATION VIEWS -->
        <!-- ===================================================================== -->
        <div id="login-screen" class="auth-view p-8 flex flex-col h-screen justify-center bg-gradient-to-br from-green-50 to-blue-50">
            <div class="text-center mb-12">
                <i class="fas fa-cubes text-5xl text-green-700"></i>
                <h1 class="text-4xl font-bold text-gray-800 mt-4">SIGMA</h1>
                <p class="text-gray-500">Gestão de Materiais da UFERSA</p>
            </div>
            <div class="space-y-4">
                <div class="relative">
                    <i class="fas fa-envelope absolute left-4 top-1/2 -translate-y-1/2 text-gray-400"></i>
                    <input type="email" id="login-email" value="admin@ufersa.edu.br" placeholder="Email Institucional" class="mt-1 block w-full pl-12 pr-4 py-3 bg-white border border-gray-300 rounded-xl shadow-sm focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-green-500">
                </div>
                <div class="relative">
                    <i class="fas fa-lock absolute left-4 top-1/2 -translate-y-1/2 text-gray-400"></i>
                    <input type="password" id="login-password" value="123456" placeholder="Senha" class="mt-1 block w-full pl-12 pr-10 py-3 bg-white border border-gray-300 rounded-xl shadow-sm focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-green-500">
                    <button type="button" onclick="togglePasswordVisibility('login-password')" class="absolute right-4 top-1/2 -translate-y-1/2 text-gray-500"><i class="fas fa-eye"></i></button>
                </div>
            </div>
            <div class="mt-8">
                <button onclick="handleLogin()" class="w-full bg-green-700 text-white font-bold py-3 px-4 rounded-xl hover:bg-green-800 transition-all shadow-lg hover:shadow-xl btn-primary-shine">
                    Entrar
                </button>
            </div>
            <div class="text-center mt-6 text-sm flex justify-center items-center gap-4">
               <a href="#" onclick="showRecovery()" class="font-medium text-green-700 hover:text-green-800">Esqueceu a senha?</a>
                <div class="h-4 w-px bg-gray-300"></div>
                <a href="#" onclick="showSignUp()" class="font-medium text-green-700 hover:text-green-800">Cadastre-se</a>
            </div>
        </div>

        <div id="signup-screen" class="auth-view p-8 flex-col h-screen justify-center hidden">
            <div class="text-center mb-8">
                <h1 class="text-3xl font-bold text-gray-800">Criar Conta</h1>
                <p class="text-gray-500">Junte-se ao SIGMA</p>
                 <p class="mt-4 text-xs text-center text-blue-800 bg-blue-50 p-2 rounded-lg border border-blue-200">
                    <i class="fas fa-info-circle mr-1"></i>
                    O nome e a matrícula devem ser os mesmos cadastrados no SIGAA.
                </p>
            </div>
            <div id="signup-form" class="space-y-4">
                <input type="text" id="signup-name" placeholder="Nome Completo" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
                <input type="email" id="signup-email" placeholder="Email Institucional" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
                <input type="text" id="signup-id" placeholder="Matrícula / ID" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
                <div>
                    <input type="password" id="signup-password" onkeyup="checkPasswordStrength(this.value)" placeholder="Senha" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
                    <div class="flex mt-2 space-x-1" id="password-strength-meter">
                        <div class="h-1 rounded-full flex-1 bg-gray-200"></div>
                        <div class="h-1 rounded-full flex-1 bg-gray-200"></div>
                        <div class="h-1 rounded-full flex-1 bg-gray-200"></div>
                        <div class="h-1 rounded-full flex-1 bg-gray-200"></div>
                    </div>
                    <p id="password-strength-text" class="text-xs text-right mt-1 text-gray-500"></p>
                </div>
                 <select id="signup-usertype" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm text-gray-500">
                    <option value="" disabled selected>Tipo de Usuário</option>
                    <option value="student">Aluno</option>
                    <option value="teacher">Professor</option>
                    <option value="staff">Servidor</option>
                </select>
            </div>
            <div class="mt-6 space-y-3">
                <button onclick="handleSignUp()" class="w-full bg-green-700 text-white font-bold py-3 px-4 rounded-xl hover:bg-green-800 btn-secondary">Cadastrar</button>
                <button onclick="showLogin()" class="w-full bg-gray-200 text-gray-800 font-bold py-3 px-4 rounded-xl hover:bg-gray-300 btn-secondary">Voltar para o Login</button>
            </div>
        </div>
        
        <div id="recovery-screen" class="auth-view p-8 flex-col h-screen justify-center hidden">
            <div class="text-center mb-8">
                <h1 class="text-3xl font-bold text-gray-800">Recuperar Senha</h1>
                <p class="text-gray-500">Enviaremos um link para seu email.</p>
            </div>
            <div class="space-y-4">
                <input type="email" id="recovery-email" placeholder="Email Institucional" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
            </div>
            <div class="mt-6 space-y-3">
                <button onclick="sendRecoveryLink()" class="w-full bg-green-700 text-white font-bold py-3 px-4 rounded-xl hover:bg-green-800 btn-secondary">Enviar Link</button>
                <button onclick="showLogin()" class="w-full bg-gray-200 text-gray-800 font-bold py-3 px-4 rounded-xl hover:bg-gray-300 btn-secondary">Voltar para o Login</button>
            </div>
        </div>

        <div id="reset-password-screen" class="auth-view p-8 flex-col h-screen justify-center hidden">
            <div class="text-center mb-8">
                <h1 class="text-3xl font-bold text-gray-800">Redefinir Senha</h1>
                <p class="text-gray-500">Crie uma nova senha para sua conta.</p>
            </div>
            <div class="space-y-4">
                <input type="password" id="reset-new-password" placeholder="Nova Senha" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
                <input type="password" id="reset-confirm-password" placeholder="Confirmar Nova Senha" class="block w-full px-3 py-2 bg-white border border-gray-300 rounded-xl shadow-sm">
            </div>
            <div class="mt-6 space-y-3">
                <button onclick="resetPassword()" class="w-full bg-green-700 text-white font-bold py-3 px-4 rounded-xl hover:bg-green-800 btn-secondary">Redefinir Senha</button>
                <button onclick="showLogin()" class="w-full bg-gray-200 text-gray-800 font-bold py-3 px-4 rounded-xl hover:bg-gray-300 btn-secondary">Voltar para o Login</button>
            </div>
        </div>

        <!-- ===================================================================== -->
        <!-- MAIN APPLICATION VIEWS -->
        <!-- ===================================================================== -->
        <div id="main-app" class="hidden pb-24">
            
            <div id="home-view" class="main-view">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10">
                    <div class="flex items-center">
                        <img id="header-avatar" src="https://placehold.co/40x40/007A4D/FFFFFF?text=AT" alt="Avatar" class="w-10 h-10 rounded-full object-cover">
                        <div class="ml-3">
                            <h2 id="home-username" class="text-lg font-bold">Olá, Aluno Teste!</h2>
                            <p class="text-sm text-gray-500">Bem-vindo(a) de volta.</p>
                        </div>
                    </div>
                </header>
                <main class="p-4 md:p-6 space-y-8">
                    <section>
                        <h3 class="font-bold text-xl mb-4 text-gray-700">Meu Status</h3>
                        <div id="quick-panel" class="grid grid-cols-2 gap-4"></div>
                    </section>
                    <section>
                        <h3 class="font-bold text-xl mb-4 text-gray-700">Disponíveis Hoje</h3>
                        <div id="available-today-carousel" class="materials-carousel"></div>
                    </section>
                     <section>
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="font-bold text-xl text-gray-700">Atividade de Empréstimos</h3>
                            <div id="chart-filters" class="flex bg-gray-200 rounded-full p-1">
                                <button onclick="updateLoanChart('6M')" class="chart-filter-btn active text-sm font-semibold py-1 px-3 rounded-full">6M</button>
                                <button onclick="updateLoanChart('1Y')" class="chart-filter-btn text-sm font-semibold py-1 px-3 rounded-full">1A</button>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-xl shadow-sm">
                            <div class="chart-container">
                                <canvas id="loansChart"></canvas>
                            </div>
                            <div id="chart-stats" class="mt-4 pt-4 border-t border-gray-200 grid grid-cols-3 gap-2 text-center">
                            </div>
                        </div>
                    </section>
                </main>
            </div>

            <div id="request-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex justify-between items-center">
                    <h2 class="text-xl font-bold text-center text-gray-800 flex-1">Solicitar Material</h2>
                    <button id="wishlist-btn" onclick="showWishlistModal()" class="relative bg-gray-100 px-3 py-2 rounded-full hover:bg-gray-200">
                        <i class="fas fa-heart text-red-500"></i>
                        <span id="wishlist-count" class="absolute -top-1 -right-1 bg-red-500 text-white text-xs rounded-full h-4 w-4 flex items-center justify-center">0</span>
                    </button>
                </header>
                <main class="p-4 md:p-6">
                    <div class="mb-4">
                        <input type="text" id="search-material" onkeyup="filterMaterials()" placeholder="🔎 Buscar por nome do material..." class="w-full px-4 py-3 border border-gray-300 rounded-xl">
                    </div>
                    <div id="category-filters" class="mb-4 flex flex-wrap gap-2"></div>
                    <div id="material-list" class="space-y-4"></div>
                    <div class="mt-8">
                        <h3 class="font-bold text-xl mb-4 text-gray-700">Próximas Devoluções</h3>
                        <div id="unavailable-list" class="space-y-4"></div>
                    </div>
                </main>
            </div>

            <div id="history-view" class="main-view hidden">
                 <header class="bg-white p-4 shadow-sm sticky top-0 z-10"><h2 class="text-xl font-bold text-center text-gray-800">Meus Empréstimos</h2></header>
                 <main class="p-4 md:p-6">
                    <div class="mb-4 border-b border-gray-200">
                        <nav class="flex -mb-px" id="history-tabs">
                            <button onclick="switchHistoryTab('active')" class="tab-button border-b-2 border-green-700 text-green-700 py-3 px-4 font-semibold">Solicitações</button>
                            <button onclick="switchHistoryTab('past')" class="tab-button border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300 py-3 px-4 font-semibold">Histórico</button>
                        </nav>
                    </div>
                    <div id="history-tab-active" class="space-y-3"></div>
                    <div id="history-tab-past" class="space-y-3 hidden"></div>
                </main>
            </div>
            
            <div id="admin-view" class="main-view hidden">
                 <header class="bg-white p-4 shadow-sm sticky top-0 z-10"><h2 class="text-xl font-bold text-center text-gray-800">Painel do Administrador</h2></header>
                <main class="p-4 md:p-6 space-y-6">
                    <section><h3 class="font-bold text-xl mb-4 text-gray-700">Solicitações Pendentes</h3><div id="admin-requests-list" class="space-y-3"></div></section>
                    <section><h3 class="font-bold text-xl mb-4 text-gray-700">Registrar Devolução e Punições</h3><div id="admin-punishment-section" class="space-y-3"></div></section>
                    <section><h3 class="font-bold text-xl mb-4 text-gray-700">Gerenciar Usuários</h3><div id="admin-users-list" class="space-y-3"></div></section>
                    <section><h3 class="font-bold text-xl mb-4 text-gray-700">Inventário de Itens</h3><div id="admin-inventory-list" class="space-y-3"></div></section>
                </main>
            </div>

            <div id="profile-view" class="main-view hidden bg-gray-50">
                <main class="p-0">
                    <div class="relative pb-16">
                        <div class="h-32 rounded-b-3xl bg-gradient-to-r from-green-600 to-teal-500"></div>
                        <div class="absolute top-20 left-1/2 -translate-x-1/2">
                            <img id="profile-avatar" src="https://placehold.co/80x80/007A4D/FFFFFF?text=AT" alt="Avatar grande" class="w-24 h-24 rounded-full border-4 border-white shadow-lg object-cover">
                        </div>
                    </div>

                    <div class="text-center pt-2 px-4">
                        <h3 id="profile-username" class="text-2xl font-bold">Aluno Teste</h3>
                        <p id="profile-email" class="text-gray-500">aluno.teste@ufersa.edu.br</p>
                        <p id="profile-matricula" class="text-gray-500 text-sm mb-4">Matrícula: 202412345</p>
                        <div id="user-status-badge" class="px-3 py-1 text-sm font-semibold rounded-full inline-block"></div>
                    </div>

                    <div class="w-full mt-6 space-y-2 px-4">
                        <button onclick="navigate('edit-profile')" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-edit w-6 mr-2 text-gray-500"></i>Editar Perfil</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                        <button onclick="navigate('change-password')" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-key w-6 mr-2 text-gray-500"></i>Alterar Senha</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                        <button onclick="navigate('notifications')" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-bell w-6 mr-2 text-gray-500"></i>Notificações</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                        <button onclick="navigate('about')" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-info-circle w-6 mr-2 text-gray-500"></i>Sobre o App</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                        <button onclick="navigate('privacy')" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-shield-alt w-6 mr-2 text-gray-500"></i>Políticas de Privacidade</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                        <button onclick="showShareModal()" class="btn-action w-full bg-white text-left p-4 rounded-xl flex justify-between items-center shadow-sm"><span><i class="fas fa-share-alt w-6 mr-2 text-gray-500"></i>Compartilhar App</span><i class="fas fa-chevron-right text-gray-400"></i></button>
                    </div>
                    <div class="px-4 pb-4">
                        <button onclick="logout()" class="w-full mt-8 bg-red-100 text-red-700 font-bold py-3 px-4 rounded-xl hover:bg-red-200 transition-colors btn-secondary">Sair (Logout)</button>
                    </div>
                </main>
            </div>

            <div id="edit-profile-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Editar Perfil</h2></header>
                <main class="p-4 md:p-6 space-y-4">
                    <div class="flex flex-col items-center"><div class="relative"><img id="edit-profile-avatar" src="https://placehold.co/100x100/007A4D/FFFFFF?text=AT" alt="Avatar editável" class="w-24 h-24 rounded-full mb-2 border-4 border-white shadow-lg object-cover"><button onclick="triggerAvatarUpload()" class="absolute bottom-0 right-0 bg-green-800 text-white w-8 h-8 rounded-full flex items-center justify-center border-2 border-white"><i class="fas fa-camera"></i></button></div><input type="file" id="avatar-upload" class="hidden" accept="image/*" onchange="previewAvatar(event)"></div>
                    <div><label class="text-sm font-medium">Nome Completo</label><input type="text" id="edit-profile-name" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <div><label class="text-sm font-medium">Email Institucional</label><input type="email" id="edit-profile-email" disabled class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl bg-gray-100 text-gray-500"></div>
                    <div><label class="text-sm font-medium">Matrícula</label><input type="text" id="edit-profile-id" disabled class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl bg-gray-100 text-gray-500"></div>
                    <button onclick="saveProfileChanges()" class="w-full mt-4 bg-green-700 text-white font-bold py-3 rounded-xl btn-secondary">Salvar Alterações</button>
                </main>
            </div>

            <div id="change-password-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Alterar Senha</h2></header>
                <main class="p-4 md:p-6 space-y-4">
                    <div><label class="text-sm font-medium">Senha Atual</label><input type="password" id="current-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <div class="text-right text-sm -mt-2"><a href="#" onclick="forgotCurrentPassword()" class="font-medium text-green-700 hover:text-green-800">Esqueceu a senha atual?</a></div>
                    <div><label class="text-sm font-medium">Nova Senha</label><input type="password" id="new-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <div><label class="text-sm font-medium">Confirmar Nova Senha</label><input type="password" id="confirm-new-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <button onclick="handleChangePassword()" class="w-full mt-4 bg-green-700 text-white font-bold py-3 rounded-xl btn-secondary">Alterar Senha</button>
                </main>
            </div>
            
            <div id="notifications-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Notificações</h2></header>
                <main class="p-4 md:p-6 space-y-3">
                    <div class="bg-blue-50 p-4 rounded-xl flex items-start gap-3"><i class="fas fa-info-circle text-blue-500 mt-1"></i><div><p class="font-semibold">Devolução Próxima</p><p class="text-sm text-gray-600">Seu empréstimo do item "Notebook Dell Vostro" vence em 3 dias.</p></div></div>
                    <div class="bg-green-50 p-4 rounded-xl flex items-start gap-3"><i class="fas fa-check-circle text-green-500 mt-1"></i><div><p class="font-semibold">Empréstimo Aprovado</p><p class="text-sm text-gray-600">Sua solicitação para "Câmera DSLR" foi aprovada. Retire no setor Audiovisual.</p></div></div>
                    <div class="bg-gray-100 p-4 rounded-xl flex items-start gap-3"><i class="fas fa-history text-gray-500 mt-1"></i><div><p class="font-semibold">Item Devolvido</p><p class="text-sm text-gray-600">Você devolveu o item "Caixa de Som Amplificada" com sucesso.</p></div></div>
                </main>
            </div>
            
            <div id="about-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Sobre o SIGMA</h2></header>
                <main class="p-4 md:p-6 text-gray-700 space-y-4">
                    <div class="text-center"><i class="fas fa-cubes text-6xl text-green-700"></i><h3 class="text-2xl font-bold mt-2">SIGMA v1.0</h3><p>Sistema de Gestão de Materiais</p></div>
                    <p>O SIGMA é uma plataforma robusta e intuitiva, projetada para modernizar e otimizar o processo de solicitação, gerenciamento e devolução de materiais e equipamentos na Universidade Federal Rural do Semi-Árido (UFERSA).</p>
                     <h4 class="font-bold text-lg pt-2">Nossa Missão</h4>
                    <p>Facilitar o acesso a recursos acadêmicos, promovendo a eficiência operacional e a responsabilidade no uso de equipamentos da universidade. Nosso objetivo é proporcionar uma ferramenta centralizada e eficiente para alunos, professores e servidores.</p>
                     <h4 class="font-bold text-lg pt-2">Desenvolvedores</h4>
                     <p>Este sistema foi concebido e desenvolvido por uma equipe dedicada de estudantes e profissionais da UFERSA, comprometidos com a inovação e a melhoria contínua dos serviços universitários.</p>
                    <p class="text-center text-sm text-gray-500 mt-8">&copy; 2025 UFERSA. Todos os direitos reservados.</p>
                </main>
            </div>
            
            <div id="privacy-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Políticas de Privacidade</h2></header>
                <main class="p-4 md:p-6 text-gray-700 space-y-4">
                    <p class="text-sm text-gray-500">Última atualização: 15 de Junho de 2025</p>
                    <h3 class="font-bold text-lg">1. Coleta de Informações</h3><p class="text-sm">Coletamos informações que você nos fornece diretamente ao se cadastrar, como nome completo, email institucional e número de matrícula. Também registramos dados de suas atividades, como solicitações, empréstimos e devoluções para garantir a integridade do serviço.</p>
                    <h3 class="font-bold text-lg">2. Uso das Informações</h3><p class="text-sm">As informações são utilizadas para: operar, manter e melhorar nossos serviços; processar suas solicitações de empréstimo; enviar notificações importantes sobre devoluções, status de solicitações e possíveis sanções; e garantir a segurança do nosso sistema e da comunidade acadêmica.</p>
                    <h3 class="font-bold text-lg">3. Compartilhamento e Segurança</h3><p class="text-sm">Não compartilhamos suas informações pessoais com terceiros, exceto quando necessário para cumprir com a lei ou para proteger nossos direitos. A segurança dos seus dados é nossa prioridade, e utilizamos práticas de mercado para proteger suas informações contra acesso não autorizado.</p>
                    <h3 class="font-bold text-lg">4. Seus Direitos</h3><p class="text-sm">Você tem o direito de acessar e editar suas informações de perfil a qualquer momento. Caso deseje excluir sua conta, entre em contato com a administração do sistema. A exclusão de dados estará sujeita às políticas de retenção de registros da universidade.</p>
                    <h3 class="font-bold text-lg">5. Contato</h3><p class="text-sm">Se tiver qualquer dúvida sobre estas políticas, por favor, entre em contato conosco através do e-mail: <a href="mailto:suporte.sigma@ufersa.edu.br" class="text-green-700 hover:underline">suporte.sigma@ufersa.edu.br</a>.</p>
                </main>
            </div>

             <div id="confirm-code-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('profile')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Redefinir Senha</h2></header>
                <main class="p-4 md:p-6 space-y-4">
                    <p class="text-center text-sm text-gray-600">Insira o código enviado para o seu email e crie uma nova senha.</p>
                    <div><label class="text-sm font-medium">Código de Confirmação</label><input type="text" id="confirm-code-input" placeholder="_ _ _ _ _ _" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl text-center tracking-[1em]"></div>
                    <div><label class="text-sm font-medium">Nova Senha</label><input type="password" id="confirm-new-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <div><label class="text-sm font-medium">Confirmar Nova Senha</label><input type="password" id="confirm-confirm-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-xl"></div>
                    <button onclick="saveNewPasswordFromProfile()" class="w-full mt-4 bg-green-700 text-white font-bold py-3 rounded-xl btn-secondary">Redefinir Senha</button>
                </main>
            </div>
            
            <div id="manage-user-view" class="main-view hidden">
                <header class="bg-white p-4 shadow-sm sticky top-0 z-10 flex items-center"><button onclick="navigate('admin')" class="mr-4"><i class="fas fa-arrow-left text-xl"></i></button><h2 class="text-xl font-bold text-gray-800">Gerenciar Usuário</h2></header>
                <main class="p-4 md:p-6 space-y-4">
                    <input type="hidden" id="manage-user-id">
                    <div class="text-center">
                        <h3 id="manage-user-name" class="text-xl font-bold"></h3>
                        <p id="manage-user-email" class="text-gray-500"></p>
                    </div>
                    <div class="bg-gray-100 p-4 rounded-xl">
                        <h4 class="font-semibold mb-3 text-gray-700">Ações Administrativas</h4>
                        <div class="space-y-2">
                           <div class="flex items-center gap-2">
                                <input type="number" id="manage-user-suspension" class="w-full border border-gray-300 rounded-lg p-2" placeholder="Dias de suspensão">
                                <button onclick="suspendUser()" class="bg-yellow-500 text-white font-bold py-2 px-4 rounded-lg">Suspender</button>
                           </div>
                           <button id="remove-suspension-btn" onclick="removeSuspension()" class="w-full bg-green-200 text-green-800 font-bold py-2 rounded-lg hidden">Remover Suspensão</button>
                            <button onclick="forcePasswordReset()" class="w-full bg-blue-100 text-blue-700 font-bold py-2 rounded-lg">Forçar Redefinição de Senha</button>
                            <button onclick="deleteUser()" class="w-full bg-red-100 text-red-700 font-bold py-2 rounded-lg">Excluir Usuário</button>
                        </div>
                    </div>
                </main>
            </div>
        </div>

        <!-- ===================================================================== -->
        <!-- BOTTOM NAVIGATION -->
        <!-- ===================================================================== -->
        <nav id="bottom-navigation" class="hidden fixed bottom-0 left-0 right-0 h-20 bg-white border-t border-gray-200 flex justify-center items-center bottom-nav">
             <div class="flex justify-around w-full max-w-md">
                <button onclick="navigate('home')" class="bottom-nav-item active flex flex-col items-center justify-center text-gray-500"><i class="fas fa-home text-2xl"></i><span class="text-xs mt-1">Início</span></button>
                <button onclick="navigate('request')" class="bottom-nav-item flex flex-col items-center justify-center text-gray-500"><i class="fas fa-plus-circle text-2xl"></i><span class="text-xs mt-1">Solicitar</span></button>
                <button onclick="navigate('admin')" class="bottom-nav-item flex flex-col items-center justify-center text-gray-500 hidden"><i class="fas fa-user-shield text-2xl"></i><span class="text-xs mt-1">Admin</span></button>
                <button onclick="navigate('history')" class="bottom-nav-item flex flex-col items-center justify-center text-gray-500"><i class="fas fa-exchange-alt text-2xl"></i><span class="text-xs mt-1">Empréstimos</span></button>
                <button onclick="navigate('profile')" class="bottom-nav-item flex flex-col items-center justify-center text-gray-500"><i class="fas fa-user-circle text-2xl"></i><span class="text-xs mt-1">Perfil</span></button>
            </div>
        </nav>
    </div>
    
    <!-- ===================================================================== -->
    <!-- MODALS & TOASTS -->
    <!-- ===================================================================== -->
    <div id="toast-notification" class="toast fixed top-0 left-1/2 -translate-x-1/2 max-w-sm w-full p-4 rounded-lg shadow-lg flex items-center z-50 text-white">
        <i id="toast-icon" class="fas mr-3"></i>
        <span id="toast-message"></span>
    </div>

    <div id="confirmation-modal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
        <div class="bg-white rounded-lg shadow-xl p-6 w-full max-w-sm text-center">
            <h3 id="modal-title" class="text-xl font-bold mb-2"></h3>
            <p id="modal-body" class="text-gray-600 mb-6"></p>
            <div id="modal-content-extra"></div>
            <div id="modal-buttons" class="flex justify-center gap-4">
                <button id="modal-cancel" class="px-6 py-2 bg-gray-200 rounded-lg font-semibold">Cancelar</button>
                <button id="modal-confirm" class="px-6 py-2 bg-green-800 text-white rounded-lg font-semibold">Confirmar</button>
            </div>
        </div>
    </div>
    
    <div id="wishlist-modal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-sm">
            <div class="flex justify-between items-center p-4 border-b">
                 <h3 class="text-xl font-bold">Lista de Desejos</h3>
                 <button onclick="hideWishlistModal()" class="text-gray-500 hover:text-gray-800">&times;</button>
            </div>
            <div id="wishlist-items" class="p-4 space-y-3 max-h-80 overflow-y-auto">
                <!-- Wishlist items will be injected here -->
            </div>
        </div>
    </div>


    <script type="module">
        // ========================== GLOBAL STATE & MOCK DATA ==========================
        let allMaterials = [
            { id: 'mat1', name: "Projetor Dell 2400MP", category: "Audiovisual", available: 3, total: 5, icon: "fa-video" },
            { id: 'mat2', name: "Notebook Dell Vostro", category: "Informática", available: 5, total: 8, icon: "fa-laptop" },
            { id: 'mat3', name: "Kit de Robótica Arduino", category: "Engenharia", available: 10, total: 10, icon: "fa-microchip" },
            { id: 'mat4', name: "Caixa de Som Amplificada", category: "Audiovisual", available: 0, total: 2, icon: "fa-volume-up" },
            { id: 'mat5', name: "Osciloscópio Digital", category: "Engenharia", available: 4, total: 4, icon: "fa-wave-square" },
            { id: 'mat6', name: "Câmera DSLR Canon T8i", category: "Comunicação", available: 0, total: 3, icon: "fa-camera-retro" },
            { id: 'mat7', name: "Impressora 3D Creality", category: "Engenharia", available: 2, total: 2, icon: "fa-cube" },
            { id: 'mat8', name: "Drone DJI Mini 2", category: "Comunicação", available: 3, total: 3, icon: "fa-helicopter" },
            { id: 'mat9', name: "Mesa Digitalizadora Wacom", category: "Design", available: 5, total: 5, icon: "fa-tablet-alt" },
            { id: 'mat10', name: "Kit de Iluminação Softbox", category: "Audiovisual", available: 4, total: 4, icon: "fa-lightbulb" },
            { id: 'mat11', name: "Gravador de Áudio Zoom H4n", category: "Audiovisual", available: 6, total: 6, icon: "fa-microphone" },
        ];
        let allLoans = []; 
        let allUsers = []; 
        let currentUserData = null; 
        let wishlist = [];

        const loanChartData = {
            '6M': { labels: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun'], data: [3, 2, 5, 4, 1, 2] },
            '1Y': { labels: ['Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez', 'Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun'], data: [4, 5, 3, 6, 7, 5, 3, 2, 5, 4, 1, 2] }
        };
        
        // ========================== APPLICATION LOGIC ==========================
        
        function setupMockDataForUser(email) {
            wishlist = [];

            currentUserData = {
                id: 'mockUser' + Date.now(),
                name: email.split('@')[0],
                email: email,
                matricula: '2025' + Math.floor(Math.random() * 100000),
                status: 'Regular',
                suspensionEndDate: null,
                isAdmin: email.toLowerCase().includes('admin'),
                avatarUrl: null
            };

            allUsers = [
                currentUserData,
                { id: 'joao123', name: 'João Silva', email: 'joao.silva@ufersa.edu.br', matricula: '202398765', status: 'Suspenso', suspensionEndDate: getFutureDate(10), isAdmin: false}
            ];
            
            allLoans = [
                 { id: 'loan1', userId: 'aluno123', itemId: 'mat1', name: "Projetor Dell 2400MP", status: 'Aprovado', requestDate: new Date(2025, 4, 15), returnDate: new Date(2025, 4, 25) },
                 { id: 'loan2', userId: 'aluno123', itemId: 'mat3', name: "Kit de Robótica Arduino", status: 'Em Análise', requestDate: new Date(2025, 5, 10) },
                 { id: 'loan3', userId: 'joao123', itemId: 'mat2', name: "Notebook Dell Vostro", status: 'Em Análise', requestDate: new Date(2025, 5, 11)},
                 { id: 'loan4', userId: 'aluno123', itemId: 'mat4', name: "Caixa de Som Amplificada", status: 'Aprovado', requestDate: new Date(2025, 5, 1), returnDate: new Date(2025, 5, 20) },
                 { id: 'loan5', userId: 'aluno123', itemId: 'mat6', name: "Câmera DSLR Canon T8i", status: 'Aprovado', requestDate: new Date(2025, 5, 5), returnDate: new Date(2025, 5, 22) }
            ];
        }

        function initializeAppUI() {
             document.querySelectorAll('.auth-view').forEach(v => v.classList.add('hidden'));
             document.getElementById('main-app').classList.remove('hidden');
             document.getElementById('bottom-navigation').classList.remove('hidden');

            updateUserProfileUI();
            updateAdminNavVisibility();
            populateDashboard();
            populateHistoryTabs();
            populateMaterials();
            updateWishlistCount();
            if (currentUserData.isAdmin) {
                populateAdminPanel();
            }
            navigate('home');
            renderLoanChart();
        }

        // --- UI Screens ---
        function showScreen(screenId) {
            document.querySelectorAll('.auth-view').forEach(div => div.classList.add('hidden'));
            const screen = document.getElementById(screenId);
            if(screen) screen.classList.remove('hidden');
        }
        window.showLogin = () => showScreen('login-screen');
        window.showSignUp = () => showScreen('signup-screen');
        window.showRecovery = () => showScreen('recovery-screen');

        // --- AUTH FUNCTIONS (MOCKED for fast entry) ---
        window.handleLogin = () => {
            const email = document.getElementById('login-email').value;
            if (!email) {
                showToast('Por favor, insira um email para continuar.', 'error');
                return;
            }
            
            const btn = document.querySelector('#login-screen button');
            btn.disabled = true;
            btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Entrando...';

            setTimeout(() => {
                console.log(`Bypass login for: ${email}`);
                setupMockDataForUser(email);
                initializeAppUI();
                btn.disabled = false;
                btn.textContent = 'Entrar';
            }, 500);
        };
        
        window.logout = () => {
            location.reload();
        };

        // --- UI POPULATION ---
        function populateDashboard() {
            if (!currentUserData) return;
            const userLoans = allLoans.filter(loan => loan.userId === currentUserData.id);
            const activeLoans = userLoans.filter(item => item.status === 'Aprovado');
            const pendingLoans = userLoans.filter(item => item.status === 'Em Análise');
            
            const quickPanel = document.getElementById('quick-panel');
            if (quickPanel) {
                quickPanel.innerHTML = `
                <button onclick="navigateToHistoryTab('active')" class="quick-panel-card bg-blue-100 p-4 rounded-xl text-center">
                    <div class="flex items-center justify-center text-blue-800"><i class="fas fa-box-open text-2xl mr-3"></i><p class="text-3xl font-bold">${activeLoans.length}</p></div>
                    <p class="text-sm text-blue-700 mt-1">Empréstimos Atuais</p>
                </button>
                <button onclick="navigateToHistoryTab('active')" class="quick-panel-card bg-yellow-100 p-4 rounded-xl text-center">
                    <div class="flex items-center justify-center text-yellow-800"><i class="fas fa-clock text-2xl mr-3"></i><p class="text-3xl font-bold">${pendingLoans.length}</p></div>
                    <p class="text-sm text-yellow-700 mt-1">Em Análise</p>
                </button>`;
            }
            const availableTodayCarousel = document.getElementById('available-today-carousel');
            if(availableTodayCarousel) {
                const available = allMaterials.filter(m => m.available > 0).slice(0, 7);
                availableTodayCarousel.innerHTML = available.length > 0 ? available.map(material => `
                    <div class="material-carousel-card bg-white p-3 rounded-xl shadow-md flex flex-col items-center gap-2 text-center">
                        <div class="w-16 h-16 bg-gray-100 rounded-lg flex items-center justify-center"><i class="fas ${material.icon || 'fa-box'} text-3xl text-gray-500"></i></div>
                        <h5 class="font-bold text-sm leading-tight">${material.name}</h4>
                        <button onclick="requestMaterial('${material.id}')" class="w-full bg-green-100 text-green-800 text-xs font-bold py-1 px-2 rounded-md hover:bg-green-200">Solicitar</button>
                    </div>
                `).join('') : `<p class="text-center text-gray-500 w-full">Nenhum material disponível hoje.</p>`;
            }
        }

        function populateMaterials() {
            const materialList = document.getElementById('material-list');
            const categories = [...new Set(allMaterials.map(m => m.category))];
            const categoryFilters = document.getElementById('category-filters');
            const unavailableList = document.getElementById('unavailable-list');

            if(categoryFilters){
                categoryFilters.innerHTML = `<button onclick="filterByCategory('all')" class="category-filter-btn active text-sm font-semibold py-1 px-3 rounded-full bg-gray-200">Todos</button>` + 
                categories.map(cat => `<button onclick="filterByCategory('${cat}')" class="category-filter-btn text-sm font-semibold py-1 px-3 rounded-full bg-gray-200">${cat}</button>`).join('');
            }
            
            if(materialList) {
                 materialList.innerHTML = allMaterials.map(material => {
                     const isInWishlist = wishlist.includes(material.id);
                     const unavailableCount = material.total - material.available;
                     return `
                     <div class="material-card bg-white p-3 rounded-xl shadow-md flex items-center gap-4" data-category="${material.category}" data-name="${material.name.toLowerCase()}">
                         <div class="w-16 h-16 bg-gray-100 rounded-lg flex items-center justify-center"><i class="fas ${material.icon || 'fa-box'} text-3xl text-gray-500"></i></div>
                         <div class="flex-grow">
                             <h4 class="font-bold text-md">${material.name}</h4>
                             <p class="text-sm text-gray-500">${material.category}</p>
                             <div class="text-sm mt-1">
                                 <span class="font-semibold text-green-700">${material.available} disponíveis</span>
                                 <span class="text-gray-400 mx-1">|</span>
                                 <span class="font-semibold text-red-700">${unavailableCount} emprestados</span>
                             </div>
                         </div>
                          <div class="flex flex-col gap-2">
                            <button ${material.available === 0 ? 'disabled' : ''} onclick="showRequestDetail('${material.id}')" class="bg-green-700 text-white font-bold text-sm px-4 py-2 rounded-lg hover:bg-green-800 disabled:bg-gray-400 disabled:cursor-not-allowed btn-action">Solicitar</button>
                            <button onclick="toggleWishlist('${material.id}', this)" class="${isInWishlist ? 'text-red-500' : 'text-gray-400'} hover:text-red-500"><i class="fas fa-heart"></i></button>
                          </div>
                     </div>`
                 }).join('');
            }
            if (unavailableList) {
                const unavailable = allMaterials.filter(m => m.available === 0);
                let content = '';
                unavailable.forEach(material => {
                    const earliestReturnLoan = allLoans
                        .filter(loan => loan.itemId === material.id && loan.status === 'Aprovado' && loan.returnDate)
                        .sort((a, b) => a.returnDate - b.returnDate)[0];

                    if (earliestReturnLoan) {
                        content += `
                            <div class="material-card bg-gray-100 p-3 rounded-xl shadow-sm flex items-center gap-4 opacity-70">
                                <div class="w-16 h-16 bg-gray-200 rounded-lg flex items-center justify-center"><i class="fas ${material.icon || 'fa-box'} text-3xl text-gray-400"></i></div>
                                <div class="flex-grow">
                                    <h4 class="font-bold text-md">${material.name}</h4>
                                    <p class="text-sm text-gray-500">Indisponível</p>
                                    <p class="text-sm font-semibold text-blue-600">Próxima devolução em: ${earliestReturnLoan.returnDate.toLocaleDateString('pt-BR')}</p>
                                </div>
                                <button onclick="toggleWishlist('${material.id}', this)" class="text-gray-400 hover:text-red-500"><i class="fas fa-heart text-2xl"></i></button>
                            </div>
                        `;
                    }
                });
                unavailableList.innerHTML = content || `<div class="text-center p-4 bg-gray-50 rounded-xl"><p class="text-gray-500">Nenhum item com previsão de devolução.</p></div>`;
            }
        }

        function populateHistoryTabs() {
            if (!currentUserData) return;
            const userLoans = allLoans.filter(loan => loan.userId === currentUserData.id);
            const activeList = document.getElementById('history-tab-active');
            const pastList = document.getElementById('history-tab-past');
            
            const activeItems = userLoans.filter(item => item.status === 'Em Análise' || item.status === 'Aprovado');
            const pastItems = userLoans.filter(item => item.status === 'Devolvido' || item.status === 'Negado');
            
            const renderItem = (item) => {
                const statusMap = {
                    'Em Análise': { icon: 'fa-clock', color: 'bg-yellow-100 text-yellow-800', iconColor: 'text-yellow-500' },
                    'Aprovado': { icon: 'fa-check-circle', color: 'bg-green-100 text-green-800', iconColor: 'text-green-500' },
                    'Devolvido': { icon: 'fa-history', color: 'bg-gray-100 text-gray-800', iconColor: 'text-gray-500' },
                    'Negado': { icon: 'fa-times-circle', color: 'bg-red-100 text-red-800', iconColor: 'text-red-500' }
                };
                const statusInfo = statusMap[item.status] || statusMap['Devolvido'];
                const requestDate = item.requestDate?.toLocaleDateString('pt-BR') || 'N/A';
                let details = `<p class="text-sm text-gray-500 mt-1">Data da solicitação: ${requestDate}</p>`;
                if(item.status === 'Aprovado') {
                     const returnDate = item.returnDate?.toLocaleDateString('pt-BR') || 'N/A';
                     details += `<p class="text-sm text-gray-500 mt-1">Data de devolução: <span class="font-semibold text-red-600">${returnDate}</span></p>`;
                }
                if (item.status === 'Negado' && item.rejectionReason) {
                    details += `<div class="mt-2 pt-2 border-t border-gray-200"><p class="text-xs text-gray-500 flex items-start gap-2"><i class="fas fa-info-circle mt-1 text-red-500"></i><span>Motivo: ${item.rejectionReason}</span></p></div>`;
                }

                return `<div class="bg-white p-4 rounded-xl shadow-sm flex items-start gap-4">
                            <div class="w-10 h-10 rounded-full ${statusInfo.color} flex-shrink-0 flex items-center justify-center"><i class="fas ${statusInfo.icon} ${statusInfo.iconColor}"></i></div>
                            <div class="flex-grow">
                                <p class="font-bold">${item.name}</p>
                                <span class="text-xs font-semibold ${statusInfo.color} px-2 py-1 rounded-full">${item.status}</span>
                                ${details}
                            </div>
                        </div>`;
            };

            if(activeList){
                 activeList.innerHTML = activeItems.length === 0 ? `<div class="text-center p-6 bg-gray-50 rounded-xl"><div class="text-5xl mb-2 text-gray-300"><i class="fas fa-box-open"></i></div><p class="text-gray-500">Nenhuma solicitação ativa.</p></div>` : activeItems.map(renderItem).join('');
            }
            
            if(pastList) {
                pastList.innerHTML = pastItems.length === 0 ? `<div class="text-center p-6 bg-gray-50 rounded-xl"><div class="text-5xl mb-2 text-gray-300"><i class="fas fa-history"></i></div><p class="text-gray-500">Seu histórico está vazio.</p></div>` : pastItems.map(renderItem).join('');
            }
        }

        function populateAdminPanel() {
            if (!currentUserData?.isAdmin) return;
            
            const requestsList = document.getElementById('admin-requests-list');
            if (requestsList) {
                const adminPending = allLoans.filter(item => item.status === 'Em Análise');
                requestsList.innerHTML = adminPending.length > 0 ? adminPending.map(req => {
                    const user = allUsers.find(u => u.id === req.userId);
                    return `<div class="bg-white p-4 rounded-xl shadow-sm" id="req-${req.id}"><p><span class="font-bold">${user?.name || 'Desconhecido'}</span> solicitou <span class="font-semibold">${req.name}</span></p><div class="flex gap-2 mt-3"><button onclick="handleApproval('${req.id}', true)" class="flex-1 bg-green-100 text-green-800 font-semibold py-2 rounded-lg">Aprovar</button><button onclick="handleApproval('${req.id}', false)" class="flex-1 bg-red-100 text-red-800 font-semibold py-2 rounded-lg">Rejeitar</button></div></div>`;
                }).join('') : `<div class="text-center p-4 bg-gray-100 rounded-xl"><p class="text-gray-500">Nenhuma solicitação pendente.</p></div>`;
            }

            const inventoryList = document.getElementById('admin-inventory-list');
            if (inventoryList) {
                inventoryList.innerHTML = allMaterials.map(mat => `<div class="bg-white p-4 rounded-xl shadow-sm flex justify-between items-center"><div><p class="font-bold">${mat.name}</p><p class="text-sm text-gray-600">Disponível: ${mat.available} de ${mat.total}</p></div><button onclick="manageItem('${mat.id}')" class="text-blue-600 font-semibold">Gerenciar</button></div>`).join('');
            }

            const punishmentSection = document.getElementById('admin-punishment-section');
            if (punishmentSection) {
                const activeLoans = allLoans.filter(i => i.status === 'Aprovado');
                punishmentSection.innerHTML = `<div class="bg-white p-4 rounded-xl shadow-sm">
                    <select id="loan-to-return" class="w-full border border-gray-300 rounded-lg p-2 mb-2">
                        <option value="">Selecione um empréstimo para devolver...</option>
                        ${activeLoans.map(loan => `<option value="${loan.id}">${loan.name} (${allUsers.find(u => u.id === loan.userId)?.name || 'Desconhecido'})</option>`).join('')}
                    </select>
                    <div class="flex items-center gap-4 mb-3"><label class="flex items-center"><input type="checkbox" id="return-late" class="mr-2">Devolução Atrasada</label><label class="flex items-center"><input type="checkbox" id="return-damaged" class="mr-2">Material Danificado</label></div>
                    <input type="number" id="suspension-days" class="w-full border border-gray-300 rounded-lg p-2" placeholder="Dias de suspensão (opcional)">
                    <button onclick="registerReturn()" class="w-full mt-3 bg-blue-600 text-white font-bold py-2 rounded-lg">Registrar Devolução</button>
                </div>`;
            }

            const usersList = document.getElementById('admin-users-list');
            if (usersList) {
                usersList.innerHTML = allUsers.map(user => {
                    const suspensionDate = user.suspensionEndDate?.toLocaleDateString('pt-BR') || '';
                    return `<div class="bg-white p-4 rounded-xl shadow-sm flex justify-between items-center">
                        <div>
                            <p class="font-bold">${user.name}</p>
                            <p class="text-sm text-gray-600">${user.email}</p>
                            <p class="text-xs font-semibold ${user.status === 'Regular' ? 'text-green-600' : 'text-red-600'}">${user.status === 'Suspenso' ? `Suspenso até ${suspensionDate}` : 'Regular'}</p>
                        </div>
                        <button onclick="manageUser('${user.id}')" class="text-blue-600 font-semibold">Gerenciar</button>
                    </div>`;
                }).join('');
            }
        }


        function updateUserProfileUI() {
            if (!currentUserData) return;
            const initials = currentUserData.name.split(' ').map(n => n[0]).join('').substring(0, 2).toUpperCase();
            const avatarUrl = currentUserData.avatarUrl || `https://placehold.co/80x80/007A4D/FFFFFF?text=${initials}`;

            document.getElementById('home-username').textContent = `Olá, ${currentUserData.name.split(' ')[0]}!`;
            document.getElementById('profile-username').textContent = currentUserData.name;
            document.getElementById('profile-email').textContent = currentUserData.email;
            document.getElementById('profile-matricula').textContent = `Matrícula: ${currentUserData.matricula}`;
            document.getElementById('header-avatar').src = avatarUrl;
            document.getElementById('profile-avatar').src = avatarUrl;
            document.getElementById('edit-profile-avatar').src = avatarUrl;

            updateUserStatusBadge();
        }

        function updateUserStatusBadge() {
            if(!currentUserData) return;
            const badge = document.getElementById('user-status-badge');
            const user = allUsers.find(u => u.id === currentUserData.id);
            if (badge && user) {
                if (user.status === 'Regular') {
                    badge.className = 'px-3 py-1 text-sm font-semibold rounded-full bg-green-200 text-green-800';
                    badge.innerHTML = `<i class="fas fa-check-circle mr-1"></i> Regular`;
                } else {
                    const suspensionDate = user.suspensionEndDate?.toLocaleDateString('pt-BR') || '';
                    badge.className = 'px-3 py-1 text-sm font-semibold rounded-full bg-red-200 text-red-800';
                    badge.innerHTML = `<i class="fas fa-times-circle mr-1"></i> Suspenso até ${suspensionDate}`;
                }
            }
        }

        function updateAdminNavVisibility() {
            const adminNav = document.querySelector('button[onclick="navigate(\'admin\')"]');
            if (adminNav) {
                adminNav.classList.toggle('hidden', !currentUserData?.isAdmin);
            }
        }

        // --- ACTIONS ---
        window.requestMaterial = (materialId) => { 
            const user = allUsers.find(u => u.id === currentUserData.id);
            if (user.status === 'Suspenso') {
                 const suspensionDate = user.suspensionEndDate?.toLocaleDateString('pt-BR') || '';
                showToast(`Você está suspenso até ${suspensionDate}.`, 'error');
                return;
            }

            const material = allMaterials.find(m => m.id === materialId);
            showModal('Confirmar Solicitação', `Você deseja solicitar o empréstimo de: ${material.name}?`, () => {
                if (material && material.available > 0) {
                    material.available--;
                    const newRequest = { id: `loan-${Date.now()}`, userId: currentUserData.id, itemId: material.id, name: material.name, status: 'Em Análise', requestDate: new Date() };
                    allLoans.push(newRequest);
                    
                    hideModal();
                    showToast('Solicitação enviada para análise!', 'success');
                    populateMaterials();
                    navigate('history');
                } else {
                    hideModal();
                    showToast('Material indisponível no momento.', 'error');
                }
            });
        }
        
        window.handleApproval = (requestId, isApprove) => {
            const request = allLoans.find(req => req.id === requestId);
            if (!request) return;

            const title = isApprove ? 'Aprovar Solicitação?' : 'Rejeitar Solicitação?';
            let body = `Você tem certeza que deseja ${isApprove ? 'aprovar' : 'rejeitar'} a solicitação para "${request.name}"?`;
            let extraContent = !isApprove ? `<div class="mt-4"><textarea id="rejection-reason" class="w-full border border-gray-300 rounded-lg p-2" placeholder="Escreva o motivo da rejeição..."></textarea></div>` : '';

            showModal(title, body, () => {
                if (isApprove) {
                    request.status = 'Aprovado';
                    request.returnDate = getFutureDate(15);
                } else {
                    const reason = document.getElementById('rejection-reason').value;
                    if (!reason) { showToast('Por favor, informe o motivo da rejeição.', 'error'); return; }
                    request.status = 'Negado';
                    request.rejectionReason = reason;
                    const material = allMaterials.find(m => m.id === request.itemId);
                    if (material) material.available++;
                }
                hideModal();
                showToast(`Solicitação ${isApprove ? 'aprovada' : 'rejeitada'} com sucesso!`, 'success');
                populateAdminPanel();
            }, extraContent, true, isApprove ? 'Aprovar' : 'Rejeitar');
        }

        window.registerReturn = () => {
            const loanId = document.getElementById('loan-to-return').value;
            if (!loanId) { showToast('Selecione um empréstimo para registrar a devolução.', 'error'); return; }

            const isLate = document.getElementById('return-late').checked;
            const isDamaged = document.getElementById('return-damaged').checked;
            const suspensionDays = document.getElementById('suspension-days').value;

            const loan = allLoans.find(item => item.id === loanId);
            if (loan) {
                const user = allUsers.find(u => u.id === loan.userId);
                if ((isLate || isDamaged) && suspensionDays > 0 && user) {
                    user.status = 'Suspenso';
                    user.suspensionEndDate = getFutureDate(suspensionDays);
                    showToast(`${user.name} suspenso por ${suspensionDays} dias.`, 'success');
                } else {
                    showToast('Devolução registrada com sucesso.', 'success');
                }
                
                loan.status = 'Devolvido';
                const material = allMaterials.find(m => m.id === loan.itemId);
                if (material) material.available++;
            }
            populateAdminPanel();
        }
        
        // --- UTILITY & HELPERS ---
        window.navigateToHistoryTab = (tab) => {
            navigate('history');
            switchHistoryTab(tab);
        }

        window.navigate = (viewName) => {
            document.querySelectorAll('.main-view').forEach(view => view.classList.add('hidden'));
            const targetView = document.getElementById(`${viewName}-view`);
            if (targetView) {
                targetView.classList.remove('hidden');
            }

            if (viewName === 'edit-profile' && currentUserData) {
                document.getElementById('edit-profile-name').value = currentUserData.name;
                document.getElementById('edit-profile-email').value = currentUserData.email;
                document.getElementById('edit-profile-id').value = currentUserData.matricula;
            }

            if (viewName === 'request') populateMaterials();
            if (viewName === 'admin' && currentUserData?.isAdmin) populateAdminPanel();
            if (viewName === 'history') populateHistoryTabs();


            const mainViews = ['home', 'request', 'history', 'admin', 'profile'];
            if(mainViews.includes(viewName)) {
                document.querySelectorAll('.bottom-nav-item').forEach(item => item.classList.remove('active'));
                const navItem = document.querySelector(`.bottom-nav-item[onclick="navigate('${viewName}')"]`);
                if(navItem) navItem.classList.add('active');
            }
        }
        
        window.filterByCategory = (category) => {
            document.querySelectorAll('.material-card').forEach(card => {
                card.style.display = (category === 'all' || card.dataset.category === category) ? 'flex' : 'none';
            });
            document.querySelectorAll('.category-filter-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelector(`.category-filter-btn[onclick="filterByCategory('${category}')"]`).classList.add('active');
        };
        
        window.filterMaterials = () => {
            const query = document.getElementById('search-material').value.toLowerCase();
            document.querySelectorAll('.material-card').forEach(card => {
                const name = card.dataset.name;
                card.style.display = name.includes(query) ? 'flex' : 'none';
            });
        };

        window.switchHistoryTab = (tab) => {
            document.getElementById('history-tab-active').classList.toggle('hidden', tab !== 'active');
            document.getElementById('history-tab-past').classList.toggle('hidden', tab !== 'past');
            
            document.querySelectorAll('#history-tabs .tab-button').forEach(button => {
                const isCurrentTab = button.getAttribute('onclick').includes(`'${tab}'`);
                button.classList.toggle('border-green-700', isCurrentTab); 
                button.classList.toggle('text-green-700', isCurrentTab);
                button.classList.toggle('border-transparent', !isCurrentTab); 
                button.classList.toggle('text-gray-500', !isCurrentTab);
            });
        };
        
        let loansChartInstance = null;
        function renderLoanChart() {
            if (loansChartInstance) { loansChartInstance.destroy(); }
            const ctx = document.getElementById('loansChart')?.getContext('2d');
            if (!ctx) return;
            const gradient = ctx.createLinearGradient(0, 0, 0, 300);
            gradient.addColorStop(0, 'rgba(0, 122, 77, 0.4)');
            gradient.addColorStop(1, 'rgba(0, 122, 77, 0)');
            loansChartInstance = new Chart(ctx, {
                type: 'line',
                data: { labels: [], datasets: [{ label: 'Nº de Empréstimos', data: [], backgroundColor: gradient, borderColor: '#007A4D', borderWidth: 3, pointBackgroundColor: '#007A4D', pointRadius: 5, pointHoverRadius: 7, tension: 0.4, fill: true }] },
                options: { responsive: true, maintainAspectRatio: false, scales: { y: { beginAtZero: true, grid: { drawBorder: false } }, x: { grid: { display: false } } }, plugins: { legend: { display: false }, tooltip: { backgroundColor: '#00384D', titleFont: { size: 14, weight: 'bold' }, bodyFont: { size: 12 }, padding: 10, cornerRadius: 8, displayColors: false } } }
            });
            updateLoanChart('6M');
        }
        
        window.updateLoanChart = (period) => {
            const data = loanChartData[period];
            if (loansChartInstance && data) {
                loansChartInstance.data.labels = data.labels;
                loansChartInstance.data.datasets[0].data = data.data;
                loansChartInstance.update();

                const stats = document.getElementById('chart-stats');
                const total = data.data.reduce((a, b) => a + b, 0);
                const avg = (total / data.data.length).toFixed(1);
                const max = Math.max(...data.data);
                const peakMonth = total > 0 ? data.labels[data.data.indexOf(max)] : 'N/A';
                stats.innerHTML = `
                    <div><p class="font-bold text-lg">${total}</p><p class="text-xs text-gray-500">Total</p></div>
                    <div><p class="font-bold text-lg">${peakMonth}</p><p class="text-xs text-gray-500">Mês de Pico</p></div>
                    <div><p class="font-bold text-lg">${avg}</p><p class="text-xs text-gray-500">Média Mensal</p></div>
                `;
            }

            document.querySelectorAll('.chart-filter-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelector(`.chart-filter-btn[onclick="updateLoanChart('${period}')"]`).classList.add('active');
        }

        window.showToast = (message, type = 'success') => {
            const toast = document.getElementById('toast-notification');
            const icon = document.getElementById('toast-icon');
            document.getElementById('toast-message').textContent = message;

            toast.className = 'toast fixed top-0 left-1/2 -translate-x-1/2 max-w-sm w-full p-4 rounded-lg shadow-lg flex items-center z-50 text-white';
            icon.className = 'fas mr-3';

            if (type === 'success') {
                toast.classList.add('bg-green-600');
                icon.classList.add('fa-check-circle');
            } else if (type === 'error'){
                toast.classList.add('bg-red-600');
                icon.classList.add('fa-exclamation-triangle');
            } else {
                toast.classList.add('bg-blue-500');
                icon.classList.add('fa-info-circle');
            }

            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }
        
        window.togglePasswordVisibility = (inputId) => {
            const input = document.getElementById(inputId);
            const icon = input.nextElementSibling.querySelector('i');
            if (input.type === 'password') {
                input.type = 'text';
                icon.classList.replace('fa-eye', 'fa-eye-slash');
            } else {
                input.type = 'password';
                icon.classList.replace('fa-eye-slash', 'fa-eye');
            }
        }
        
        window.checkPasswordStrength = (password) => {
             let strength = 0;
             if (password.length >= 8) strength++;
             if (password.match(/[a-z]/)) strength++;
             if (password.match(/[A-Z]/)) strength++;
             if (password.match(/[0-9]/)) strength++;
             if (password.match(/[^a-zA-Z0-9]/)) strength++;

             const meter = document.getElementById('password-strength-meter');
             const bars = meter.querySelectorAll('div');
             const text = document.getElementById('password-strength-text');

             let colorClass = '';
             let strengthText = '';
             let textColorClass = 'text-gray-500';

             if (password.length > 0) {
                 switch (strength) {
                     case 1:
                     case 2:
                         colorClass = 'bg-red-500';
                         textColorClass = 'text-red-500';
                         strengthText = 'Fraca';
                         break;
                     case 3:
                     case 4:
                         colorClass = 'bg-yellow-500';
                         textColorClass = 'text-yellow-500';
                         strengthText = 'Média';
                         break;
                     case 5:
                         colorClass = 'bg-green-500';
                         textColorClass = 'text-green-500';
                         strengthText = 'Forte';
                         break;
                     default:
                         colorClass = 'bg-red-500';
                         textColorClass = 'text-red-500';
                         strengthText = 'Muito Fraca';
                 }
             }
             
             bars.forEach((bar, index) => {
                 bar.className = 'h-1 rounded-full flex-1 transition-colors duration-300';
                 if (index < strength) {
                     bar.classList.add(colorClass);
                 } else {
                     bar.classList.add('bg-gray-200');
                 }
             });

             if (text) {
                 text.textContent = strengthText;
                 text.className = `text-xs text-right mt-1 transition-colors duration-300 ${textColorClass}`;
             }
        }
        
        function getFutureDate(days) {
            const futureDate = new Date();
            futureDate.setDate(futureDate.getDate() + parseInt(days));
            return futureDate;
        }

        // --- MODALS ---
        window.showModal = (title, body, onConfirm, extraContent = '', showCancel = true, confirmText = 'Confirmar') => {
             document.getElementById('modal-title').innerText = title;
             document.getElementById('modal-body').innerText = body;
             document.getElementById('modal-content-extra').innerHTML = extraContent;
             const confirmBtn = document.getElementById('modal-confirm');
             const cancelBtn = document.getElementById('modal-cancel');
             confirmBtn.innerText = confirmText;
             confirmBtn.onclick = onConfirm;
             cancelBtn.style.display = showCancel ? 'block' : 'none';
             cancelBtn.onclick = hideModal;
             document.getElementById('confirmation-modal').classList.remove('hidden');
        }
        window.hideModal = () => { document.getElementById('confirmation-modal').classList.add('hidden'); }
        
        window.showShareModal = () => {
             const shareText = encodeURIComponent("Confira o SIGMA, o app de gestão de materiais da UFERSA!");
             const shareLink = "https://ufersa.edu.br/sigma-app";
             const extra = `
                <div class="my-4 space-y-3">
                    <a href="https://api.whatsapp.com/send?text=${shareText}%20${shareLink}" target="_blank" class="block w-full text-center bg-green-500 text-white font-bold py-3 px-4 rounded-xl hover:bg-green-600"><i class="fab fa-whatsapp mr-2"></i>WhatsApp</a>
                    <a href="https://t.me/share/url?url=${shareLink}&text=${shareText}" target="_blank" class="block w-full text-center bg-blue-500 text-white font-bold py-3 px-4 rounded-xl hover:bg-blue-600"><i class="fab fa-telegram-plane mr-2"></i>Telegram</a>
                    <div class="relative"><input type="text" readonly value="${shareLink}" id="share-link-input" class="w-full text-center bg-gray-100 p-2 rounded-md border"><button onclick="copyShareLink()" class="absolute right-2 top-1/2 -translate-y-1/2 text-gray-500"><i class="fas fa-copy"></i></button></div>
                </div>`;
             showModal('Compartilhar App', 'Compartilhe o link do SIGMA com seus colegas!', () => hideModal(), extra, true, 'Fechar');
        }

        window.copyShareLink = () => {
             const linkInput = document.getElementById('share-link-input');
             linkInput.select();
             document.execCommand('copy');
             showToast('Link copiado!', 'success');
        }

        window.triggerAvatarUpload = () => { document.getElementById('avatar-upload').click(); }

        window.previewAvatar = (event) => {
            const file = event.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (e) => {
                const dataUrl = e.target.result;
                document.getElementById('edit-profile-avatar').src = dataUrl;
                document.getElementById('profile-avatar').src = dataUrl;
                document.getElementById('header-avatar').src = dataUrl;
                currentUserData.avatarUrl = dataUrl;
                showToast('Foto de perfil alterada (apenas para visualização).', 'info');
            };
            reader.readAsDataURL(file);
        };
        
        window.updateWishlistCount = () => {
            const countElement = document.getElementById('wishlist-count');
            if (countElement) {
                countElement.textContent = wishlist.length;
                countElement.classList.toggle('hidden', wishlist.length === 0);
            }
        };

        window.toggleWishlist = (materialId, element) => {
            const index = wishlist.indexOf(materialId);
            if (index > -1) {
                wishlist.splice(index, 1);
                element.classList.remove('text-red-500');
                element.classList.add('text-gray-400');
                showToast('Item removido da lista de desejos.', 'info');
            } else {
                wishlist.push(materialId);
                element.classList.add('text-red-500');
                element.classList.remove('text-gray-400');
                showToast('Item adicionado à lista de desejos!', 'success');
            }
            updateWishlistCount();
        };

        window.showWishlistModal = () => {
            const modal = document.getElementById('wishlist-modal');
            const itemsContainer = document.getElementById('wishlist-items');
            if (wishlist.length === 0) {
                itemsContainer.innerHTML = `<p class="text-center text-gray-500 py-8">Sua lista de desejos está vazia.</p>`;
            } else {
                itemsContainer.innerHTML = wishlist.map(itemId => {
                    const material = allMaterials.find(m => m.id === itemId);
                    if (!material) return '';
                    return `
                        <div class="flex items-center justify-between p-2 rounded-lg hover:bg-gray-50">
                            <div class="flex items-center gap-3">
                                <i class="fas ${material.icon || 'fa-box'} text-xl text-gray-500"></i>
                                <span class="font-semibold">${material.name}</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <button onclick="requestMaterial('${material.id}')" class="text-green-600 hover:text-green-800 text-sm font-bold">Solicitar</button>
                                <button onclick="removeFromWishlist('${material.id}')" class="text-red-500 hover:text-red-700 font-bold">&times;</button>
                            </div>
                        </div>
                    `;
                }).join('');
            }
            modal.classList.remove('hidden');
        };

        window.hideWishlistModal = () => {
            document.getElementById('wishlist-modal').classList.add('hidden');
        };
        
        window.removeFromWishlist = (materialId) => {
            const buttonInList = document.querySelector(`.material-card button[onclick*="toggleWishlist('${materialId}')"]`);
            if (buttonInList) {
                toggleWishlist(materialId, buttonInList);
            }
            showWishlistModal(); // Re-render the modal content
        };


        // --- INITIAL LOAD ---
        document.addEventListener('DOMContentLoaded', () => {
            showLogin();
        });

        // --- GLOBAL FUNCTION ASSIGNMENTS ---
        Object.assign(window, {
            handleSignUp: () => showToast('Cadastro desativado no modo de demonstração.', 'info'),
            sendRecoveryLink: () => showToast('Recuperação de senha desativada no modo de demonstração.', 'info'),
            resetPassword: () => showToast('Recuperação de senha desativada no modo de demonstração.', 'info'),
            handleChangePassword: () => showToast('Alteração de senha desativada no modo de demonstração.', 'info'),
            saveProfileChanges: () => {
                const newName = document.getElementById('edit-profile-name').value;
                if(newName && currentUserData) {
                    currentUserData.name = newName;
                    updateUserProfileUI();
                    showToast('Nome alterado com sucesso!', 'success');
                    navigate('profile');
                } else {
                    showToast('O nome não pode estar vazio.', 'error');
                }
            },
            manageItem: (id) => showToast(`Gerenciamento para item ${id} não implementado.`, 'info'),
            
            manageUser: (userId) => {
                const user = allUsers.find(u => u.id === userId);
                if(user) {
                    document.getElementById('manage-user-id').value = user.id;
                    document.getElementById('manage-user-name').textContent = user.name;
                    document.getElementById('manage-user-email').textContent = user.email;
                    const removeSuspensionBtn = document.getElementById('remove-suspension-btn');
                    removeSuspensionBtn.classList.toggle('hidden', user.status !== 'Suspenso');
                    navigate('manage-user');
                }
            },
            suspendUser: () => {
                const userId = document.getElementById('manage-user-id').value;
                const user = allUsers.find(u => u.id === userId);
                const suspensionDays = document.getElementById('manage-user-suspension').value;
                if (!suspensionDays || suspensionDays <= 0) {
                    showToast('Por favor, insira um número válido de dias.', 'error');
                    return;
                }
                if (user) {
                    user.status = 'Suspenso';
                    user.suspensionEndDate = getFutureDate(suspensionDays);
                    showToast(`${user.name} foi suspenso por ${suspensionDays} dias.`, 'success');
                    populateAdminPanel();
                    navigate('admin');
                }
            },
            removeSuspension: () => {
                 const userId = document.getElementById('manage-user-id').value;
                 const user = allUsers.find(u => u.id === userId);
                 if (user) {
                    user.status = 'Regular';
                    user.suspensionEndDate = null;
                    showToast(`Suspensão de ${user.name} foi removida.`, 'success');
                    populateAdminPanel();
                    navigate('admin');
                 }
            },
            forcePasswordReset: () => {
                const userId = document.getElementById('manage-user-id').value;
                const user = allUsers.find(u => u.id === userId);
                if (user) showToast(`Email de redefinição enviado para ${user.email}. (Simulação)`, 'success');
            },
            deleteUser: () => {
                const userId = document.getElementById('manage-user-id').value;
                if (userId === currentUserData.id) {
                    showToast('Você não pode excluir sua própria conta.', 'error');
                    return;
                }
                const user = allUsers.find(u => u.id === userId);
                showModal('Excluir Usuário', `Atenção: esta ação é irreversível. Excluir ${user.name}?`, () => {
                    allUsers = allUsers.filter(u => u.id !== userId);
                    allLoans = allLoans.filter(l => l.userId !== userId);
                    hideModal();
                    showToast(`Usuário ${user.name} excluído.`, 'success');
                    populateAdminPanel();
                    navigate('admin');
                });
            }
        });

    </script>
</body>
</html>
