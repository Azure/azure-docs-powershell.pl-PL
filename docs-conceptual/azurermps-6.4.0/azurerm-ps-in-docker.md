---
title: Uruchamianie programu Azure PowerShell w kontenerze platformy Docker
description: Dowiedz się, jak uruchomić program Azure PowerShell w kontenerze platformy Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406363"
---
## <a name="run-azure-powershell-in-a-docker-container"></a>Uruchamianie programu Azure PowerShell w kontenerze platformy Docker

Jest dostępny zestaw obrazów platformy Docker wstępnie skonfigurowanych z programem Azure PowerShell. Dostępne są dwa typy kontenerów: kontenery z tradycyjnym programem PowerShell działającym w systemie Windows i kontenery z programem PowerShell Core działającym w systemie Windows lub Linux.

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