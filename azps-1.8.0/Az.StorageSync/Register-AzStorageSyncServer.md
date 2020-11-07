---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707450"
---
# Register-AzStorageSyncServer

## STRESZCZENIe
To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania. Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.

## POLECENIA

### ObjectParameterSet (domyślny)
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StringParameterSet
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentStringParameterSet
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
To polecenie rejestruje serwer w usłudze synchronizacji magazynu, zasób najwyższego poziomu w usłudze Azure File Sync. Utworzono relację zaufania między serwerem a usługą synchronizacji magazynu, która zapewnia bezpieczne przesyłanie danych i kanałów zarządzania. Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze. Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu. Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.
Polecenie musi być uruchamiane lokalnie na serwerze, który ma zostać zarejestrowany — wykonywane bezpośrednio lub za pośrednictwem zdalnej sesji programu PowerShell. Nie można zaakceptować obiektu komputera zdalnego.

## Przykłady

### Przykład 1
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

To polecenie spowoduje zarejestrowanie serwera lokalnego.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Obiekt nadrzędnyobject
Obiekt StorageSyncService, zwykle przepuszczany przez parametr.

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
Identyfikator zasobu nadrzędnego StorageSyncService

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageSyncServiceName
Nazwa StorageSyncService.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService

## WYSYŁA

### Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer

## INFORMACYJN

## LINKI POKREWNE
