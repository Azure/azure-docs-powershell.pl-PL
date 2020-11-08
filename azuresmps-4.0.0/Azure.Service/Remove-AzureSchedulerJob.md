---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055095"
---
# <span data-ttu-id="1faf1-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1faf1-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="1faf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1faf1-102">SYNOPSIS</span></span>
<span data-ttu-id="1faf1-103">Usuwa zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="1faf1-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="1faf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1faf1-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1faf1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1faf1-105">DESCRIPTION</span></span>
<span data-ttu-id="1faf1-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1faf1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1faf1-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1faf1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1faf1-108">Polecenie cmdlet **Remove-AzureSchedulerJob** usuwa zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="1faf1-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="1faf1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1faf1-109">EXAMPLES</span></span>

### <span data-ttu-id="1faf1-110">Przykład 1: usuwanie zadania harmonogramu</span><span class="sxs-lookup"><span data-stu-id="1faf1-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="1faf1-111">To polecenie usuwa zadanie o nazwie Job17.</span><span class="sxs-lookup"><span data-stu-id="1faf1-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="1faf1-112">To zadanie jest częścią kolekcji zadań o nazwie JobCollection01 i znajduje się w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1faf1-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="1faf1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1faf1-113">PARAMETERS</span></span>

### <span data-ttu-id="1faf1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1faf1-114">-Force</span></span>
<span data-ttu-id="1faf1-115">Wskazuje, że to polecenie cmdlet usuwa zadanie harmonogramu bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1faf1-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1faf1-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1faf1-116">-JobCollectionName</span></span>
<span data-ttu-id="1faf1-117">Określa nazwę kolekcji zawierającej zadanie harmonogramu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1faf1-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="1faf1-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="1faf1-118">-JobName</span></span>
<span data-ttu-id="1faf1-119">Określa nazwę zadania harmonogramu, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="1faf1-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="1faf1-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1faf1-120">-Location</span></span>
<span data-ttu-id="1faf1-121">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="1faf1-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="1faf1-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1faf1-122">Valid values are:</span></span> 

- <span data-ttu-id="1faf1-123">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="1faf1-123">Anywhere Asia</span></span>
- <span data-ttu-id="1faf1-124">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="1faf1-124">Anywhere Europe</span></span>
- <span data-ttu-id="1faf1-125">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="1faf1-125">Anywhere US</span></span>
- <span data-ttu-id="1faf1-126">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="1faf1-126">East Asia</span></span>
- <span data-ttu-id="1faf1-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="1faf1-127">East US</span></span>
- <span data-ttu-id="1faf1-128">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="1faf1-128">North Central US</span></span>
- <span data-ttu-id="1faf1-129">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="1faf1-129">North Europe</span></span>
- <span data-ttu-id="1faf1-130">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="1faf1-130">South Central US</span></span>
- <span data-ttu-id="1faf1-131">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="1faf1-131">Southeast Asia</span></span>
- <span data-ttu-id="1faf1-132">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="1faf1-132">West Europe</span></span>
- <span data-ttu-id="1faf1-133">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="1faf1-133">West US</span></span>

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

### <span data-ttu-id="1faf1-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="1faf1-134">-Profile</span></span>
<span data-ttu-id="1faf1-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faf1-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1faf1-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1faf1-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1faf1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faf1-137">CommonParameters</span></span>
<span data-ttu-id="1faf1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1faf1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faf1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1faf1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faf1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1faf1-140">INPUTS</span></span>

## <span data-ttu-id="1faf1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1faf1-141">OUTPUTS</span></span>

## <span data-ttu-id="1faf1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1faf1-142">NOTES</span></span>

## <span data-ttu-id="1faf1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1faf1-143">RELATED LINKS</span></span>

[<span data-ttu-id="1faf1-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1faf1-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


