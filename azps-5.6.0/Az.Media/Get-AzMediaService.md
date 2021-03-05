---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006625"
---
# <span data-ttu-id="ea9bd-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ea9bd-101">Get-AzMediaService</span></span>

## <span data-ttu-id="ea9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9bd-103">Pobiera informacje o usłudze multimediów.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-103">Gets information about a media service.</span></span>

## <span data-ttu-id="ea9bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea9bd-104">SYNTAX</span></span>

### <span data-ttu-id="ea9bd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea9bd-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9bd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea9bd-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea9bd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea9bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ea9bd-108">Polecenie **cmdlet Get-AzMediaService** pobiera informacje o usłudze multimediów.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="ea9bd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea9bd-109">EXAMPLES</span></span>

### <span data-ttu-id="ea9bd-110">Przykład 1. Uzyskiwanie wszystkich usług multimedialnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ea9bd-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="ea9bd-111">To polecenie pobiera właściwości wszystkich usług multimedialnych w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="ea9bd-112">Przykład 2. Uzyskiwanie właściwości usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="ea9bd-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="ea9bd-113">To polecenie pobiera właściwości usługi multimediów o nazwie MediaService1 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="ea9bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea9bd-114">PARAMETERS</span></span>

### <span data-ttu-id="ea9bd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea9bd-115">-AccountName</span></span>
<span data-ttu-id="ea9bd-116">Określa nazwę usługi multimediów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ea9bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9bd-117">-DefaultProfile</span></span>
<span data-ttu-id="ea9bd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ea9bd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea9bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea9bd-120">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="ea9bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9bd-121">CommonParameters</span></span>
<span data-ttu-id="ea9bd-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9bd-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9bd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9bd-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea9bd-124">INPUTS</span></span>

### <span data-ttu-id="ea9bd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ea9bd-125">System.String</span></span>

## <span data-ttu-id="ea9bd-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea9bd-126">OUTPUTS</span></span>

### <span data-ttu-id="ea9bd-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="ea9bd-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="ea9bd-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea9bd-128">NOTES</span></span>

## <span data-ttu-id="ea9bd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea9bd-129">RELATED LINKS</span></span>

[<span data-ttu-id="ea9bd-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ea9bd-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="ea9bd-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ea9bd-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="ea9bd-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ea9bd-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


