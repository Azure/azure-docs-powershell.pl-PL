---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219720"
---
# AZ. StorageSync, moduł
## Opis
Polecenia cmdlet w module synchronizacji magazynu umożliwiają zarządzanie operacjami związanymi z synchronizacją plików Azure w programie PowerShell.

## AZ. StorageSync polecenia cmdlet
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
To polecenie wyświetla listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji magazynu.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw. Można go kierować do całego udziału, podfolderu lub zestawu plików. Można wykryć maksymalnie 10 000 zmian. Jeśli zakres zmian jest dla Ciebie znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 zmian.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
To polecenie ponownie wywołuje wszystkie pliki warstw z powrotem na dysk lokalny.

### [Nowe — AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure w grupie synchronizacji.

### [Nowe — AzStorageSyncGroup](New-AzStorageSyncGroup.md)
To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.

### [Nowe — AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze. Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.

### [Nowe — AzStorageSyncService](New-AzStorageSyncService.md)
To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
To polecenie służy do ustawiania usługi synchronizacji magazynu w grupie zasobów.

### [Rejestr — AzStorageSyncServer](Register-AzStorageSyncServer.md)
To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania. Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji. Bez co najmniej jednego punktu końcowego w chmurze nie można zsynchronizować innych punktów końcowych serwera w tej grupie synchronizacji.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
To polecenie spowoduje usunięcie określonej grupy synchronizacji.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
To polecenie spowoduje usunięcie określonego punktu końcowego serwera. Synchronizacja z tą lokalizacją zostanie natychmiast zatrzymana.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.

### [Resetowanie — AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Służy tylko do rozwiązywania problemów. To polecenie spowoduje wywrócenie certyfikatu serwera synchronizacji magazynu użytego do opisania tożsamości serwera w usłudze synchronizacji magazynu.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.

### [Wyrejestrowanie — AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze. To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.

