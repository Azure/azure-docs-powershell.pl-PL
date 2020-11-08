---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054946"
---
# <span data-ttu-id="507cd-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="507cd-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="507cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="507cd-102">SYNOPSIS</span></span>
<span data-ttu-id="507cd-103">Tworzy kolekcję zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="507cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="507cd-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="507cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="507cd-105">DESCRIPTION</span></span>
<span data-ttu-id="507cd-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="507cd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="507cd-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="507cd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="507cd-108">Polecenie cmdlet **New-AzureSchedulerJobCollection** tworzy kolekcję zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="507cd-109">Jeśli nie określisz wartości parametru *Plan* , polecenie cmdlet utworzy standardową kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="507cd-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="507cd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="507cd-110">EXAMPLES</span></span>

### <span data-ttu-id="507cd-111">Przykład 1. Tworzenie kolekcji zadań harmonogramu zawierającej wartości domyślne</span><span class="sxs-lookup"><span data-stu-id="507cd-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="507cd-112">To polecenie tworzy standardową kolekcję zadań harmonogramu o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="507cd-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="507cd-113">Nowa kolekcja zawiera domyślną liczbę zadań i maksymalny cykl dla kolekcji zadań harmonogramu standardowego.</span><span class="sxs-lookup"><span data-stu-id="507cd-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="507cd-114">Przykład 2: Tworzenie kolekcji zadań harmonogramu z określonymi wartościami</span><span class="sxs-lookup"><span data-stu-id="507cd-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="507cd-115">To polecenie tworzy standardową kolekcję zadań harmonogramu o nazwie JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="507cd-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="507cd-116">Nowa kolekcja zawiera maksymalną liczbę zadań 30 i maksymalnie 12 godzin.</span><span class="sxs-lookup"><span data-stu-id="507cd-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="507cd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="507cd-117">PARAMETERS</span></span>

### <span data-ttu-id="507cd-118">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="507cd-118">-Frequency</span></span>
<span data-ttu-id="507cd-119">Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w tej kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507cd-120">-Interval</span><span class="sxs-lookup"><span data-stu-id="507cd-120">-Interval</span></span>
<span data-ttu-id="507cd-121">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="507cd-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507cd-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="507cd-122">-JobCollectionName</span></span>
<span data-ttu-id="507cd-123">Określa nazwę nowej kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-123">Specifies the name for the new scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507cd-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="507cd-124">-Location</span></span>
<span data-ttu-id="507cd-125">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="507cd-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="507cd-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="507cd-126">Valid values are:</span></span> 

- <span data-ttu-id="507cd-127">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="507cd-127">Anywhere Asia</span></span>
- <span data-ttu-id="507cd-128">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="507cd-128">Anywhere Europe</span></span>
- <span data-ttu-id="507cd-129">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="507cd-129">Anywhere US</span></span>
- <span data-ttu-id="507cd-130">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="507cd-130">East Asia</span></span>
- <span data-ttu-id="507cd-131">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="507cd-131">East US</span></span>
- <span data-ttu-id="507cd-132">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="507cd-132">North Central US</span></span>
- <span data-ttu-id="507cd-133">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="507cd-133">North Europe</span></span>
- <span data-ttu-id="507cd-134">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="507cd-134">South Central US</span></span>
- <span data-ttu-id="507cd-135">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="507cd-135">Southeast Asia</span></span>
- <span data-ttu-id="507cd-136">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="507cd-136">West Europe</span></span>
- <span data-ttu-id="507cd-137">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="507cd-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507cd-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="507cd-138">-MaxJobCount</span></span>
<span data-ttu-id="507cd-139">Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507cd-140">-Plan</span><span class="sxs-lookup"><span data-stu-id="507cd-140">-Plan</span></span>
<span data-ttu-id="507cd-141">Określa plan kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="507cd-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="507cd-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="507cd-142">-Profile</span></span>
<span data-ttu-id="507cd-143">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="507cd-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="507cd-144">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="507cd-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="507cd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507cd-145">CommonParameters</span></span>
<span data-ttu-id="507cd-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507cd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507cd-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="507cd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507cd-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="507cd-148">INPUTS</span></span>

## <span data-ttu-id="507cd-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="507cd-149">OUTPUTS</span></span>

## <span data-ttu-id="507cd-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="507cd-150">NOTES</span></span>

## <span data-ttu-id="507cd-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="507cd-151">RELATED LINKS</span></span>

[<span data-ttu-id="507cd-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="507cd-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="507cd-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="507cd-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="507cd-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="507cd-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


