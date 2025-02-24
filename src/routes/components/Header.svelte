<script>


let isMenuOpen = false;

function toggleMenu() {
  isMenuOpen = !isMenuOpen;
}

function closeMenu() {
  isMenuOpen = false;
}



</script>

<div class=" bg-[#0e1620] sticky top-0 z-50 flex  flex-col sm:flex-row justify-center w-full p-1">

    <div class="sm:hidden w-full flex justify-between bg-[rgb(26 10 59 / 20%)]  backdrop-blur-[6px]">

        <div class="flex items-center p-2 text-white">
                    <a href="/" class="text-lg text-blue-500 font-extrabold">TechConf 2025</a>
        </div>

        {#if !isMenuOpen}

    <button onclick={toggleMenu}  class=" m-1 w-[40px] h-[40px] rounded-[10px] p-2 bg-[rgb(26 10 59 / 20%)] shadow-lg backdrop-blur-[4px]   text-white cursor-pointer relative z-10   shadow-md hover:bg-white/30 hover:border-white/30 hover:shadow-white/30">
        <i class="fa-solid fa-bars text-blue-500"></i>
      </button>

      {:else}

      <button onclick={toggleMenu}  class=" m-1 w-[40px] h-[40px] rounded-[10px] p-2 bg-[rgb(26 10 59 / 20%)] shadow-lg backdrop-blur-[4px]   text-white cursor-pointer relative z-10   shadow-md hover:bg-white/30 hover:border-white/30 hover:shadow-white/30">
        <i class="fa-solid fa-xmark text-blue-500"></i>
      </button>

      {/if}

  </div>

    <ul class="{isMenuOpen? 'flex' : 'hidden'} list-none relative sm:flex flex-col sm:flex-row sm:p-1 sm:rounded-full items-center justify-center bg-[rgb(26 10 59 / 20%)]  sm:shadow-lg backdrop-blur-[10px] sm:backdrop-blur-[4px]  sm:border1 sm:border-white/30">
        <li class="logo mr-2">
            <a href="/">
            <h1 class="text-lg ms-2 text-blue-500 font-extrabold hidden sm:block">TechConf</h1>
            </a>
        </li>
        <li>
            <a href="/schedule" class="tab px-5 py-2 text-xs text-white cursor-pointer relative z-10 mix-blend-difference uppercase hover:text-white hover:bg-white/10 hover:rounded-full hover:shadow-lg hover:border-white/10">
            Schedule
        </a>
        </li>
        <li>
            <a href="/speakers" class="tab px-5 py-2 text-xs text-white cursor-pointer relative z-10 mix-blend-difference uppercase hover:text-white hover:bg-white/10 hover:rounded-full hover:shadow-lg hover:border-white/10">
            Speakers
            </a>
        </li>
        <li>
            <a href="/sponsors" class="tab px-5 py-2 text-xs text-white cursor-pointer relative z-10 mix-blend-difference uppercase hover:text-white hover:bg-white/10 hover:rounded-full hover:shadow-lg hover:border-white/10">
            Sponsors
            </a>
        </li>
        <li >
            <a href="/contact" class="tab px-5 py-2 text-xs text-white cursor-pointer relative z-10 mix-blend-difference uppercase hover:text-white hover:bg-white/10 hover:rounded-full hover:shadow-lg hover:border-white/10">
            Contact
            </a>
        </li>
        <li >
            <a href="/about" class="tab px-5 py-2 text-xs text-white cursor-pointer relative z-10 mix-blend-difference uppercase hover:text-white hover:bg-white/10 hover:rounded-full hover:shadow-lg hover:border-white/10">
            About
            </a>
        </li>
        <li class=" hidden sm:block  md:block px-6 py-3 text-xs text-white cursor-pointer relative z-10 bg-white/10 rounded-full ml-2 flex justify-center items-center shadow-lg hover:bg-white/30 hover:border-white/30 hover:shadow-white/30">
            <div>Register</div>
        </li>
        <!-- <li class="profile bg-white/10 shadow-lg border border-white/10 rounded-full w-10 h-10 flex cursor-pointer"> -->
        <div class="cursor absolute h-7 rounded-full transition-all duration-300 ease-in-out opacity-0 bg-white/10 shadow-lg border border-white/10 z-0"></div>
    </ul>
</div>

<style>
    
.hamburger {
    width: 26px;
    height: 26px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    gap: 4px;
}

    .hamburger-top, .hamburger-middle, .hamburger-bottom {
    /* position: absolute; */
    width: 24px;
    height: 2px;
    /* top: 0; */
    /* left: 0; */
    background: #fff;
    /* transform: rotate(0); */
    transition: all 0.5s;
}
</style>