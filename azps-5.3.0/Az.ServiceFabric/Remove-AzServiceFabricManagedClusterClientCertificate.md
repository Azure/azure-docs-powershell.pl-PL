---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502792"
---
# Remove-AzServiceFabricManagedClusterClientCertificate

## STRESZCZENIe
Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.

## POLECENIA

### ClientCertByTpByObj (domyślny)
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClientCertByCnTpName
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ClientCertByCnByName
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ClientCertByCnByObj
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.

## Przykłady

### Przykład 1
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

Usuń certyfikat klienta według nazwy pospolitej.

### Przykład 2
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

Usuń certyfikat klienta według odcisku palca.

### Przykład 3
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

Usuń certyfikat klienta według odcisku palca z potokiem.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

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

### -CommonName
Nazwa pospolita certyfikatu klienta.

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Zarządzany zasób klastra

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określ nazwę klastra.

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru Description}}

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

### -ResourceGroupName
Określ nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Odcisk palca
Odcisk palca certyfikatu klienta.

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster

## INFORMACYJN

## LINKI POKREWNE
