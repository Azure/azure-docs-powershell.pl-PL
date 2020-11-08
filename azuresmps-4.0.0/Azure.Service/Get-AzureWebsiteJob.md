---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055239"
---
# <span data-ttu-id="172e2-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="172e2-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="172e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="172e2-102">SYNOPSIS</span></span>
<span data-ttu-id="172e2-103">Pobiera zadania sieci Web skojarzone z witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="172e2-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="172e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="172e2-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="172e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="172e2-105">DESCRIPTION</span></span>
<span data-ttu-id="172e2-106">Pobiera zadania sieci Web skojarzone z witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="172e2-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="172e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="172e2-107">EXAMPLES</span></span>

### <span data-ttu-id="172e2-108">Przykład 1: uzyskiwanie szczegółowych informacji o zadaniach w sieci Web</span><span class="sxs-lookup"><span data-stu-id="172e2-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="172e2-109">Pobiera zadanie sieci Web o nazwie MyWebJob z gniazda produkcyjnego witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="172e2-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="172e2-110">Przykład 2: pobieranie wszystkich zadań w sieci Web dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="172e2-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="172e2-111">Pobiera wszystkie zadania sieci Web skojarzone z miejscem produkcyjnym witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="172e2-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="172e2-112">Przykład 3: pobieranie wszystkich wyzwolonych zadań w sieci Web</span><span class="sxs-lookup"><span data-stu-id="172e2-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="172e2-113">Pobiera wszystkie wyzwolone zadania sieci Web z miejsca przemieszczenia witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="172e2-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="172e2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="172e2-114">PARAMETERS</span></span>

### <span data-ttu-id="172e2-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="172e2-115">-JobName</span></span>
<span data-ttu-id="172e2-116">Nazwa zadania w sieci Web</span><span class="sxs-lookup"><span data-stu-id="172e2-116">The web job name</span></span>

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

### <span data-ttu-id="172e2-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="172e2-117">-JobType</span></span>
<span data-ttu-id="172e2-118">Typ zadania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="172e2-118">The web job type.</span></span>
<span data-ttu-id="172e2-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="172e2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="172e2-120">Wyzwolon</span><span class="sxs-lookup"><span data-stu-id="172e2-120">Triggered</span></span>
- <span data-ttu-id="172e2-121">Stałego</span><span class="sxs-lookup"><span data-stu-id="172e2-121">Continuous</span></span>

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

### <span data-ttu-id="172e2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="172e2-122">-Name</span></span>
<span data-ttu-id="172e2-123">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="172e2-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="172e2-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="172e2-124">-Profile</span></span>
<span data-ttu-id="172e2-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172e2-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="172e2-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="172e2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="172e2-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="172e2-127">-Slot</span></span>
<span data-ttu-id="172e2-128">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="172e2-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="172e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172e2-129">CommonParameters</span></span>
<span data-ttu-id="172e2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172e2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172e2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172e2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="172e2-132">INPUTS</span></span>

## <span data-ttu-id="172e2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="172e2-133">OUTPUTS</span></span>

## <span data-ttu-id="172e2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="172e2-134">NOTES</span></span>

## <span data-ttu-id="172e2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="172e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="172e2-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="172e2-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="172e2-137">Nowe — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="172e2-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="172e2-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="172e2-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="172e2-139">Start — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="172e2-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="172e2-140">Zatrzymaj — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="172e2-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


