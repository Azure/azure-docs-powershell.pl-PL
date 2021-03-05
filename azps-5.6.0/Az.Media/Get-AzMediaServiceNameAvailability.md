---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d8928aea539910751c61ad03f5e5a4d67188e371
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960465"
---
# <span data-ttu-id="8d160-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8d160-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="8d160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d160-102">SYNOPSIS</span></span>
<span data-ttu-id="8d160-103">Sprawdza, czy nazwa usługi multimediów jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="8d160-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="8d160-104">Nazwy usług multimedialnych są unikatowe globalnie.</span><span class="sxs-lookup"><span data-stu-id="8d160-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="8d160-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d160-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="8d160-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d160-106">DESCRIPTION</span></span>
<span data-ttu-id="8d160-107">Polecenie **cmdlet Get-AzMediaServiceNameAvailability** sprawdza, czy nazwa usługi multimediów jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="8d160-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="8d160-108">Nazwy usług multimedialnych są unikatowe globalnie.</span><span class="sxs-lookup"><span data-stu-id="8d160-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="8d160-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d160-109">EXAMPLES</span></span>

### <span data-ttu-id="8d160-110">Przykład 1. Sprawdzanie, czy nazwa usługi multimediów jest dostępna</span><span class="sxs-lookup"><span data-stu-id="8d160-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="8d160-111">To polecenie sprawdza, czy nazwa MediaService1 jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="8d160-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="8d160-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d160-112">PARAMETERS</span></span>

### <span data-ttu-id="8d160-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d160-113">-AccountName</span></span>
<span data-ttu-id="8d160-114">Określa nazwę usługi multimediów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d160-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d160-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d160-115">-DefaultProfile</span></span>
<span data-ttu-id="8d160-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8d160-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d160-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d160-117">CommonParameters</span></span>
<span data-ttu-id="8d160-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d160-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d160-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d160-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d160-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d160-120">INPUTS</span></span>

### <span data-ttu-id="8d160-121">Brak</span><span class="sxs-lookup"><span data-stu-id="8d160-121">None</span></span>

## <span data-ttu-id="8d160-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d160-122">OUTPUTS</span></span>

### <span data-ttu-id="8d160-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="8d160-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="8d160-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d160-124">NOTES</span></span>

## <span data-ttu-id="8d160-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d160-125">RELATED LINKS</span></span>

[<span data-ttu-id="8d160-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d160-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="8d160-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d160-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="8d160-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d160-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="8d160-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d160-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


