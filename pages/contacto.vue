<template>
<div>
    <Header/>
    <br>
    <div class = "container">
    <section class="mb-4 contact">

    <!--Section heading-->
    <h2 class="h1-responsive font-weight-bold text-center my-4">Contactanos</h2>
    <!--Section description-->
    <p class="text-center w-responsive mx-auto mb-5">¿Tiene usted alguna pregunta? No dude en contactarnos directamente. Nuestro equipo se pondrá en contacto contigo en
        cuestión de horas para ayudarte.</p>

    <div class="row">

        <!--Grid column-->
        <div class="col-md-9 mb-md-0 mb-5">
            <form id="contact-form" name="contact-form"  >

                <!--Grid row-->
                <div class="row">

                    <!--Grid column-->
                    <div class="col-md-6">
                        <div class="md-form mb-0">
                            <input type="text" id="name" name="name" class="form-control">
                            <label for="name" class="">Nombres </label>
                        </div>
                    </div>

                    <div class="col-md-6">
                        <div class="md-form mb-0">
                            <input type="email" id="email" name="email" class="form-control">
                            <label for="email" class="">Correo electronico</label>
                        </div>
                    </div>

                </div>
                <div class="row">
                    <div class="col-md-12">
                        <div class="md-form mb-0">
                            <input type="text" id="subject" name="subject" class="form-control">
                            <label for="subject" class="">Asunto</label>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-md-12">

                        <div class="md-form">
                            <textarea type="text" id="message" name="message" rows="2" class="form-control md-textarea"></textarea>
                            <label for="message">Mensaje</label>
                        </div>

                    </div>
                </div>

            </form>

            <div class="text-center text-md-right">
                <a class="btn btn-primary">Enviar</a>
            </div>
            <div class="status"></div>
        </div>
        <div class="col-md-3 text-center">
            <ul class="list-unstyled mb-0">
                <li><i class="fas fa-map-marker-alt fa-2x"></i>
                    <p>Lima, Perú</p>
                </li>

                <li><i class="fas fa-phone mt-4 fa-2x"></i>
                    <p>+ 01 485296</p>
                </li>

                <li><i class="fas fa-envelope mt-4 fa-2x"></i>
                    <p>contact@moover.com</p>
                </li>
            </ul>
        </div>

    </div>

</section>
    </div>
    
</div>

</template>
<style>
.contact{
    background:slategrey ;
    padding: 10pt;
    border-radius: 10pt;
}

</style>