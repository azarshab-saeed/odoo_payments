# Odoo Payments — Alsatpardakht

Odoo payment-acquirer add-on for the Alsatpardakht gateway.

افزونهٔ درگاه پرداخت آل‌سات پرداخت برای اودو.

## Included module

`payment_alsatpardakht/` contains the payment integration, controllers, views, payment-provider data, frontend assets, and Persian translations.

The module manifest declares:

| Setting | Value |
| --- | --- |
| Module version | `1.0` |
| Odoo dependency | `payment` |
| Python dependencies | `urllib3`, `zeep`, `requests` |
| Declared module license | `LGPL-3` |

The manifest does not specify an Odoo major version. Compatibility with a particular Odoo release must be checked before installation.

## Installation outline

1. Prepare a development Odoo instance with the `payment` module available.
2. Install the declared Python dependencies in that instance's Python environment.
3. Place `payment_alsatpardakht` in a directory included in Odoo's `addons_path`.
4. Restart Odoo, refresh the Apps list, and locate the Alsatpardakht payment module.
5. Configure the gateway through the payment settings exposed by the module.

Review the module's models and views for the required merchant settings. Keep real merchant credentials outside source control.

## Repository guide

| Path | Purpose |
| --- | --- |
| `payment_alsatpardakht/__manifest__.py` | Metadata, dependencies, data files, and hooks. |
| `payment_alsatpardakht/models/` | Payment integration models. |
| `payment_alsatpardakht/controllers/` | HTTP controller implementation. |
| `payment_alsatpardakht/views/` | Payment forms and templates. |
| `payment_alsatpardakht/data/` | Payment acquirer and icon records. |
| `payment_alsatpardakht/i18n/fa_IR.po` | Persian translations. |

## Validation status

Installation and payment flows have not been executed as part of this documentation update. Before deployment, verify the target Odoo version, module installation, gateway configuration, payment callbacks, and transaction-state handling in a test environment.

The manifest currently lists frontend assets under `payment_test/static/src/js/**/*`, while this repository stores JavaScript under `payment_alsatpardakht/static/src/js/`. Review this mismatch against the target Odoo version.

## Attribution and license

The manifest credits Alsatpardakht and declares LGPL-3. Preserve existing attribution and review the applicable licensing terms before redistribution.

