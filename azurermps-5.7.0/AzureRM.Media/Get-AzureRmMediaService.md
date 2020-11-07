---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717513"
---
# <span data-ttu-id="090ee-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="090ee-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="090ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="090ee-102">SYNOPSIS</span></span>
<span data-ttu-id="090ee-103">Pobiera informacje o usłudze multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="090ee-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="090ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="090ee-104">SYNTAX</span></span>

### <span data-ttu-id="090ee-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="090ee-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="090ee-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="090ee-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="090ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="090ee-107">DESCRIPTION</span></span>
<span data-ttu-id="090ee-108">Polecenie cmdlet **Get-AzureRmMediaService** pobiera informacje o usłudze multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="090ee-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="090ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="090ee-109">EXAMPLES</span></span>

### <span data-ttu-id="090ee-110">Przykład 1: pobieranie wszystkich usług multimedialnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="090ee-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="090ee-111">To polecenie pobiera właściwości wszystkich usług multimedialnych w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="090ee-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="090ee-112">Przykład 2: Uzyskaj właściwości usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="090ee-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="090ee-113">To polecenie pobiera właściwości usługi multimediów o nazwie MediaService1 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="090ee-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="090ee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="090ee-114">PARAMETERS</span></span>

### <span data-ttu-id="090ee-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="090ee-115">-AccountName</span></span>
<span data-ttu-id="090ee-116">Określa nazwę usługi multimedialnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="090ee-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090ee-117">-DefaultProfile</span></span>
<span data-ttu-id="090ee-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="090ee-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="090ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="090ee-120">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="090ee-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090ee-121">CommonParameters</span></span>
<span data-ttu-id="090ee-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="090ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090ee-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090ee-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="090ee-124">INPUTS</span></span>

### <span data-ttu-id="090ee-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="090ee-125">None</span></span>
<span data-ttu-id="090ee-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="090ee-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="090ee-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="090ee-127">OUTPUTS</span></span>

### <span data-ttu-id="090ee-128">Microsoft. Azure. Commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="090ee-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="090ee-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="090ee-129">NOTES</span></span>

## <span data-ttu-id="090ee-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="090ee-130">RELATED LINKS</span></span>

[<span data-ttu-id="090ee-131">Nowe — AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="090ee-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="090ee-132">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="090ee-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="090ee-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="090ee-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


