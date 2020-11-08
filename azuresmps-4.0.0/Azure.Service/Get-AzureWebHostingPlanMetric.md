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
# <span data-ttu-id="bf927-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="bf927-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="bf927-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf927-102">SYNOPSIS</span></span>
<span data-ttu-id="bf927-103">Pobiera metryki planów hostingu witryny sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf927-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="bf927-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf927-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf927-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf927-105">DESCRIPTION</span></span>
<span data-ttu-id="bf927-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf927-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bf927-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bf927-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bf927-108">Polecenie cmdlet **Get-AzureWebHostingPlanMetric** pobiera metryki dla planów hostingu usługi Azure Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf927-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="bf927-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf927-109">EXAMPLES</span></span>

### <span data-ttu-id="bf927-110">Przykład 1: uzyskiwanie metryk dla ostatnich trzech godzin na poziomie poszczególnych wystąpień</span><span class="sxs-lookup"><span data-stu-id="bf927-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
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

<span data-ttu-id="bf927-111">To polecenie pobiera metryki planu hostingu w sieci Web dla ostatnich trzech godzin na poziomie każdego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="bf927-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="bf927-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf927-112">PARAMETERS</span></span>

### <span data-ttu-id="bf927-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="bf927-113">-EndDate</span></span>
<span data-ttu-id="bf927-114">Określa godzinę zakończenia jako obiekt **DateTime** , z której mają zostać zwrócone metryki.</span><span class="sxs-lookup"><span data-stu-id="bf927-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="bf927-115">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="bf927-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="bf927-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bf927-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="bf927-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="bf927-117">-InstanceDetails</span></span>
<span data-ttu-id="bf927-118">Wskazuje, że to polecenie cmdlet zawiera szczegóły dotyczące poziomu każdego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="bf927-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="bf927-119">Jeśli plan hostingu witryny internetowej jest uruchomiony na co najmniej dwóch komputerach, to polecenie cmdlet zwróci szczegóły metryki dla każdego komputera.</span><span class="sxs-lookup"><span data-stu-id="bf927-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

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

### <span data-ttu-id="bf927-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="bf927-120">-MetricNames</span></span>
<span data-ttu-id="bf927-121">Gatunek tablica miar do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bf927-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="bf927-122">Jeśli nie określisz wartości dla tego parametru, to polecenie cmdlet będzie pobierać wszystkie metryki.</span><span class="sxs-lookup"><span data-stu-id="bf927-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="bf927-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf927-123">-Name</span></span>
<span data-ttu-id="bf927-124">Określa nazwę planu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf927-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="bf927-125">Domyślnie polecenie **Get-AzureWebHostingPlanMetric** pobiera wszystkie witryny sieci Web w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf927-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="bf927-126">Ten parametr nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="bf927-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="bf927-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="bf927-127">-Profile</span></span>
<span data-ttu-id="bf927-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf927-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf927-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bf927-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf927-130">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="bf927-130">-StartDate</span></span>
<span data-ttu-id="bf927-131">Określa godzinę rozpoczęcia jako obiekt **DateTime** , dla którego mają być uzyskiwane metryki.</span><span class="sxs-lookup"><span data-stu-id="bf927-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

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

### <span data-ttu-id="bf927-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="bf927-132">-TimeGrain</span></span>
<span data-ttu-id="bf927-133">Określa jednostkę czasu, dla której mają zostać wyświetlone metryki.</span><span class="sxs-lookup"><span data-stu-id="bf927-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="bf927-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="bf927-134">Valid values are:</span></span> 

- <span data-ttu-id="bf927-135">PT1M (minuta)</span><span class="sxs-lookup"><span data-stu-id="bf927-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="bf927-136">PT1H (godzina)</span><span class="sxs-lookup"><span data-stu-id="bf927-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="bf927-137">P1D (dzień)</span><span class="sxs-lookup"><span data-stu-id="bf927-137">P1D (Day)</span></span>

<span data-ttu-id="bf927-138">Wartość domyślna to PT1H.</span><span class="sxs-lookup"><span data-stu-id="bf927-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="bf927-139">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="bf927-139">-WebSpaceName</span></span>
<span data-ttu-id="bf927-140">Określa nazwę przestrzeni sieci w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf927-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="bf927-141">Domyślnie polecenie **Get-AzureWebHostingPlanMetric** pobiera wszystkie plany w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf927-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="bf927-142">Ten parametr nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="bf927-142">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="bf927-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf927-143">CommonParameters</span></span>
<span data-ttu-id="bf927-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf927-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf927-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf927-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf927-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf927-146">INPUTS</span></span>

###  
<span data-ttu-id="bf927-147">Do tego polecenia cmdlet można przekazać dane wejściowe według nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="bf927-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bf927-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf927-148">OUTPUTS</span></span>

###  
<span data-ttu-id="bf927-149">Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="bf927-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="bf927-150">Domyślnie funkcja **Get-AzureWebHostingPlanMetric** zwraca tablicę obiektów **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="bf927-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="bf927-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf927-151">NOTES</span></span>

## <span data-ttu-id="bf927-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf927-152">RELATED LINKS</span></span>

[<span data-ttu-id="bf927-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="bf927-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


