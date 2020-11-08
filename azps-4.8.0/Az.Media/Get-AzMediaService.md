---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222473"
---
# <span data-ttu-id="5e7b8-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5e7b8-101">Get-AzMediaService</span></span>

## <span data-ttu-id="5e7b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7b8-103">Pobiera informacje o usłudze multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-103">Gets information about a media service.</span></span>

## <span data-ttu-id="5e7b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e7b8-104">SYNTAX</span></span>

### <span data-ttu-id="5e7b8-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e7b8-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e7b8-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e7b8-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e7b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5e7b8-107">DESCRIPTION</span></span>
<span data-ttu-id="5e7b8-108">Polecenie cmdlet **Get-AzMediaService** pobiera informacje o usłudze multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="5e7b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e7b8-109">EXAMPLES</span></span>

### <span data-ttu-id="5e7b8-110">Przykład 1: pobieranie wszystkich usług multimedialnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="5e7b8-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="5e7b8-111">To polecenie pobiera właściwości wszystkich usług multimedialnych w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="5e7b8-112">Przykład 2: Uzyskaj właściwości usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="5e7b8-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="5e7b8-113">To polecenie pobiera właściwości usługi multimediów o nazwie MediaService1 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="5e7b8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e7b8-114">PARAMETERS</span></span>

### <span data-ttu-id="5e7b8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e7b8-115">-AccountName</span></span>
<span data-ttu-id="5e7b8-116">Określa nazwę usługi multimedialnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7b8-117">-DefaultProfile</span></span>
<span data-ttu-id="5e7b8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5e7b8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e7b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e7b8-120">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7b8-121">CommonParameters</span></span>
<span data-ttu-id="5e7b8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7b8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7b8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7b8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e7b8-124">INPUTS</span></span>

### <span data-ttu-id="5e7b8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5e7b8-125">System.String</span></span>

## <span data-ttu-id="5e7b8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e7b8-126">OUTPUTS</span></span>

### <span data-ttu-id="5e7b8-127">Microsoft. Azure. Commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="5e7b8-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="5e7b8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e7b8-128">NOTES</span></span>

## <span data-ttu-id="5e7b8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e7b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="5e7b8-130">Nowe — AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5e7b8-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="5e7b8-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5e7b8-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="5e7b8-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5e7b8-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


