---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054448"
---
# <span data-ttu-id="c3624-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c3624-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="c3624-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3624-102">SYNOPSIS</span></span>
<span data-ttu-id="c3624-103">Usuwa istniejące zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="c3624-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="c3624-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3624-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3624-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3624-105">DESCRIPTION</span></span>
<span data-ttu-id="c3624-106">Usuwa istniejące zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="c3624-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="c3624-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3624-107">EXAMPLES</span></span>

### <span data-ttu-id="c3624-108">Przykład 1. Usuń istniejące zadanie sieci Web dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="c3624-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="c3624-109">Usuwa zadanie sieci Web o nazwie MyWebJob dla witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="c3624-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="c3624-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3624-110">PARAMETERS</span></span>

### <span data-ttu-id="c3624-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c3624-111">-Force</span></span>
<span data-ttu-id="c3624-112">Wskazuje, że to polecenie cmdlet usunie zadanie sieci Web bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3624-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c3624-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c3624-113">-JobName</span></span>
<span data-ttu-id="c3624-114">Nazwa zadania w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3624-114">The web job name.</span></span>

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

### <span data-ttu-id="c3624-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="c3624-115">-JobType</span></span>
<span data-ttu-id="c3624-116">Typ zadania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3624-116">The web job type.</span></span>
<span data-ttu-id="c3624-117">Można uruchamiać lub powodować ciągłość.</span><span class="sxs-lookup"><span data-stu-id="c3624-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="c3624-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3624-118">-Name</span></span>
<span data-ttu-id="c3624-119">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c3624-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="c3624-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3624-120">-Profile</span></span>
<span data-ttu-id="c3624-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3624-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3624-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c3624-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3624-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="c3624-123">-Slot</span></span>
<span data-ttu-id="c3624-124">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c3624-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="c3624-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3624-125">CommonParameters</span></span>
<span data-ttu-id="c3624-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3624-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3624-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3624-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3624-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3624-128">INPUTS</span></span>

## <span data-ttu-id="c3624-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3624-129">OUTPUTS</span></span>

## <span data-ttu-id="c3624-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3624-130">NOTES</span></span>

## <span data-ttu-id="c3624-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3624-131">RELATED LINKS</span></span>

[<span data-ttu-id="c3624-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c3624-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="c3624-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c3624-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="c3624-134">Nowe — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c3624-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="c3624-135">Start — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c3624-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="c3624-136">Zatrzymaj — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="c3624-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


