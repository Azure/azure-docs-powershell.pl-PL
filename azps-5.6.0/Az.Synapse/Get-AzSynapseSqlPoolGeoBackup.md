---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957866"
---
# Get-AzSynapseSqlPoolGeoBackup

## SYNOPSIS
Pobiera nadmiarową geograficznie kopię zapasową puli sql.

## SKŁADNIA

### GetByNameParameterSet (domyślne)
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolGeoBackupResourceId
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSynapseSqlPoolGeoBackup** pobiera określoną geograficznie nadmiarową kopię zapasową puli SQL lub wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym.
Geograficznie nadmiarowa kopia zapasowa to zasób, który można przywrócić, używając plików danych z oddzielnej lokalizacji geograficznej.
Za pomocą Geo-Restore można przywrócić geograficznie nadmiarową kopię zapasową na wypadek 30-owej 32-65-855 0000 0000000000000000000000000000000000000000000000000000000

## PRZYKŁADY

### Przykład 1. Uzyskiwanie określonej nadmiarowej geograficznej kopii zapasowej
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
Polecenie cmdlet pobiera kopię zapasową lokalizacji geograficznej dla puli sql.

### Przykład 2. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych w obszarze roboczym
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym.

### Przykład 3. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych w obszarze roboczym przy użyciu filtrowania
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe w określonym obszarze roboczym, które zaczynają się od "Contoso".

## PARAMETERS

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

### — Nazwa
Pula języka Sql Synapse.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Wprowadź identyfikator zasobu geo kopii zapasowej puli sql.

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

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
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nazwa obszaru roboczego aplikacji Synapse.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Synapse.Models.PSBackupModel

## NOTATKI

## LINKI POKREWNE
