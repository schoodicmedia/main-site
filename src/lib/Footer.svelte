<script>
	import { page } from '$app/stores';
    import Logo from "./Logo.svelte";
	import Wave from "./Wave.svelte";

    import SocialIcons from '@rodneylab/svelte-social-icons';

    const year = new Date().getFullYear();
</script>

<footer class="text-center z-50">
    {#if !$page.error}
        <div class="w-full h-8 lg:h-[6vw] bg-almond">
            <Wave class="text-croix" height="100%" />
        </div>
    {/if}
    <div class="bg-croix text-white h-screen short:h-auto lg:h-auto">
        <div class="flex flex-col lg:flex-row justify-center lg:items-start gap-10 md:gap-20 xl:gap-40 py-20 h-full">
            <section class="flex flex-col items-center lg:order-1 gap-1 lg:gap-4">
                <a href="/" class="navlink" aria-label="Back to top"><Logo variant="white" /></a>
                <div>
                    <p>Proudly built with ❤️ in Washington County</p>
                    <p>Copyright &copy; {year} Schoodic Media</p>
                </div>
                <div class="flex gap-2">
                    <a href="https://www.facebook.com/schoodicmedia"><SocialIcons network="facebook" bgColor="white" /></a>
                    <a href="https://www.linkedin.com/company/schoodic"><SocialIcons network="linkedin" bgColor="white" /></a>
                    <a href="https://www.github.com/schoodicmedia"><SocialIcons network="github" bgColor="white" /></a>
                </div>
            </section>
            <section class="flex flex-col items-center gap-1 lg:gap-4">
                <h3 class="text-xl font-bold">Services</h3>
                <nav aria-label="Footer">
                    <ul>
                        <li><a href="/full-stack">Full Stack Web Development</a></li>
                        <li><a href="/responsive-design">Responsive Web Design</a></li>
                        <li><a href="/digital-marketing">Digital Marketing</a></li>
                        <li><a href="/search-engine-optimization">Search Engine Optimization</a></li>
                        <li><a href="/managed-hosting">Managed Hosting</a></li>
                    </ul>
                </nav>
            </section>
            <section class="flex flex-col items-center gap-1 lg:gap-4 order-2">
                <h3 class="text-xl font-bold">Legal</h3>
                <ul>
                    <li><a href="/privacy-policy">Privacy Policy</a></li>
                    <li><a href="/terms-and-conditions">Terms and Conditions</a></li>
                </ul>
            </section>
        </div>
    </div>
</footer>