---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180739"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Aktualizuje zestaw rekordów DNS.

## SKŁADNIA

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzDnsRecordSet** aktualizuje zestaw rekordów w usłudze Azure DNS z lokalnego **obiektu RecordSet.**
Obiekt **RecordSet** można przekazać jako parametr lub za pomocą operatora potoku.
Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.
Zestaw rekordów nie zostanie zaktualizowany, jeśli został zmieniony w usłudze Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**
Zapewnia to ochronę w przypadku jednoczesnych zmian.
To zachowanie można pominąć przy użyciu *parametru Zastąp,* który aktualizuje zestaw rekordów niezależnie od jednoczesnych zmian.

## PRZYKŁADY

### Przykład 1. Aktualizowanie zestawu rekordów
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Pierwsze polecenie używa Get-AzDnsRecordSet cmdlet w celu uzyskania określonego zestawu rekordów, a następnie zapisuje go w $RecordSet zmienną.
Drugie i trzecie polecenie to operacje off-line umożliwiające dodanie dwóch rekordów A do zestawu rekordów.
Ostatnie polecenie używa polecenia cmdlet **Set-AzDnsRecordSet** w celu zatwierdzenia aktualizacji.

### Przykład 2. Aktualizowanie rekordu SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Pierwsze polecenie używa polecenia cmdlet **Get-AzDnsRecordset** w celu uzyskania określonego zestawu rekordów, a następnie zapisuje go w $RecordSet zmienną.
Drugie polecenie aktualizuje określony rekord SOA w $RecordSet.
Ostatnie polecenie propaguje aktualizację w programie $RecordSet za pomocą polecenia cmdlet **Set-AzDnsRecordSet.**

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Zastąp
Wskazuje, aby zaktualizować zestaw rekordów niezależnie od jednoczesnych zmian.
Zestaw rekordów nie zostanie zaktualizowany, jeśli został zmieniony w usłudze Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**
Zapewnia to ochronę w przypadku jednoczesnych zmian.
Aby pominąć to zachowanie, można użyć parametru *Zastąp,* co powoduje, że zestaw rekordów jest aktualizowany niezależnie od jednoczesnych zmian.

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

### -RecordSet
Określa zestaw **rekordów do** zaktualizowania.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTATKI
Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.
Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, $ConfirmPreference zmienna programu Windows PowerShell ma wartość Średni lub niższy.
Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.
Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie. 

## LINKI POKREWNE

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
