---
title: Korzystanie z programu Azure PowerShell na platformie Docker
description: Jak używać programu Azure PowerShell wstępnie zainstalowanego w obrazie platformy Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402684"
---
# <a name="using-azure-powershell-in-docker"></a>Korzystanie z programu Azure PowerShell na platformie Docker

Publikujemy obrazy platformy Docker z wstępnie zainstalowanym programem Azure PowerShell. W tym artykule pokazano, jak rozpocząć korzystanie z programu Azure PowerShell w kontenerze platformy Docker.

## <a name="finding-available-images"></a>Znajdowanie dostępnych obrazów

Wydane obrazy wymagają platformy Docker 17.05 lub nowszej. Oczekuje się również, że możesz uruchomić platformę Docker bez użycia polecenia `sudo` ani lokalnych uprawnień administracyjnych. Skorzystaj z oficjalnych [instrukcji][install], aby poprawnie zainstalować platformę `docker`.

Wydane kontenery zostały utworzone na podstawie oficjalnych kontenerów programu PowerShell, a następnie dodano do nich moduł Az jako warstwę.

Najnowszy stabilny obraz obejmuje następujące składniki:

- Ubuntu 18.04
- PowerShell 6.2.4
- Najnowszy moduł Az programu Azure PowerShell

Pełną listę dostępnych obrazów można znaleźć na naszej stronie [obrazów platformy Docker][az image].

## <a name="using-azure-powershell-in-a-container"></a>Korzystanie z programu Azure PowerShell w kontenerze

Poniższe kroki pokazują polecenia platformy Docker wymagane do pobrania obrazu i uruchomienia interaktywnej sesji programu PowerShell.

1. Pobierz najnowszy obraz azure-powershell.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Uruchom kontener azure-powershell w trybie interaktywnym:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Interaktywne uruchamianie kontenera azure-powershell przy użyciu uwierzytelniania hosta

Jeśli w systemie hostującym platformę Docker jest już zainstalowany program Azure PowerShell, być może masz buforowane poświadczenia platformy Azure. Tych poświadczeń można używać w sesji programu PowerShell działającej w kontenerze platformy Docker.

Domyślnie buforowane poświadczenia znajdują się w katalogu `$HOME/.Azure` na hoście. Usługa Docker musi mieć dostęp do tej lokalizacji, aby uzyskać dostęp do poświadczeń. Następujące polecenie uruchamia kontener z zainstalowaną pamięcią podręczną poświadczeń i uruchamia interaktywną sesję programu PowerShell.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Usuwanie obrazu, gdy nie jest już konieczny

Następujące polecenie służy do usuwania kontenera platformy Docker, gdy nie jest już potrzebny.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell