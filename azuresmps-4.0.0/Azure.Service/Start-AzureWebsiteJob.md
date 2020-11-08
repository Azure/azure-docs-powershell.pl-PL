---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054733"
---
# <span data-ttu-id="c6dc4-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c6dc4-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="c6dc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6dc4-103">Rozpoczynanie zadania sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="c6dc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6dc4-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6dc4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c6dc4-106">Polecenie cmdlet **Start-AzureWebsiteJob** uruchamia zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="c6dc4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="c6dc4-108">Przykład 1. Rozpoczynanie zadania sieci Web dla witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="c6dc4-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="c6dc4-109">Rozpoczyna zadanie sieci Web o nazwie MyWebJob dla witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="c6dc4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="c6dc4-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="c6dc4-111">-JobName</span></span>
<span data-ttu-id="c6dc4-112">Nazwa zadania w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-112">The web job name.</span></span>

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

### <span data-ttu-id="c6dc4-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="c6dc4-113">-JobType</span></span>
<span data-ttu-id="c6dc4-114">Typ zadania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-114">The web job type.</span></span>
<span data-ttu-id="c6dc4-115">Można uruchamiać lub powodować ciągłość.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="c6dc4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6dc4-116">-Name</span></span>
<span data-ttu-id="c6dc4-117">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="c6dc4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6dc4-118">-PassThru</span></span>
<span data-ttu-id="c6dc4-119">Zwraca wartość logiczną wskazującą, że zadanie zostało pomyślnie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="c6dc4-120">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="c6dc4-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6dc4-121">-Profile</span></span>
<span data-ttu-id="c6dc4-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6dc4-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6dc4-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="c6dc4-124">-Slot</span></span>
<span data-ttu-id="c6dc4-125">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="c6dc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6dc4-126">CommonParameters</span></span>
<span data-ttu-id="c6dc4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6dc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6dc4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6dc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6dc4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6dc4-129">INPUTS</span></span>

## <span data-ttu-id="c6dc4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6dc4-130">OUTPUTS</span></span>

## <span data-ttu-id="c6dc4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6dc4-131">NOTES</span></span>

## <span data-ttu-id="c6dc4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6dc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6dc4-133">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c6dc4-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="c6dc4-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c6dc4-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="c6dc4-135">Nowe — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c6dc4-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="c6dc4-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c6dc4-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="c6dc4-137">Start — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c6dc4-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


