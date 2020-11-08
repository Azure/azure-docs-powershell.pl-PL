---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054409"
---
# <span data-ttu-id="fcfbb-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fcfbb-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="fcfbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfbb-103">Umożliwia zaktualizowanie kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="fcfbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcfbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcfbb-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfbb-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fcfbb-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fcfbb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fcfbb-108">Polecenie cmdlet **Set-AzureSchedulerJobCollection** umożliwia zaktualizowanie kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="fcfbb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcfbb-109">EXAMPLES</span></span>

### <span data-ttu-id="fcfbb-110">Przykład 1. Zmienianie maksymalnej liczby zadań dla kolekcji</span><span class="sxs-lookup"><span data-stu-id="fcfbb-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="fcfbb-111">To polecenie powoduje zmianę maksymalnej liczby zadań na 30 w istniejącej kolekcji zadań harmonogramu o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="fcfbb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcfbb-112">PARAMETERS</span></span>

### <span data-ttu-id="fcfbb-113">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="fcfbb-113">-Frequency</span></span>
<span data-ttu-id="fcfbb-114">Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w tej kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="fcfbb-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fcfbb-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcfbb-116">Minutę</span><span class="sxs-lookup"><span data-stu-id="fcfbb-116">Minute</span></span>
- <span data-ttu-id="fcfbb-117">Dobow</span><span class="sxs-lookup"><span data-stu-id="fcfbb-117">Hour</span></span>
- <span data-ttu-id="fcfbb-118">Dniach</span><span class="sxs-lookup"><span data-stu-id="fcfbb-118">Day</span></span>
- <span data-ttu-id="fcfbb-119">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="fcfbb-119">Week</span></span>
- <span data-ttu-id="fcfbb-120">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="fcfbb-120">Month</span></span>
- <span data-ttu-id="fcfbb-121">Poprzedniego</span><span class="sxs-lookup"><span data-stu-id="fcfbb-121">Year</span></span>

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

### <span data-ttu-id="fcfbb-122">-Interval</span><span class="sxs-lookup"><span data-stu-id="fcfbb-122">-Interval</span></span>
<span data-ttu-id="fcfbb-123">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="fcfbb-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="fcfbb-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fcfbb-124">-JobCollectionName</span></span>
<span data-ttu-id="fcfbb-125">Określa nazwę kolekcji zadań harmonogramu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="fcfbb-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fcfbb-126">-Location</span></span>
<span data-ttu-id="fcfbb-127">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="fcfbb-128">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="fcfbb-128">Valid values are:</span></span> 

- <span data-ttu-id="fcfbb-129">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="fcfbb-129">Anywhere Asia</span></span>
- <span data-ttu-id="fcfbb-130">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="fcfbb-130">Anywhere Europe</span></span>
- <span data-ttu-id="fcfbb-131">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-131">Anywhere US</span></span>
- <span data-ttu-id="fcfbb-132">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="fcfbb-132">East Asia</span></span>
- <span data-ttu-id="fcfbb-133">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-133">East US</span></span>
- <span data-ttu-id="fcfbb-134">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-134">North Central US</span></span>
- <span data-ttu-id="fcfbb-135">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="fcfbb-135">North Europe</span></span>
- <span data-ttu-id="fcfbb-136">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="fcfbb-136">South Central US</span></span>
- <span data-ttu-id="fcfbb-137">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="fcfbb-137">Southeast Asia</span></span>
- <span data-ttu-id="fcfbb-138">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="fcfbb-138">West Europe</span></span>
- <span data-ttu-id="fcfbb-139">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-139">West US</span></span>

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

### <span data-ttu-id="fcfbb-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="fcfbb-140">-MaxJobCount</span></span>
<span data-ttu-id="fcfbb-141">Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="fcfbb-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcfbb-142">-PassThru</span></span>
<span data-ttu-id="fcfbb-143">Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="fcfbb-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcfbb-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="fcfbb-145">-Plan</span></span>
<span data-ttu-id="fcfbb-146">Określa plan kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="fcfbb-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="fcfbb-147">-Profile</span></span>
<span data-ttu-id="fcfbb-148">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcfbb-149">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcfbb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfbb-150">CommonParameters</span></span>
<span data-ttu-id="fcfbb-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfbb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfbb-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfbb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfbb-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcfbb-153">INPUTS</span></span>

## <span data-ttu-id="fcfbb-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcfbb-154">OUTPUTS</span></span>

## <span data-ttu-id="fcfbb-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcfbb-155">NOTES</span></span>

## <span data-ttu-id="fcfbb-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcfbb-156">RELATED LINKS</span></span>

[<span data-ttu-id="fcfbb-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fcfbb-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="fcfbb-158">Nowe — AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fcfbb-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="fcfbb-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fcfbb-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


