---
title: Uruchamianie programu Azure PowerShell w kontenerze platformy Docker
description: Dowiedz się, jak uruchomić program Azure PowerShell w kontenerze platformy Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018531"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Uruchamianie programu Azure PowerShell w kontenerze platformy Docker

Aby ułatwić uruchamianie programu Azure PowerShell w środowiskach przenośnych, firma Microsoft publikuje obrazy platformy Docker z wstępnie zainstalowanym programem Azure PowerShell. Te obrazy oferują gościa z systemem Linux i programem PowerShell Core lub gościa z systemem Windows i programem PowerShell Core lub PowerShell 5.

| Środowisko | Obraz platformy Docker |
|-------------|--------------|
| Program PowerShell w systemie Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Program PowerShell Core w systemie Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Program PowerShell Core w systemie Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Aby uruchomić dowolne z tych kontenerów, należy użyć polecenia `docker run -it $ImageName` w celu otworzenia interakcyjnego terminalu. Aby na przykład uruchomić kontener z programem PowerShell Core w systemie Linux, użyj polecenia:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Aby uruchomić kontener systemu Windows na platformie Docker, host musi mieć system operacyjny Windows, a platforma Docker musi być skonfigurowana do uruchamiania kontenerów systemu Windows. Aby dowiedzieć się więcej o przełączaniu między środowiskami Windows i Linux na platformie Docker, zobacz dokumentację platformy Docker: [Switch between Windows and Linux containers (Przełączanie między kontenerami systemu Windows i Linux)](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).

## <a name="use-a-powershell-core-container"></a>Używanie kontenera programu PowerShell Core

Kontenery programu PowerShell Core są udostępniane z preinstalowanym programem PowerShell Core w wersji 6 i modułem `AzureRM.NetCore`. Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Używanie kontenera systemu Windows z programem PowerShell

Kontener systemu Windows ma preinstalowany moduł `AzureRM`. Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
