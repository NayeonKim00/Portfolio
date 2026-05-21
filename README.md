# Quant Finance Portfolio

금융공학, 리스크관리, 파생상품, 팀 프로젝트, 논문 복제 작업을 GitHub 업로드용으로 정리한 포트폴리오입니다.

## Projects

| Folder | Project | Contents |
| --- | --- | --- |
| [01-risk-management](01-risk-management) | Risk Management | Market risk, credit risk, VaR/CVaR, fixed income and credit risk materials |
| [02-derivatives](02-derivatives) | Derivatives | Monte Carlo simulation, hedge trading, American option/LSMC, convertible bond, volatility surface |
| [03-team-projects](03-team-projects) | Team Projects | Asset management reports, proposals, competition document |
| [04-paper-replication](04-paper-replication) | Paper Replication | Fama-French 1992 style empirical replication notebooks and datasets |

## Environment

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Notes

- `*.ipynb` files are intended to be viewed directly on GitHub or executed in Jupyter.
- Public upload 전에 참고문헌 PDF, 팀 프로젝트 문서, 공모전 문서의 공개 가능 여부를 확인하는 것을 권장합니다.
- `__pycache__`, notebook checkpoint, local virtual environment files are ignored through `.gitignore`.
- `monthly_panel_data.csv`는 GitHub 100MB 제한을 넘는 생성 산출물이어서 로컬 보관 폴더로 분리했습니다. 필요하면 `04-paper-replication`의 Fama-MacBeth notebook에서 다시 생성할 수 있습니다.
