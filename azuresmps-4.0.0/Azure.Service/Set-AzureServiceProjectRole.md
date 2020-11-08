---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054918"
---
# Set-AzureServiceProjectRole

## STRESZCZENIe
Ustawia liczbę wystąpień lub wersję wykonawczą roli.

## POLECENIA

### Instance
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Runtime
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### VMSize
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Set-AzureServiceProjectRole** ustawia liczbę wystąpień roli dla określonej roli.

## Przykłady

### Przykład 1: Ustawianie wystąpień roli sieci Web
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

Ustawia liczbę wystąpień roli sieci Web o nazwie MyWebRole1 na wartość 2.

### Przykład 2: Ustawianie wystąpień roli pracownika
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

Ustawia liczbę wystąpień roli dla roli pracownika o nazwie WorkerRole1 na 2.

### Przykład 3: Ustawianie wersji środowiska wykonawczego dla usługi roli
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

Ustawia node.exeą wersję środowiska wykonawczego dla roli MyRole1 na 0.6.20.

## PARAMETRÓW

### -Wystąpienia
Określa liczbę wystąpień roli dla określonej roli w sieci Web lub w ramach procesu roboczego.

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rolename
Określa nazwę roli sieci Web lub procesu roboczego, która ma zostać zmieniona.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Określa środowisko uruchomieniowe, które ma zostać dodane do określonej roli.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Określa wersję środowiska uruchomieniowego, którą należy dodać do roli.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Określa rozmiar maszyny wirtualnej roli.

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

###  
Określa rozmiar maszyny wirtualnej.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


