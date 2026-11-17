# Money Tracker App di Google Cloud

Deployment aplikasi Money Tracker (frontend PHP CodeIgniter 3.1.10 dan backend Node.js) ke Google Cloud.

## Arsitektur
- Region: asia-southeast2
- Frontend: App Engine (service `frontend`, PHP 8.3)
- Backend: App Engine (service `backend`, Node.js 22)
- Database: Cloud SQL MySQL 5.7 (`money-tracker-db`, database `money_tracker`)
- Penyimpanan gambar: Cloud Storage bucket `submission-mgce-juanda-14703-images`

## URL
- Frontend: http://frontend.submission-mgce-juanda-14703.et.r.appspot.com
- Backend: https://backend-dot-submission-mgce-juanda-14703.et.r.appspot.com

## Catatan
- `serviceaccountkey.json` tidak disertakan. Buat key sendiri untuk service account `money-tracker-uploader` lalu simpan sebagai `backend/serviceaccountkey.json`.
- Cloud SQL memakai IP publik sesuai brief. Untuk produksi, batasi `authorized-networks`.
- Service `default` minimal dibuat hanya karena App Engine mewajibkannya.
