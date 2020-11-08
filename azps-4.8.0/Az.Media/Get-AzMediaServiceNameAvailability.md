---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222468"
---
# <span data-ttu-id="e59de-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e59de-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="e59de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e59de-102">SYNOPSIS</span></span>
<span data-ttu-id="e59de-103">Sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="e59de-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="e59de-104">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="e59de-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="e59de-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e59de-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="e59de-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e59de-106">DESCRIPTION</span></span>
<span data-ttu-id="e59de-107">Polecenie cmdlet **Get-AzMediaServiceNameAvailability** sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="e59de-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="e59de-108">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="e59de-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="e59de-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e59de-109">EXAMPLES</span></span>

### <span data-ttu-id="e59de-110">Przykład 1. Sprawdź, czy nazwa usługi multimedialnej jest dostępna</span><span class="sxs-lookup"><span data-stu-id="e59de-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="e59de-111">To polecenie sprawdza, czy nazwa MediaService1 jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="e59de-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="e59de-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e59de-112">PARAMETERS</span></span>

### <span data-ttu-id="e59de-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e59de-113">-AccountName</span></span>
<span data-ttu-id="e59de-114">Określa nazwę usługi multimedialnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e59de-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e59de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59de-115">-DefaultProfile</span></span>
<span data-ttu-id="e59de-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e59de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e59de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59de-117">CommonParameters</span></span>
<span data-ttu-id="e59de-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59de-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e59de-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59de-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e59de-120">INPUTS</span></span>

### <span data-ttu-id="e59de-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e59de-121">None</span></span>

## <span data-ttu-id="e59de-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e59de-122">OUTPUTS</span></span>

### <span data-ttu-id="e59de-123">Microsoft. Azure. Commands. Media. models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="e59de-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="e59de-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e59de-124">NOTES</span></span>

## <span data-ttu-id="e59de-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e59de-125">RELATED LINKS</span></span>

[<span data-ttu-id="e59de-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e59de-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="e59de-127">Nowe — AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e59de-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="e59de-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e59de-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="e59de-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e59de-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


