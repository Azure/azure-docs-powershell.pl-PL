---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055237"
---
# <span data-ttu-id="f59e2-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="f59e2-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="f59e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f59e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f59e2-103">Pobiera metryki dla witryny internetowej platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f59e2-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="f59e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f59e2-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f59e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f59e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f59e2-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f59e2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f59e2-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f59e2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f59e2-108">Polecenie cmdlet **Get-AzureWebsiteMetric** pobiera metryki dla witryny internetowej platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f59e2-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="f59e2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f59e2-109">EXAMPLES</span></span>

### <span data-ttu-id="f59e2-110">Przykład 1: uzyskiwanie metryk dla ostatnich trzech godzin na poziomie wystąpienia dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="f59e2-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="f59e2-111">To polecenie pobiera metryki dla ostatnich trzech godzin na poziomie wystąpienia dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f59e2-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="f59e2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f59e2-112">PARAMETERS</span></span>

### <span data-ttu-id="f59e2-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f59e2-113">-EndDate</span></span>
<span data-ttu-id="f59e2-114">Określa czas, jako obiekt **DateTime** , aby zatrzymać uzyskiwanie metryk.</span><span class="sxs-lookup"><span data-stu-id="f59e2-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="f59e2-115">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="f59e2-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f59e2-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f59e2-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="f59e2-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="f59e2-117">-InstanceDetails</span></span>
<span data-ttu-id="f59e2-118">Wskazuje, że to polecenie cmdlet zawiera szczegóły dotyczące poziomu każdego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f59e2-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="f59e2-119">Jeśli plan hostingu w sieci Web jest uruchomiony na co najmniej dwóch komputerach, to polecenie cmdlet zwraca metryki dla każdego komputera.</span><span class="sxs-lookup"><span data-stu-id="f59e2-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="f59e2-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="f59e2-120">-MetricNames</span></span>
<span data-ttu-id="f59e2-121">Określa tablicę metryk, które należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="f59e2-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="f59e2-122">Jeśli nie podano tego parametru, polecenie cmdlet pobiera wszystkie metryki.</span><span class="sxs-lookup"><span data-stu-id="f59e2-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="f59e2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f59e2-123">-Name</span></span>
<span data-ttu-id="f59e2-124">Określa nazwę witryny sieci Web w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f59e2-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="f59e2-125">Ten parametr nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="f59e2-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="f59e2-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="f59e2-126">-Profile</span></span>
<span data-ttu-id="f59e2-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f59e2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f59e2-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f59e2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f59e2-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="f59e2-129">-Slot</span></span>
<span data-ttu-id="f59e2-130">Określa środowisko wdrożenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="f59e2-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="f59e2-131">Prawidłowe wartości: produkcja i przemieszczanie.</span><span class="sxs-lookup"><span data-stu-id="f59e2-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="f59e2-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="f59e2-132">-SlotView</span></span>
<span data-ttu-id="f59e2-133">Wskazuje, że to polecenie cmdlet pobiera metryki dla nazw hostów, które odbierają ruch w bieżącym gnieździe.</span><span class="sxs-lookup"><span data-stu-id="f59e2-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="f59e2-134">Jeśli Zamiana nastąpi w okresie, metryki są scalane.</span><span class="sxs-lookup"><span data-stu-id="f59e2-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="f59e2-135">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="f59e2-135">-StartDate</span></span>
<span data-ttu-id="f59e2-136">Określa czas, w jakim obiekt **DateTime** ma rozpocząć uzyskiwanie metryk.</span><span class="sxs-lookup"><span data-stu-id="f59e2-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="f59e2-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="f59e2-137">-TimeGrain</span></span>
<span data-ttu-id="f59e2-138">Określa jednostkę czasu dla metryk.</span><span class="sxs-lookup"><span data-stu-id="f59e2-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="f59e2-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f59e2-139">Valid values are:</span></span> 

- <span data-ttu-id="f59e2-140">PT1M (minuta)</span><span class="sxs-lookup"><span data-stu-id="f59e2-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="f59e2-141">PT1H (godzina)</span><span class="sxs-lookup"><span data-stu-id="f59e2-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="f59e2-142">P1D (dzień)</span><span class="sxs-lookup"><span data-stu-id="f59e2-142">P1D (Day)</span></span>

<span data-ttu-id="f59e2-143">Wartość domyślna to PT1H.</span><span class="sxs-lookup"><span data-stu-id="f59e2-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="f59e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59e2-144">CommonParameters</span></span>
<span data-ttu-id="f59e2-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59e2-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59e2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59e2-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f59e2-147">INPUTS</span></span>

###  
<span data-ttu-id="f59e2-148">Do tego polecenia cmdlet można przekazać dane wejściowe według nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="f59e2-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f59e2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f59e2-149">OUTPUTS</span></span>

### <span data-ttu-id="f59e2-150">Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="f59e2-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="f59e2-151">Domyślnie funkcja **Get-AzureWebsiteMetric** zwraca tablicę obiektów **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="f59e2-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="f59e2-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f59e2-152">NOTES</span></span>

## <span data-ttu-id="f59e2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f59e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="f59e2-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f59e2-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


