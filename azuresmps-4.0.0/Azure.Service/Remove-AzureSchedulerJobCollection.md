---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055094"
---
# <span data-ttu-id="7ac94-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7ac94-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="7ac94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ac94-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac94-103">Usuwa kolekcję zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="7ac94-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="7ac94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ac94-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7ac94-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ac94-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac94-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac94-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7ac94-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7ac94-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7ac94-108">Polecenie cmdlet **Remove-AzureSchedulerJobCollection** usuwa kolekcję zadań harmonogramu i wszystkie zadania w ramach tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="7ac94-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="7ac94-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ac94-109">EXAMPLES</span></span>

### <span data-ttu-id="7ac94-110">Przykład 1: usuwanie kolekcji zadań dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="7ac94-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="7ac94-111">To polecenie usuwa kolekcję zadań harmonogramu o nazwie JobCollection01 w Północnej, centralnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7ac94-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="7ac94-112">Polecenie usuwa również zadania w obszarze JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="7ac94-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="7ac94-113">Przykład 2: usuwanie lokalizacji zadania</span><span class="sxs-lookup"><span data-stu-id="7ac94-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="7ac94-114">To polecenie usuwa kolekcję zadań harmonogramu o nazwie JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="7ac94-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="7ac94-115">Polecenie usuwa również zadania w obszarze JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="7ac94-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="7ac94-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ac94-116">PARAMETERS</span></span>

### <span data-ttu-id="7ac94-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7ac94-117">-Force</span></span>
<span data-ttu-id="7ac94-118">Wskazuje, że to polecenie cmdlet usunie kolekcję zadań harmonogramu bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ac94-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7ac94-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7ac94-119">-JobCollectionName</span></span>
<span data-ttu-id="7ac94-120">Określa nazwę kolekcji zadań harmonogramu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7ac94-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="7ac94-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7ac94-121">-Location</span></span>
<span data-ttu-id="7ac94-122">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="7ac94-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="7ac94-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7ac94-123">Valid values are:</span></span> 

- <span data-ttu-id="7ac94-124">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="7ac94-124">Anywhere Asia</span></span>
- <span data-ttu-id="7ac94-125">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="7ac94-125">Anywhere Europe</span></span>
- <span data-ttu-id="7ac94-126">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="7ac94-126">Anywhere US</span></span>
- <span data-ttu-id="7ac94-127">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="7ac94-127">East Asia</span></span>
- <span data-ttu-id="7ac94-128">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="7ac94-128">East US</span></span>
- <span data-ttu-id="7ac94-129">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="7ac94-129">North Central US</span></span>
- <span data-ttu-id="7ac94-130">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="7ac94-130">North Europe</span></span>
- <span data-ttu-id="7ac94-131">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="7ac94-131">South Central US</span></span>
- <span data-ttu-id="7ac94-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="7ac94-132">Southeast Asia</span></span>
- <span data-ttu-id="7ac94-133">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="7ac94-133">West Europe</span></span>
- <span data-ttu-id="7ac94-134">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="7ac94-134">West US</span></span>

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

### <span data-ttu-id="7ac94-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="7ac94-135">-Profile</span></span>
<span data-ttu-id="7ac94-136">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac94-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ac94-137">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7ac94-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ac94-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac94-138">CommonParameters</span></span>
<span data-ttu-id="7ac94-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac94-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac94-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac94-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac94-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac94-141">INPUTS</span></span>

## <span data-ttu-id="7ac94-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ac94-142">OUTPUTS</span></span>

## <span data-ttu-id="7ac94-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ac94-143">NOTES</span></span>

## <span data-ttu-id="7ac94-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac94-144">RELATED LINKS</span></span>

[<span data-ttu-id="7ac94-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7ac94-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="7ac94-146">Nowe — AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7ac94-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="7ac94-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7ac94-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


