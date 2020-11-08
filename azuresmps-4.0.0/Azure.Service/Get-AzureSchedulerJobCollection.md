---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054578"
---
# <span data-ttu-id="98fd3-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="98fd3-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="98fd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="98fd3-103">Pobiera kolekcje zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="98fd3-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="98fd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98fd3-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="98fd3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="98fd3-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98fd3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="98fd3-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="98fd3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="98fd3-108">Polecenie cmdlet **Get-AzureSchedulerJobCollection** pobiera co najmniej jedno kolekcje zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="98fd3-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="98fd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98fd3-109">EXAMPLES</span></span>

### <span data-ttu-id="98fd3-110">Przykład 1. Pobierz wszystkie kolekcje</span><span class="sxs-lookup"><span data-stu-id="98fd3-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="98fd3-111">To polecenie pobiera wszystkie kolekcje zadań harmonogramu we wszystkich lokalizacjach w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="98fd3-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="98fd3-112">Przykład 2: pobieranie wszystkich kolekcji dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="98fd3-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="98fd3-113">To polecenie pobiera wszystkie kolekcje zadań harmonogramu w lokalizacji o nazwie My Central Północna.</span><span class="sxs-lookup"><span data-stu-id="98fd3-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="98fd3-114">Przykład 3: uzyskiwanie kolekcji przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="98fd3-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="98fd3-115">To polecenie pobiera kolekcję zadań harmonogramu o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="98fd3-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="98fd3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98fd3-116">PARAMETERS</span></span>

### <span data-ttu-id="98fd3-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="98fd3-117">-JobCollectionName</span></span>
<span data-ttu-id="98fd3-118">Określa nazwę kolekcji zadań harmonogramu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="98fd3-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="98fd3-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98fd3-119">-Location</span></span>
<span data-ttu-id="98fd3-120">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="98fd3-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="98fd3-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="98fd3-121">Valid values are:</span></span> 

- <span data-ttu-id="98fd3-122">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="98fd3-122">Anywhere Asia</span></span>
- <span data-ttu-id="98fd3-123">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="98fd3-123">Anywhere Europe</span></span>
- <span data-ttu-id="98fd3-124">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="98fd3-124">Anywhere US</span></span>
- <span data-ttu-id="98fd3-125">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="98fd3-125">East Asia</span></span>
- <span data-ttu-id="98fd3-126">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="98fd3-126">East US</span></span>
- <span data-ttu-id="98fd3-127">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="98fd3-127">North Central US</span></span>
- <span data-ttu-id="98fd3-128">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="98fd3-128">North Europe</span></span>
- <span data-ttu-id="98fd3-129">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="98fd3-129">South Central US</span></span>
- <span data-ttu-id="98fd3-130">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="98fd3-130">Southeast Asia</span></span>
- <span data-ttu-id="98fd3-131">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="98fd3-131">West Europe</span></span>
- <span data-ttu-id="98fd3-132">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="98fd3-132">West US</span></span>

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

### <span data-ttu-id="98fd3-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="98fd3-133">-Profile</span></span>
<span data-ttu-id="98fd3-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98fd3-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98fd3-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="98fd3-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98fd3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fd3-136">CommonParameters</span></span>
<span data-ttu-id="98fd3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fd3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fd3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98fd3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fd3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98fd3-139">INPUTS</span></span>

## <span data-ttu-id="98fd3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98fd3-140">OUTPUTS</span></span>

## <span data-ttu-id="98fd3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98fd3-141">NOTES</span></span>

## <span data-ttu-id="98fd3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98fd3-142">RELATED LINKS</span></span>

[<span data-ttu-id="98fd3-143">Nowe — AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="98fd3-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="98fd3-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="98fd3-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="98fd3-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="98fd3-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


