---
title: Rozpoczynanie pracy z programem Azure PowerShell
description: Rozpoczynanie pracy z programem Azure PowerShell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 68b2b50afdd2dc79bdbd8f8b203a7cd3664c4973
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409231"
---
# <a name="get-started-with-azure-powershell"></a>Rozpoczynanie pracy z programem Azure PowerShell

Program Azure PowerShell jest przeznaczony do zarządzania i administrowania zasobami platformy Azure z wiersza polecenia.
Za pomocą programu Azure PowerShell możesz tworzyć zautomatyzowane narzędzia korzystające z modelu usługi Azure Resource Manager. Wypróbuj go w przeglądarce przy użyciu [usługi Azure Cloud Shell](/azure/cloud-shell/overview) lub zainstaluj go na komputerze lokalnym.

W tym artykule przedstawiono podstawowe pojęcia związane z programem Azure PowerShell, które ułatwiają rozpoczęcie korzystania z niego.

## <a name="install-or-run-in-azure-cloud-shell"></a>Instalowanie lub uruchamianie w usłudze Azure Cloud Shell

Najprostszym sposobem rozpoczęcia pracy z programem Azure PowerShell jest wypróbowanie go w środowisku usługi Azure Cloud Shell. Aby rozpocząć pracę z usługą Cloud Shell, zobacz [Przewodnik Szybki start dotyczący programu PowerShell w usłudze Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell). Usługa Cloud Shell uruchamia program PowerShell w kontenerze systemu Linux, więc funkcje specyficzne dla systemu Windows są niedostępne.

Jeśli chcesz zainstalować program Azure PowerShell na komputerze lokalnym, wykonaj instrukcje podane w temacie [Instalowanie modułu Azure PowerShell](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Logowanie do platformy Azure

Zaloguj się interakcyjnie za pomocą polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Pomiń ten krok, jeśli korzystasz z usługi Cloud Shell. Sesja usługi Azure Cloud Shell jest już uwierzytelniona dla danego środowiska, subskrypcji i dzierżawy, w których uruchomiono sesję usługi Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych. W przypadku kont w chmurze regionalnej użyj parametru **Environment** , aby się zalogować. Uzyskaj nazwę środowiska dla swojego regionu, używając polecenia cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).
Aby na przykład zalogować się do platformy Azure w Chinach — 21Vianet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

W środowiskach Windows PowerShell 5.1 jest wyświetlane okno dialogowe logowania, w którym można podać nazwę użytkownika i hasło konta platformy Azure. W przypadku każdej innej wersji programu PowerShell uzyskasz token do użycia na stronie [microsoft.com/devicelogin](https://microsoft.com/devicelogin). Otwórz tę stronę w przeglądarce i wprowadź token, a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure i autoryzuj program Azure PowerShell.

Po zalogowaniu zobaczysz informacje wskazujące, która subskrypcja platformy Azure jest aktywna. Jeśli masz wiele subskrypcji platformy Azure w ramach konta i chcesz wybrać inną, pobierz dostępne subskrypcje przy użyciu polecenia [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), a następnie użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) z identyfikatorem subskrypcji. Aby uzyskać więcej informacji o zarządzaniu subskrypcjami platformy Azure w programie Azure PowerShell, zobacz [Use multiple Azure subscriptions (Używanie wielu subskrypcji platformy Azure)](manage-subscriptions-azureps.md).

Po zalogowaniu użyj poleceń cmdlet programu Azure PowerShell, aby uzyskiwać dostęp do zasobów w subskrypcji i zarządzać nimi. Aby dowiedzieć się więcej na temat procesu logowania i metod uwierzytelniania, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Znajdowanie poleceń

Polecenia cmdlet programu Azure PowerShell używają standardowej konwencji nazewnictwa dla programu PowerShell: `Verb-Noun`. Czasownik (verb) opisuje akcję (przykłady: `New`, `Get`, `Set`, `Remove`), a rzeczownik (noun) opisuje typ zasobu (przykłady: `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). Rzeczowniki w programie Azure PowerShell zawsze rozpoczynają się prefiksem `Az`. Aby uzyskać pełną listę standardowych czasowników, zobacz [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Zatwierdzone czasowniki dla poleceń programu PowerShell).

Znajomość dostępnych rzeczowników, czasowników i modułów programu Azure PowerShell ułatwia znajdowanie poleceń za pomocą polecenia cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Aby na przykład znaleźć wszystkie polecenia dotyczące maszyn wirtualnych i używające czasownika `Get`:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Aby ułatwić znajdowanie typowych poleceń, w poniższej tabeli podano typy zasobów, odpowiednie moduły programu Azure PowerShell i prefiksy rzeczowników do używania z poleceniem `Get-Command`:

|                              Typ zasobu                              |                   Moduł programu Azure PowerShell                    |    Prefiks rzeczownika     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [Grupa zasobów](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [Maszyny wirtualne](/azure/virtual-machines)                             | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [Konta magazynu](/azure/storage/common/storage-introduction)          | [Az.Storage](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [Usługa Key Vault](/azure/key-vault/key-vault-whatis)                          | [Az.KeyVault](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [Aplikacje internetowe](/azure/app-service)                                  | [Az.Websites](/powershell/module/az.websites)                | `AzWebApp`         |
| [Bazy danych SQL](/azure/sql-database)                                    | [Az.Sql](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

Aby uzyskać pełną listę modułów w programie Azure PowerShell, zobacz [listę modułów programu Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hostowaną w serwisie GitHub.

## <a name="telemetry"></a>Telemetria

Domyślnie program Azure PowerShell automatycznie zbiera dane telemetryczne. Firma Microsoft agreguje zebrane dane, aby wykrywać wzorce użycia i typowe problemy oraz usprawnić środowisko Azure PowerShell. Program Microsoft Azure PowerShell nie zbiera żadnych danych osobowych ani prywatnych. Aby wyłączyć zbieranie danych, musisz jawnie zrezygnować z wykonywania polecenia [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Nauka podstaw programu Azure PowerShell za pomocą samouczków i przewodników Szybki start

Aby rozpocząć pracę z programem Azure PowerShell, wypróbuj szczegółowy samouczek na temat konfigurowania maszyn wirtualnych i wykonywania dotyczących ich zapytań.

> [!div class="nextstepaction"]
> [Tworzenie maszyn wirtualnych przy użyciu programu Azure PowerShell](azureps-vm-tutorial.yml)

Dostępne są też przewodniki Szybki start dla programu Azure PowerShell dotyczące innych popularnych usług platformy Azure:

* [Tworzenie konta magazynu](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Transferowanie obiektów do i z usługi Azure Blob Storage](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Tworzenie i pobieranie wpisów tajnych w usłudze Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Tworzenie bazy danych Azure SQL Database i zapory](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Uruchamianie kontenera w usłudze Azure Container Instances](/azure/container-instances/container-instances-quickstart-powershell)
* [Tworzenie zestawu skalowania maszyn wirtualnych](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Tworzenie modułu równoważenia obciążenia w warstwie Standardowa](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Następne kroki

* [Logowanie się w programie Azure PowerShell](authenticate-azureps.md)
* [Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell](manage-subscriptions-azureps.md)
* [Tworzenie jednostek usługi przy użyciu programu Azure PowerShell](create-azure-service-principal-azureps.md)
* Uzyskiwanie pomocy od społeczności:
  * [Forum platformy Azure w witrynie MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
