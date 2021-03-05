---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973178"
---
# Moduł Az.StorageSync
## Opis
Polecenia cmdlet w module synchronizacji przestrzeni dyskowej umożliwiają zarządzanie operacjami odnoszącym się do synchronizacji plików platformy Azure w programie PowerShell.

## Az.StorageSync Cmdlet
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
To polecenie wyświetla listę wszystkich punktów końcowych chmury w obrębie danej grupy synchronizacji.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
To polecenie zawiera listę wszystkich grup synchronizacji w ramach danej usługi synchronizacji przestrzeni dyskowej.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
To polecenie zawiera listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji przestrzeni dyskowej.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
To polecenie zawiera listę wszystkich usług synchronizacji przestrzeni dyskowej w obrębie danego zakresu grupy subskrypcji/zasobów.

### [Invoke-AzstorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw. Może być kierowana do całego udziału, podfolderu lub zestawu plików. Wykrywanych może być maksymalnie 10 000 zmian. Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian można szybko zakończyć i z ograniczeniem do 10 000 zmian.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Sprawdza potencjalne problemy ze zgodnością między systemem a usługą Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
To polecenie przypomina wszystkie pliki warstwowe z powrotem na dysk lokalny.

### [New-azstorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
To polecenie tworzy punkt końcowy chmury synchronizacji plików platformy Azure w grupie synchronizacji.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
To polecenie tworzy nową grupę synchronizacji w ramach określonej usługi synchronizacji przestrzeni dyskowej.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze. Dzięki temu określona ścieżka na serwerze może rozpocząć synchronizację plików z innymi punktami końcowymi w grupie synchronizacji.

### [New-AzstorageSyncService](New-AzStorageSyncService.md)
To polecenie tworzy nową usługę synchronizacji przestrzeni dyskowej w grupie zasobów.

### [Set-AzstorageSyncService](New-AzStorageSyncService.md)
To polecenie ustawia usługę synchronizacji magazynu w grupie zasobów.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
To polecenie rejestruje serwer w usłudze synchronizacji magazynu, co tworzy relację zaufania. Następnie można użyć programu PowerShell lub portalu Azure w celu skonfigurowania synchronizacji na tym serwerze.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji. Bez co najmniej jednego punktu końcowego chmury żadne inne punkty końcowe serwera w tej grupie synchronizacji nie mogą być synchronizowane.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
To polecenie spowoduje usunięcie określonej grupy synchronizacji.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
To polecenie spowoduje usunięcie określonego punktu końcowego serwera. Synchronizacja z tą lokalizacją zostanie zatrzymana natychmiast.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
To polecenie spowoduje usunięcie określonej usługi synchronizacji przestrzeni dyskowej.

### [Reset-AzstorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Używaj tylko do rozwiązywania problemów. To polecenie spowoduje roll the storage sync server certificate used to describe the server identity to the storage sync service.

### [Set-AzstorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
To polecenie umożliwia zmiany parametrów dostosowywanych punktu końcowego serwera.

### [Unregister-azstorageSyncServer](Unregister-AzStorageSyncServer.md)
Ostrzeżenie: Wyrejestrowanie serwera spowoduje usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze. To polecenie spowoduje wyrejestrowanie serwera z usługi synchronizacji przestrzeni dyskowej.

