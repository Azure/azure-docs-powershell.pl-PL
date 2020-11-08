---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055149"
---
# <span data-ttu-id="26b2f-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="26b2f-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="26b2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="26b2f-103">Tworzy zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="26b2f-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="26b2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26b2f-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26b2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="26b2f-106">Polecenie cmdlet **New-AzureWebsiteJob** tworzy zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="26b2f-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="26b2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="26b2f-108">Przykład 1: Tworzenie nowego zadania sieci Web dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="26b2f-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="26b2f-109">Tworzy ciągłe zadanie w celu nawiązania połączenia job.bat w witrynie internetowej Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="26b2f-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="26b2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="26b2f-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="26b2f-111">-JobFile</span></span>
<span data-ttu-id="26b2f-112">Plik zadania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="26b2f-112">The web job file.</span></span>

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

### <span data-ttu-id="26b2f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="26b2f-113">-JobName</span></span>
<span data-ttu-id="26b2f-114">Nazwa zadania w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="26b2f-114">The web job name.</span></span>

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

### <span data-ttu-id="26b2f-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="26b2f-115">-JobType</span></span>
<span data-ttu-id="26b2f-116">Typ zadania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="26b2f-116">The web job type.</span></span>
<span data-ttu-id="26b2f-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b2f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26b2f-118">Wyzwolon</span><span class="sxs-lookup"><span data-stu-id="26b2f-118">Triggered</span></span> 
- <span data-ttu-id="26b2f-119">Stałego</span><span class="sxs-lookup"><span data-stu-id="26b2f-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b2f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26b2f-120">-Name</span></span>
<span data-ttu-id="26b2f-121">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="26b2f-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="26b2f-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="26b2f-122">-Profile</span></span>
<span data-ttu-id="26b2f-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b2f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26b2f-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="26b2f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26b2f-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="26b2f-125">-Slot</span></span>
<span data-ttu-id="26b2f-126">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="26b2f-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="26b2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b2f-127">CommonParameters</span></span>
<span data-ttu-id="26b2f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b2f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b2f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b2f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b2f-130">INPUTS</span></span>

## <span data-ttu-id="26b2f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26b2f-131">OUTPUTS</span></span>

## <span data-ttu-id="26b2f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26b2f-132">NOTES</span></span>

## <span data-ttu-id="26b2f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26b2f-133">RELATED LINKS</span></span>

[<span data-ttu-id="26b2f-134">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="26b2f-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="26b2f-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="26b2f-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="26b2f-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="26b2f-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="26b2f-137">Start — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="26b2f-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="26b2f-138">Zatrzymaj — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="26b2f-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


