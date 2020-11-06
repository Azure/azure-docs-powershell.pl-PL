---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: 8de8b9f389f8d57d844c17d92dd492390fbf1884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527890"
---
# <span data-ttu-id="d7145-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d7145-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="d7145-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7145-102">SYNOPSIS</span></span>
<span data-ttu-id="d7145-103">Sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="d7145-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="d7145-104">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="d7145-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7145-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7145-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d7145-106">Opis</span><span class="sxs-lookup"><span data-stu-id="d7145-106">DESCRIPTION</span></span>
<span data-ttu-id="d7145-107">Polecenie cmdlet **Get-AzureRmMediaServiceNameAvailability** sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="d7145-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="d7145-108">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="d7145-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="d7145-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7145-109">EXAMPLES</span></span>

### <span data-ttu-id="d7145-110">Przykład 1. Sprawdź, czy nazwa usługi multimedialnej jest dostępna</span><span class="sxs-lookup"><span data-stu-id="d7145-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="d7145-111">To polecenie sprawdza, czy nazwa MediaService1 jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="d7145-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="d7145-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7145-112">PARAMETERS</span></span>

### <span data-ttu-id="d7145-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7145-113">-AccountName</span></span>
<span data-ttu-id="d7145-114">Określa nazwę usługi multimedialnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7145-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7145-115">-DefaultProfile</span></span>
<span data-ttu-id="d7145-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7145-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7145-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7145-117">CommonParameters</span></span>
<span data-ttu-id="d7145-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7145-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7145-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7145-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7145-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7145-120">INPUTS</span></span>

### <span data-ttu-id="d7145-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7145-121">None</span></span>

## <span data-ttu-id="d7145-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7145-122">OUTPUTS</span></span>

### <span data-ttu-id="d7145-123">Microsoft. Azure. Commands. Media. models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="d7145-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="d7145-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7145-124">NOTES</span></span>

## <span data-ttu-id="d7145-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7145-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7145-126">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d7145-126">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="d7145-127">Nowe — AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d7145-127">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="d7145-128">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d7145-128">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="d7145-129">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d7145-129">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


