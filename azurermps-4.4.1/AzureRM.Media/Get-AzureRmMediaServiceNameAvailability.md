---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718171"
---
# <span data-ttu-id="4a0ae-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4a0ae-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="4a0ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0ae-103">Sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="4a0ae-104">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a0ae-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a0ae-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="4a0ae-106">Opis</span><span class="sxs-lookup"><span data-stu-id="4a0ae-106">DESCRIPTION</span></span>
<span data-ttu-id="4a0ae-107">Polecenie cmdlet **Get-AzureRmMediaServiceNameAvailability** sprawdza, czy nazwa usługi multimedialnej jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="4a0ae-108">Nazwy usług multimedialnych są globalnie unikatowe.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="4a0ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a0ae-109">EXAMPLES</span></span>

### <span data-ttu-id="4a0ae-110">Przykład 1. Sprawdź, czy nazwa usługi multimedialnej jest dostępna</span><span class="sxs-lookup"><span data-stu-id="4a0ae-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="4a0ae-111">To polecenie sprawdza, czy nazwa MediaService1 jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="4a0ae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a0ae-112">PARAMETERS</span></span>

### <span data-ttu-id="4a0ae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a0ae-113">-AccountName</span></span>
<span data-ttu-id="4a0ae-114">Określa nazwę usługi multimedialnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4a0ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0ae-115">-DefaultProfile</span></span>
<span data-ttu-id="4a0ae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0ae-117">CommonParameters</span></span>
<span data-ttu-id="4a0ae-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0ae-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a0ae-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0ae-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a0ae-120">INPUTS</span></span>

## <span data-ttu-id="4a0ae-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a0ae-121">OUTPUTS</span></span>

### <span data-ttu-id="4a0ae-122">Microsoft. Azure. Commands. Media. models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="4a0ae-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="4a0ae-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a0ae-123">NOTES</span></span>

## <span data-ttu-id="4a0ae-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a0ae-124">RELATED LINKS</span></span>

[<span data-ttu-id="4a0ae-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a0ae-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="4a0ae-126">Nowe — AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a0ae-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="4a0ae-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a0ae-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="4a0ae-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4a0ae-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


