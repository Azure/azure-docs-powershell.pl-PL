---
title: Używanie Azure PowerShell w platformie Docker
description: Jak używać preinstalowanych Azure PowerShell w obrazie platformy Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101882088"
---
# <a name="using-azure-powershell-in-docker"></a>Używanie Azure PowerShell w platformie Docker

Publikujemy obrazy platformy Docker z preinstalowanym Azure PowerShell. W tym artykule pokazano, jak rozpocząć korzystanie z Azure PowerShell w kontenerze platformy Docker.

## <a name="finding-available-images"></a>Znajdowanie dostępnych obrazów

Wydane obrazy wymagają platformy Docker 17,05 lub nowszej. Oczekuje się również, że można uruchomić platformę Docker bez `sudo` lub lokalnych praw administracyjnych. Zapoznaj się z oficjalnymi [instrukcjami][install] platformy Docker, aby poprawnie zainstalować program `docker` .

Najnowszy obraz kontenera zawiera najnowszą wersję programu PowerShell i najnowsze moduły Azure PowerShell obsługiwane przez AZ module.

Dla każdej nowej wersji AZ module zwalniamy obraz dla następujących systemów operacyjnych:

- Ubuntu 18,04 (wartość domyślna)
- Debian 9
- CentOs 7

Pełną listę dostępnych obrazów można znaleźć na naszej stronie [obrazu platformy Docker][az image] .

## <a name="using-azure-powershell-in-a-container"></a>Używanie Azure PowerShell w kontenerze

Poniższe kroki pokazują polecenia platformy Docker wymagane do pobrania obrazu i uruchomienia interaktywnej sesji programu PowerShell.

1. Pobierz najnowszą wersję obrazu platformy Azure-PowerShell.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Uruchom kontener Azure-PowerShell w trybie interaktywnym:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

W przypadku hostów platformy Docker systemu Windows należy włączyć udostępnianie plików platformy Docker, aby zezwolić na współużytkowanie dysków lokalnych w systemie Windows z kontenerami systemu Linux. Aby uzyskać więcej informacji, zobacz [wprowadzenie do Docker for Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Uruchamianie kontenera platformy Azure-PowerShell interaktywnie przy użyciu uwierzytelniania hosta

Jeśli masz już zainstalowaną Azure PowerShell w systemie Docker, być może masz buforowane poświadczenia platformy Azure. Tych poświadczeń można używać w sesji programu PowerShell działającej w kontenerze platformy Docker.

Domyślnie buforowane poświadczenia znajdują się w `$HOME/.Azure` katalogu na hoście. Usługa Docker musi mieć dostęp do tej lokalizacji, aby uzyskać dostęp do poświadczeń. Następujące polecenie uruchamia kontener z zainstalowaną pamięcią podręczną poświadczeń i uruchamia interaktywną sesję programu PowerShell.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Usuń obraz, gdy nie jest już konieczny

Następujące polecenie służy do usuwania kontenera platformy Docker, gdy nie jest już potrzebne.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
