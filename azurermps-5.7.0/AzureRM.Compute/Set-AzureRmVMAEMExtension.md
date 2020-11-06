---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: edc91b756b90684299d84228c04862a0ce6c2e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525278"
---
# Set-AzureRmVMAEMExtension

## STRESZCZENIe
Włączanie obsługi monitorowania systemów SAP.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmVMAEMExtension** umożliwia zaktualizowanie konfiguracji maszyny wirtualnej w celu włączenia lub zaktualizowania pomocy technicznej dotyczącej monitorowania systemów SAP zainstalowanych na maszynie wirtualnej.
Polecenie cmdlet umożliwia zainstalowanie rozszerzenia rozszerzonego monitorowania platformy Azure (AEM) zbierającego dane dotyczące wydajności i umożliwia odnajdowanie go dla systemu SAP.

## Przykłady

### Przykład 1: Używanie rozszerzenia AEM
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

To polecenie umożliwia skonfigurowanie maszyny wirtualnej o nazwie contoso — serwer w celu używania rozszerzenia AEM.
To polecenie Określa konto magazynu o nazwie stdstorage.

## PARAMETRÓW

### -DisableWAD
Wskazuje, że to polecenie cmdlet nie włącza diagnostyki platformy Azure dla maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWAD
Jeśli ten parametr zostanie podany, unifiedgroup włączy diagnostykę platformy Windows Azure dla tej maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Określa typ systemu operacyjnego dysku systemu operacyjnego.
Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.
Dopuszczalne wartości tego parametru to: Windows i Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet modyfikuje.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorage
Wskazuje, że to polecenie cmdlet pominie konfigurację miejsca do magazynowania.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej.
To polecenie cmdlet umożliwia dodanie rozszerzenia AEM dla maszyny wirtualnej, którą ten parametr określa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Określa nazwę konta magazynu, którego używa polecenie cmdlet w celu skonfigurowania rozszerzenia LinuxDiagnostics lub IaaSDiagnostics.
Jeśli maszyna wirtualna nie korzysta ze standardowego konta magazynu, należy określić wartość dla tego parametru.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Test — AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


