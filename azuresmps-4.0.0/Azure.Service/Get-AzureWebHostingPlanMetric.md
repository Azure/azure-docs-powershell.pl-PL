---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055476"
---
# Get-AzureWebHostingPlanMetric

## STRESZCZENIe
Pobiera metryki planów hostingu witryny sieci Web platformy Azure.

## POLECENIA

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Get-AzureWebHostingPlanMetric** pobiera metryki dla planów hostingu usługi Azure Web w ramach subskrypcji.

## Przykłady

### Przykład 1: uzyskiwanie metryk dla ostatnich trzech godzin na poziomie poszczególnych wystąpień
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

To polecenie pobiera metryki planu hostingu w sieci Web dla ostatnich trzech godzin na poziomie każdego wystąpienia.

## PARAMETRÓW

### -EndDate
Określa godzinę zakończenia jako obiekt **DateTime** , z której mają zostać zwrócone metryki.
Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceDetails
Wskazuje, że to polecenie cmdlet zawiera szczegóły dotyczące poziomu każdego wystąpienia.
Jeśli plan hostingu witryny internetowej jest uruchomiony na co najmniej dwóch komputerach, to polecenie cmdlet zwróci szczegóły metryki dla każdego komputera.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricNames
Gatunek tablica miar do pobrania.
Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet będzie pobierać wszystkie metryki.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę planu w subskrypcji.
Domyślnie polecenie **Get-AzureWebHostingPlanMetric** pobiera wszystkie witryny sieci Web w bieżącej subskrypcji.
Ten parametr nie obsługuje symboli wieloznacznych.

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

### -DataRozpoczęcia
Określa godzinę rozpoczęcia jako obiekt **DateTime** , dla którego mają być uzyskiwane metryki.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeGrain
Określa jednostkę czasu, dla której mają zostać wyświetlone metryki.
Prawidłowe wartości: 

- PT1M (minuta) 
- PT1H (godzina) 
- P1D (dzień)

Wartość domyślna to PT1H.

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

### -Webspacename
Określa nazwę przestrzeni sieci w subskrypcji.
Domyślnie polecenie **Get-AzureWebHostingPlanMetric** pobiera wszystkie plany w bieżącej subskrypcji.
Ten parametr nie obsługuje symboli wieloznacznych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

###  
Do tego polecenia cmdlet można przekazać dane wejściowe według nazwy właściwości, ale nie według wartości.

## WYSYŁA

###  
Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. MetricResponse

Domyślnie funkcja **Get-AzureWebHostingPlanMetric** zwraca tablicę obiektów **MetricResponse** .

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureWebHostingPlan](./Get-AzureWebHostingPlan.md)


