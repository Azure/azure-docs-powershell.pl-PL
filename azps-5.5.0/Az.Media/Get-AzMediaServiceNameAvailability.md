---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241235"
---
# <span data-ttu-id="2d327-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2d327-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="2d327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d327-102">SYNOPSIS</span></span>
<span data-ttu-id="2d327-103">Sprawdza, czy nazwa usługi multimediów jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="2d327-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="2d327-104">Nazwy usług multimedialnych są unikatowe globalnie.</span><span class="sxs-lookup"><span data-stu-id="2d327-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="2d327-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d327-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="2d327-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d327-106">DESCRIPTION</span></span>
<span data-ttu-id="2d327-107">Polecenie **cmdlet Get-AzMediaServiceNameAvailability** sprawdza, czy nazwa usługi multimediów jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="2d327-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="2d327-108">Nazwy usług multimedialnych są unikatowe globalnie.</span><span class="sxs-lookup"><span data-stu-id="2d327-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="2d327-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d327-109">EXAMPLES</span></span>

### <span data-ttu-id="2d327-110">Przykład 1. Sprawdzanie, czy nazwa usługi multimediów jest dostępna</span><span class="sxs-lookup"><span data-stu-id="2d327-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="2d327-111">To polecenie sprawdza, czy nazwa MediaService1 jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="2d327-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="2d327-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d327-112">PARAMETERS</span></span>

### <span data-ttu-id="2d327-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d327-113">-AccountName</span></span>
<span data-ttu-id="2d327-114">Określa nazwę usługi multimediów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d327-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2d327-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d327-115">-DefaultProfile</span></span>
<span data-ttu-id="2d327-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2d327-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d327-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d327-117">CommonParameters</span></span>
<span data-ttu-id="2d327-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d327-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d327-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d327-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d327-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d327-120">INPUTS</span></span>

### <span data-ttu-id="2d327-121">Brak</span><span class="sxs-lookup"><span data-stu-id="2d327-121">None</span></span>

## <span data-ttu-id="2d327-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d327-122">OUTPUTS</span></span>

### <span data-ttu-id="2d327-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="2d327-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="2d327-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d327-124">NOTES</span></span>

## <span data-ttu-id="2d327-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d327-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d327-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d327-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="2d327-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d327-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="2d327-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d327-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="2d327-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d327-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


