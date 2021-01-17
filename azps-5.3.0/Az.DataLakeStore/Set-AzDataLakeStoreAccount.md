---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 15a99d07630f6060473f66f985cfa8b8bf06d1e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489085"
---
# Set-AzDataLakeStoreAccount

## STRESZCZENIe
Modyfikuje konto w usłudze Data Lake Store.

## POLECENIA

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzDataLakeStoreAccount** modyfikuje konto usługi Data Lake Store.

## Przykłady

### Przykład 1. Dodawanie znacznika do konta
```powershell
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

To polecenie umożliwia dodanie określonego tagu do konta usługi Data Lake Store o nazwie ContosoADL.

### Przykład 2

Modyfikuje konto w usłudze Data Lake Store. (autogenerowana)

<!-- Aladdin Generated Example -->
```powershell
Set-AzDataLakeStoreAccount -FirewallState Enabled -Name 'ContosoADL'
```

## PARAMETRÓW

### -AllowAzureIpState
Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Domyślna
Określa identyfikator grupy katalogów usługi AzureActive.
Ta grupa jest domyślną grupą tworzonych plików i folderów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallState
Opcjonalnie Włącz lub Wyłącz istniejące reguły zapory.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wersja-
Jeśli typ szyfrowania jest przypisany przez użytkownika, użytkownik może obrócić swoją wersję klucza za pomocą tego parametru.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konta usługi Data Lake Store.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store do zmodyfikowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Określa znaczniki jako pary klucz-wartość.
Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Warstwowy
Pożądana warstwa zobowiązań do użycia dla tego konta.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrustedIdProviderState
Opcjonalnie Włącz lub Wyłącz istniejących dostawców zaufanych identyfikatorów.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. Collections. Hashtable

### System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. FirewallState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store......... usługi. Microsoft. Azure. Management. datalake. Store.

### System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## WYSYŁA

### Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount

## INFORMACYJN

## LINKI POKREWNE

[Get-AzDataLakeStoreAccount](./Get-AzDataLakeStoreAccount.md)

[Nowe — AzDataLakeStoreAccount](./New-AzDataLakeStoreAccount.md)

[Remove-AzDataLakeStoreAccount](./Remove-AzDataLakeStoreAccount.md)

[Test — AzDataLakeStoreAccount](./Test-AzDataLakeStoreAccount.md)


