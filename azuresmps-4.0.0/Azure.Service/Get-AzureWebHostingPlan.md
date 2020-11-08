---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055478"
---
# Get-AzureWebHostingPlan

## STRESZCZENIe
Pobiera plany hostingu usługi Azure w sieci Web w bieżącej subskrypcji.

## POLECENIA

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Get-AzureWebHostingPlan** pobiera plany hostingu w sieci Azure w bieżącej subskrypcji.

Domyślnie funkcja **Get-AzureWebHostingPlan** pobiera wszystkie plany hostingu platformy Azure w bieżącej subskrypcji i zwraca obiekt, który dostarcza podstawowych informacji o planach.
Gdy korzystasz z parametrów *przestrzeni* sieci i *nazwy* , funkcja **Get-AzureWebHostingPlan** zwraca konkretny obiekt planu hostingu.

Aby znaleźć bieżącą subskrypcję, użyj *bieżącego* parametru polecenia cmdlet **Get-AzureSubscription** .
Aby zmienić bieżącą subskrypcję, użyj polecenia cmdlet **SELECT-AzureSubscription** .

## Przykłady

### Przykład 1: pobieranie wszystkich planów hostingu w sieci Web w ramach subskrypcji
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

To polecenie pobiera wszystkie plany hostingu w sieci Web w bieżącej subskrypcji.

### Przykład 2: uzyskiwanie określonego planu hostingu w witrynie sieci Web w ramach abonamentu
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

To polecenie pobiera plan hostingu w sieci Web o nazwie Default0 w obszarze webspace o nazwie westeuropewebspace w bieżącej subskrypcji.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę planu w subskrypcji.
Domyślnie to polecenie cmdlet pobiera wszystkie plany w bieżącej subskrypcji.
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

### -Webspacename
Określa nazwę przestrzeni sieci w subskrypcji.
Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich witryn internetowych w określonym obszarze sieci Web.
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

### Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. WebHostingPlan
Domyślnie funkcja **Get-AzureWebHostingPlan** zwraca tablicę obiektów **WebHostingPlan** .

## INFORMACYJN

## LINKI POKREWNE

