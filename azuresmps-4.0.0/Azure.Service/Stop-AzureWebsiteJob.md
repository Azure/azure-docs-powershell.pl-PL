---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054804"
---
# <span data-ttu-id="316f0-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="316f0-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="316f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="316f0-102">SYNOPSIS</span></span>
<span data-ttu-id="316f0-103">Zatrzymuje zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="316f0-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="316f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="316f0-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="316f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="316f0-105">DESCRIPTION</span></span>
<span data-ttu-id="316f0-106">Polecenie cmdlet **stop-AzureWebsiteJob** zatrzymuje zadanie sieci Web dla witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="316f0-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="316f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="316f0-107">EXAMPLES</span></span>

### <span data-ttu-id="316f0-108">Przykład 1: Zatrzymywanie zadania sieci Web dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="316f0-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="316f0-109">Zatrzymuje zadanie sieci Web o nazwie MyWebJob dla witryny Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="316f0-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="316f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="316f0-110">PARAMETERS</span></span>

### <span data-ttu-id="316f0-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="316f0-111">-JobName</span></span>
<span data-ttu-id="316f0-112">Nazwa zadania w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="316f0-112">The web job name.</span></span>

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

### <span data-ttu-id="316f0-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="316f0-113">-Name</span></span>
<span data-ttu-id="316f0-114">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="316f0-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="316f0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="316f0-115">-PassThru</span></span>
<span data-ttu-id="316f0-116">Zwraca wartość logiczną wskazującą, że zadanie zostało pomyślnie zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="316f0-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="316f0-117">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="316f0-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="316f0-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="316f0-118">-Profile</span></span>
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

### <span data-ttu-id="316f0-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="316f0-119">-Slot</span></span>
<span data-ttu-id="316f0-120">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="316f0-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="316f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316f0-121">CommonParameters</span></span>
<span data-ttu-id="316f0-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316f0-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316f0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316f0-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="316f0-124">INPUTS</span></span>

## <span data-ttu-id="316f0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="316f0-125">OUTPUTS</span></span>

## <span data-ttu-id="316f0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="316f0-126">NOTES</span></span>

## <span data-ttu-id="316f0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="316f0-127">RELATED LINKS</span></span>

[<span data-ttu-id="316f0-128">Zatrzymaj — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="316f0-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="316f0-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="316f0-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="316f0-130">Nowe — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="316f0-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="316f0-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="316f0-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="316f0-132">Start — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="316f0-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


