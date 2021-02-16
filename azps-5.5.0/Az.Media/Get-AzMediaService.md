---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187411"
---
# <span data-ttu-id="50b05-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="50b05-101">Get-AzMediaService</span></span>

## <span data-ttu-id="50b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50b05-102">SYNOPSIS</span></span>
<span data-ttu-id="50b05-103">Pobiera informacje o usłudze multimediów.</span><span class="sxs-lookup"><span data-stu-id="50b05-103">Gets information about a media service.</span></span>

## <span data-ttu-id="50b05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50b05-104">SYNTAX</span></span>

### <span data-ttu-id="50b05-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b05-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50b05-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b05-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b05-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="50b05-107">DESCRIPTION</span></span>
<span data-ttu-id="50b05-108">Polecenie **cmdlet Get-AzMediaService** pobiera informacje o usłudze multimediów.</span><span class="sxs-lookup"><span data-stu-id="50b05-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="50b05-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50b05-109">EXAMPLES</span></span>

### <span data-ttu-id="50b05-110">Przykład 1. Uzyskiwanie wszystkich usług multimedialnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="50b05-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="50b05-111">To polecenie pobiera właściwości wszystkich usług multimedialnych w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="50b05-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="50b05-112">Przykład 2. Uzyskiwanie właściwości usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="50b05-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="50b05-113">To polecenie pobiera właściwości usługi multimediów o nazwie MediaService1, która należy do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="50b05-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="50b05-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50b05-114">PARAMETERS</span></span>

### <span data-ttu-id="50b05-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50b05-115">-AccountName</span></span>
<span data-ttu-id="50b05-116">Określa nazwę usługi multimediów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50b05-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="50b05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b05-117">-DefaultProfile</span></span>
<span data-ttu-id="50b05-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50b05-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50b05-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b05-119">-ResourceGroupName</span></span>
<span data-ttu-id="50b05-120">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="50b05-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="50b05-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b05-121">CommonParameters</span></span>
<span data-ttu-id="50b05-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b05-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b05-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b05-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b05-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50b05-124">INPUTS</span></span>

### <span data-ttu-id="50b05-125">System.String</span><span class="sxs-lookup"><span data-stu-id="50b05-125">System.String</span></span>

## <span data-ttu-id="50b05-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50b05-126">OUTPUTS</span></span>

### <span data-ttu-id="50b05-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="50b05-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="50b05-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50b05-128">NOTES</span></span>

## <span data-ttu-id="50b05-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50b05-129">RELATED LINKS</span></span>

[<span data-ttu-id="50b05-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="50b05-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="50b05-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="50b05-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="50b05-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="50b05-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


