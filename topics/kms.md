<!-- TCP Facts, dataset of 2026-10-10. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-08 10:06 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-09. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-10: kms

- A KMS grant of the default EVS key evs/default to another tenant was rejected, while the same grant on a custom KMS key was accepted. (KB-2RBG, docs, checked 2026-09-25)
- The console offers RSAES_OAEP_SHA_256 as wrapping algorithm while the get-parameters-for-import API also lists RSAES_PKCS1_V1_5 and RSAES_OAEP_SHA_1. The downloaded wrapping key expires after 24 hours. (KB-4WN4, docs, checked 2026-09-25)
- A KMS grant on the default EVS key evs/default is refused, while the same grant on a user created KMS key is accepted. (KB-7M7Y, docs, checked 2026-09-25)
- Symmetric imported material can be deleted by hand or given an expiry time (when expiry is chosen the console default is 24 hours after import). KMS deletes expired material within 24 hours while the key and its metadata stay in status Pending import and data encrypted with it cannot be decrypted until the same material is imported again. (KB-C3TF, docs, checked 2026-09-25)
- In eu-de the KMS call POST /v1.0/{project_id}/kms/list-key-detail does not exist (HTTP 404 APIGW.0101). POST /v1.0/{project_id}/kms/list-keys with a limit in the body returns both the key ids and key_details, including creation_date in milliseconds, so it serves as the detailed listing. (KB-DMLV, live, checked 2026-10-05)
- A disabled key or a key pending deletion is not rotated. If such a key is enabled again after one rotation period has passed, KMS rotates it within 24 hours. (KB-FPPV, docs, checked 2026-09-25)
- The service description charges keys with imported material (BYOK) the same as symmetric, asymmetric and HMAC customer master keys. (KB-HUHI, contract, checked 2026-09-25)
- To bring your own material you create a custom key with key material source External (API field origin set to external). You then fetch a wrapping key and an import token, encrypt your material with the wrapping key and import it. (KB-JGGC, docs, checked 2026-09-25)
- Imported asymmetric material (RSA_2048, RSA_3072, RSA_4096, EC_P256 and EC_P384) is permanently valid. It cannot be deleted by hand or given an expiry time and is removed only by deleting the whole key. (KB-KUNZ, docs, checked 2026-09-25)
- Automatic rotation changes only the key material while key ID, alias, description and permissions stay. Data is not re-encrypted and KMS keeps all versions: it encrypts with the latest and decrypts with the version that encrypted the data. (KB-RJRS, docs, checked 2026-09-25)
- A key with imported material cannot be rotated. The key stays bound to its material, so after deletion or expiry only the same material can be imported again. (KB-RMY5, docs, checked 2026-09-25)
- Rotation needs an enabled key whose origin is KMS. Asymmetric keys can only be rotated manually while default keys and keys with imported material cannot be rotated. (KB-SWEF, docs, checked 2026-09-25)
- The platform supplies default customer master keys named evs/default and obs/default, so disk encryption and OBS default encryption work without creating a key first. Keys are listed with POST /v1.0/{project_id}/kms/list-keys filtered by key_state. (KB-UKFK, live, checked 2026-06-15)
- Keys whose material KMS generated differ from keys with imported material: their material cannot be deleted by hand or given an expiry time and the symmetric ones can be rotated. (KB-UTXY, docs, checked 2026-09-25)
- KMS rotates a custom symmetric key automatically once rotation is enabled for it. Rotation is off by default and the period is 30 to 365 days with 365 as default. (KB-W26T, docs, checked 2026-09-25)
- Material can be imported for every key spec KMS offers: AES_256, HMAC_256, HMAC_384, HMAC_512, RSA_2048, RSA_3072, RSA_4096, EC_P256 and EC_P384. (KB-WXCI, docs, checked 2026-09-25)
- A disabled custom key is still billable. The KMS user guide says it stops incurring charges if it is deleted. (KB-XC4T, docs, checked 2026-09-25)
- Rotation is managed with the POST calls enable-key-rotation, disable-key-rotation, update-key-rotation-interval and get-key-rotation-status under /v1.0/{project_id}/kms/. The status call returns key_rotation_enabled, rotation_interval, last_rotation_time and number_of_rotations. (KB-XE5C, docs, checked 2026-09-25)
- KMS cannot export a customer master key: its FAQ says keys can only be created and used in KMS and the API has no export call, only get-publickey for the public key of an asymmetric key. For imported material the docs tell you to keep your own backup so that it can be imported again after an accidental deletion. (KB-YJ57, docs, checked 2026-09-25)
- For manual rotation, the only kind for asymmetric keys, the user guide names two methods (a new key B that replaces key A or a modified key A) with an example that swaps in a new custom key on the OBS console. The KMS FAQ says keys with KMS-generated material cannot be updated. (KB-ZE73, docs, checked 2026-09-25)
- A KMS grant that gives another tenant access to an encrypted volume has to set grantee_principal_type to domain. (KB-ZFVZ, docs, checked 2026-09-25)
- The service description bills customer master keys per active key version. Each rotation, automatic or on demand, creates an additional version that is billed. (KB-ZMQL, contract, checked 2026-09-25)
