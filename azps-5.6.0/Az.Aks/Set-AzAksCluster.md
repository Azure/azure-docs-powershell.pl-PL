---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0cf25018ad9cb432b739f5beeb147d20272d7f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002026"
---
# Set-AzAksCluster

## SYNOPSIS
Aktualizowanie lub tworzenie zarządzanego klastru Kubernetes.

## SKŁADNIA

### defaultParameterSet (Default)
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Aktualizowanie lub tworzenie zarządzanego klastru Kubernetes.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

Ustaw liczbę węzłów w klastrze Kubernetes na 5.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -DnsNamePrefix
Prefiks nazwy DNS dla klastra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNodeAutoScaling
Czy włączyć automatyczny skaler

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

### — Identyfikator
Identyfikator zarządzanego klastra Kubernetes

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KubernetesVersion
Wersja programu Kubernetes do tworzenia klastrów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxProfileAdminUserName
Nazwa użytkownika dla maszyn wirtualnych systemu Linux.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja na platformie Azure dla klastrów.
Domyślnie jest to lokalizacja grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa zarządzanego klastra przez użytkownika Kubernetes.

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeCount
Domyślna liczba węzłów dla pul węzłów.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeMaxCount
Maksymalna liczba węzłów na skalowanie automatyczne

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeMinCount
Minimalna liczba węzłów do automatycznego skalowania.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeName
Unikatowa nazwa profilu puli agenta w kontekście grupy subskrypcji i zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeOsSizeSize
Domyślna liczba węzłów dla pul węzłów.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodePoolMode
NodePoolMode reprezentuje tryb puli węzła.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeVmSize
Rozmiar maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipalIdAndSecret
Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshKeyValue
Wartość pliku klucza SSH lub ścieżka pliku klucza.
Domyślnie jest to plik {HOME}/.ssh/id_rsa.pub.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi do zastosowania do zasobu

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster

## NOTATKI

## LINKI POKREWNE
