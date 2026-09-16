<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>SaaS SEO Analyzer Gratuito</title>
    <!-- Gerador de PDF -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <!-- Ícones -->
    <link href="https://cdn.jsdelivr.net/npm/remixicon@3.5.0/fonts/remixicon.css" rel="stylesheet">
    <style>
        * { box-sizing: border-box; }
        body { font-family: 'Segoe UI', sans-serif; background: #f8f9fa; margin: 0; padding: 20px; }
        
        .container { max-width: 1000px; margin: auto; background: white; padding: 30px; border-radius: 15px; box-shadow: 0 4px 20px rgba(0,0,0,0.1); }
        
        h1 { color: #2c3e50; text-align: center; border-bottom: 3px solid #3498db; padding-bottom: 15px; }
        h2, h3 { color: #34495e; margin-top: 25px; }
        
        .input-group { display: flex; gap: 10px; margin-bottom: 20px; flex-wrap: wrap; }
        input[type="text"] { flex: 1; min-width: 250px; padding: 12px; border: 2px solid #ddd; border-radius: 8px; font-size: 14px; }
        
        .btn-group { display: flex; gap: 10px; flex-wrap: wrap; }
        button { padding: 12px 24px; border: none; border-radius: 8px; cursor: pointer; font-weight: 600; transition: all 0.3s; display: flex; align-items: center; gap: 8px; }
        
        .btn-primary { background: #3498db; color: white; }
        .btn-primary:hover { background: #2980b9; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(52,152,219,0.3); }
        
        .btn-success { background: #27ae60; color: white; }
        .btn-success:hover { background: #229954; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(39,174,96,0.3); }
        
        .btn-warning { background: #f39c12; color: white; }
        .btn-warning:hover { background: #d68910; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(243,156,18,0.3); }
        
        .btn-danger { background: #e74c3c; color: white; }
        .btn-danger:hover { background: #c0392b; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(231,76,60,0.3); }
        
        /* Scores */
        .score-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 15px; margin: 25px 0; }
        .score-box { padding: 20px; border-radius: 10px; text-align: center; color: white; font-weight: bold; }
        .score-good { background: linear-gradient(135deg, #27ae60, #2ecc71); }
        .score-medium { background: linear-gradient(135deg, #f39c12, #f1c40f); }
        .score-poor { background: linear-gradient(135deg, #e74c3c, #c0392b); }
        
        /* Cards */
        .card { background: #f8f9fa; border-radius: 10px; padding: 20px; margin: 15px 0; border-left: 4px solid #ddd; }
        .card.info { border-left-color: #3498db; }
        .card.warning { border-left-color: #f39c12; }
        .card.success { border-left-color: #27ae60; }
        .card.danger { border-left-color: #e74c3c; }
        
        /* Loading */
        .loading-overlay { position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(255,255,255,0.9); display: flex; align-items: center; justify-content: center; z-index: 1000; }
        .spinner { width: 60px; height: 60px; border: 4px solid #f3f3f3; border-top: 4px solid #3498db; border-radius: 50%; animation: spin 1s linear infinite; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        
        /* Results */
        .seo-score { text-align: center; font-size: 72px; font-weight: bold; margin: 20px 0
