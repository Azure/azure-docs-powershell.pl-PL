---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: df81f976f571a59f68d51ef734f1bc3ea5536015
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991250"
---
# New-AzEventGridTopic

## SYNOPSIS
Tworzy nowy temat siatki zdarzeń platformy Azure.

## SKŁADNIA

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Tworzy nowy temat siatki zdarzeń platformy Azure. Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

Tworzy temat Siatki zdarzeń , temat1 w określonej lokalizacji geograficznej zachódus2, w grupie zasobów \` \` \` \` \` Nazwa_grupy_Zasobów. \`

### Przykład 2
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

Tworzy temat Siatki zdarzeń , temat1 w określonej lokalizacji geograficznej zachódus2, w grupie zasobów Nazwa_grupy Zasobów o określonych tagach \` \` "Dział" i \` \` \` \` "Środowisko".

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

### -InboundIpRule
Tabela skrótów reprezentująca listę reguł ip ruchu przychodzącego. Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiadającą mu akcją do wykonania na podstawie dopasowania lub bez dopasowania maski IpMask. Możliwe wartości akcji to tylko Zezwalaj

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

### -InputMappingDefaultValue
Hashtable which represents the input mapping fields with default value in space separated key = value format. Dozwolone nazwy kluczy to: temat, typ zdarzenia i dataversion. Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.

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

### -InputMappingField
Tabela skrótów reprezentująca pola mapowania danych wejściowych w formacie klawiszy oddzielonych spacjami = format wartości. Dozwolone nazwy kluczy to: identyfikator, temat, czas zdarzenia, temat, typ zdarzenia i dataversion. Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.

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

### -InputSchema
Schemat zdarzeń wprowadzania dla tematu. Dopuszczalne wartości to: eventgridschema, customeventschema lub cloudeventv01Schema. Wartość domyślna to eventgridschema. Zwróć uwagę, że jeśli zostanie określony parametr customeventschema, należy również określić parametry InputMappingField lub/i InputMappingDefaultValue.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja tematu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Nazwa tematu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Pozwala to określić, czy ruch jest dozwolony za pośrednictwem sieci publicznej. Domyślnie jest ona włączona. Możesz dodatkowo ograniczyć się do określonych wiadomości IP, konfigurując parametry przychodzącej pocztyiprule. Dozwolone wartości są wyłączone i włączone.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, w której należy utworzyć temat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Skróty reprezentujące tagi zasobów.

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

### System.String

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

## NOTATKI

## LINKI POKREWNE
