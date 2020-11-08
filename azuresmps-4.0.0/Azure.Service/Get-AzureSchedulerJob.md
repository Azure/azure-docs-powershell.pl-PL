---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055277"
---
# <span data-ttu-id="02e03-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="02e03-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="02e03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02e03-102">SYNOPSIS</span></span>
<span data-ttu-id="02e03-103">Pobiera listę zadań harmonogramu lub określonego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="02e03-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="02e03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02e03-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02e03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02e03-105">DESCRIPTION</span></span>
<span data-ttu-id="02e03-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="02e03-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02e03-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02e03-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02e03-108">Polecenie cmdlet **Get-AzureSchedulerJobCollection** pobiera listę zadań harmonogramu lub określonego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="02e03-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="02e03-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02e03-109">EXAMPLES</span></span>

### <span data-ttu-id="02e03-110">Przykład 1. pobieranie wszystkich zadań w kolekcji</span><span class="sxs-lookup"><span data-stu-id="02e03-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="02e03-111">To polecenie pobiera zadania harmonogramu, które są częścią kolekcji zadań o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="02e03-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="02e03-112">Przykład 2: pobieranie nazwanego zadania</span><span class="sxs-lookup"><span data-stu-id="02e03-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="02e03-113">To polecenie pobiera zadanie o nazwie Job01 z kolekcji o nazwie JobCollection01 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="02e03-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="02e03-114">Przykład 3: uzyskiwanie wyłączonych zadań w kolekcji</span><span class="sxs-lookup"><span data-stu-id="02e03-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="02e03-115">To polecenie pobiera wszystkie wyłączone zadania harmonogramu, które są częścią JobCollection01 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="02e03-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="02e03-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02e03-116">PARAMETERS</span></span>

### <span data-ttu-id="02e03-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="02e03-117">-JobCollectionName</span></span>
<span data-ttu-id="02e03-118">Określa nazwę kolekcji zawierającej zadanie harmonogramu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="02e03-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="02e03-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="02e03-119">-JobName</span></span>
<span data-ttu-id="02e03-120">Określa nazwę zadania harmonogramu, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="02e03-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="02e03-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="02e03-121">-JobState</span></span>
<span data-ttu-id="02e03-122">Określa stan zadań harmonogramu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="02e03-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="02e03-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="02e03-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02e03-124">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="02e03-124">Enabled</span></span>
- <span data-ttu-id="02e03-125">Łącza</span><span class="sxs-lookup"><span data-stu-id="02e03-125">Disabled</span></span>
- <span data-ttu-id="02e03-126">Błąd</span><span class="sxs-lookup"><span data-stu-id="02e03-126">Faulted</span></span>
- <span data-ttu-id="02e03-127">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="02e03-127">Completed</span></span>

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

### <span data-ttu-id="02e03-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="02e03-128">-Location</span></span>
<span data-ttu-id="02e03-129">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="02e03-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="02e03-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="02e03-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02e03-131">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="02e03-131">Anywhere Asia</span></span>
- <span data-ttu-id="02e03-132">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="02e03-132">Anywhere Europe</span></span>
- <span data-ttu-id="02e03-133">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="02e03-133">Anywhere US</span></span>
- <span data-ttu-id="02e03-134">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="02e03-134">East Asia</span></span>
- <span data-ttu-id="02e03-135">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="02e03-135">East US</span></span>
- <span data-ttu-id="02e03-136">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="02e03-136">North Central US</span></span>
- <span data-ttu-id="02e03-137">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="02e03-137">North Europe</span></span>
- <span data-ttu-id="02e03-138">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="02e03-138">South Central US</span></span>
- <span data-ttu-id="02e03-139">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="02e03-139">Southeast Asia</span></span>
- <span data-ttu-id="02e03-140">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="02e03-140">West Europe</span></span>
- <span data-ttu-id="02e03-141">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="02e03-141">West US</span></span>

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

### <span data-ttu-id="02e03-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="02e03-142">-Profile</span></span>
<span data-ttu-id="02e03-143">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02e03-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02e03-144">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="02e03-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02e03-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e03-145">CommonParameters</span></span>
<span data-ttu-id="02e03-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e03-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e03-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e03-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e03-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02e03-148">INPUTS</span></span>

## <span data-ttu-id="02e03-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02e03-149">OUTPUTS</span></span>

## <span data-ttu-id="02e03-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02e03-150">NOTES</span></span>

## <span data-ttu-id="02e03-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02e03-151">RELATED LINKS</span></span>

[<span data-ttu-id="02e03-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="02e03-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


