# CodeIgniter-4-Toastr
The simplest Toastr you will every come accross

Believe it or not, you won't find anything simplier than this for CodeIniter 4
usage
```
        // Use this in your Controller
        session()->setFlashdata('success',  'Your Success Message goes here!');
        session()->setFlashdata('error',    'Your Error Message goes here!');
        session()->setFlashdata('info',     'Your Info Message goes here!');
        session()->setFlashdata('warning',  'Your Warning Message goes here!');
```
Just copy and paste the below below code into your footer file or your prefered location

```
      <script src="http://code.jquery.com/jquery-1.9.1.min.js"></script>
      <link href="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/css/toastr.css" rel="stylesheet" />
      <script src="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/js/toastr.js"></script>


      <?php $session = session() ?>

      <?php if($session->getFlashdata('success') != null): ?>
          <script type='text/javascript'>
              toastr.success('<?= $session->getFlashdata('success') ?>');
          </script>
      <?php elseif($session->getFlashdata('error') != null): ?>
          <script type='text/javascript'>
              toastr.success('<?= $session->getFlashdata('error') ?>');
          </script>
      <?php elseif($session->getFlashdata('info') != null): ?>
          <script type='text/javascript'>
              toastr.success('<?= $session->getFlashdata('info') ?>');
          </script>
      <?php elseif($session->getFlashdata('warning') != null): ?>
          <script type='text/javascript'>
              toastr.success('<?= $session->getFlashdata('warning') ?>');
          </script>
      <?php endif ?>
```
