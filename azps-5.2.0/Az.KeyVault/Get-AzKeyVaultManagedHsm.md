---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333034"
---
# Get-AzKeyVaultManagedHsm

## STRESZCZENIe
Pobierz HSMs zarządzaną.

## POLECENIA

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzKeyVaultManagedHsm** pobiera informacje o HSMsie zarządzanym w ramach abonamentu. Wszystkie zarządzane wystąpienia HSMs można wyświetlać w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonego modułu HSM.
Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, gdy jest wyświetlany jeden zarządzany obiekt HSM, należy to zrobić w celu uzyskania lepszej wydajności.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich zarządzanych HSMs w bieżącej subskrypcji
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera wszystkie HSMs zarządzane w bieżącej subskrypcji.

### Przykład 2: uzyskiwanie określonego zarządzanego modułu HSM
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie umożliwia pobieranie zarządzanego modułu HSM o nazwie myhsm w bieżącej subskrypcji.

### Przykład 3: uzyskiwanie zarządzanych HSMs w grupie zasobów
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera wszystkie HSMs zarządzane w grupie zasobów o nazwie myrg1.

### Przykład 4: uzyskiwanie HSMs zarządzanych przy użyciu filtrowania
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie uzyskuje wszystkie HSMs zarządzane w subskrypcji rozpoczynające się od "myhsm".

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
Nazwa modułu HSM. Polecenie cmdlet tworzy nazwę FQDN modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Określa nazwę grupy zasobów skojarzonej z badanym zarządzanym HSM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Tag
Określa klucz i opcjonalną wartość określonego tagu w celu filtrowania listy zarządzanych HSMs według.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. PSManagedHsm

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzKeyVaultManagedHsm](./New-AzKeyVaultManagedHsm.md)

[Remove-AzKeyVaultManagedHsm](./Remove-AzKeyVaultManagedHsm.md)

[Update-AzKeyVaultManagedHsm](./Update-AzKeyVaultManagedHsm.md)