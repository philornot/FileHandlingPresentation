<script lang="ts">
    import { Transition } from '@animotion/core'
    </script>
    
    <div class="grid h-full place-content-center place-items-center">
      <div class="flex flex-col items-center text-center">
        <h1 class="text mb-24 text 
        font-bold tracking-tight">Praca z plikami w Pythonie</h1>
        <p class="text-xl text-gray-400">Poznaj wygodniejszy sposób otwierania plików!</p>
        <div class="mt-12 flex items-center gap-4 text text-gray-500">
          <span class="rounded-lg border border-gray-700 px-4 py-2">Spacja</span>
          <span>aby rozpocząć</span>
        </div>
      </div>
    </div>
    
    <style>
      .text {
        opacity: 0;
        animation: fadeIn 1s ease-out forwards;
      }
    
      @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
      }
    </style>