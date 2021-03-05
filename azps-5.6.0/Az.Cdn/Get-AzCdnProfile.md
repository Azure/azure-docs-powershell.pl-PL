---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: e82e455d603ca4fd5d577e18337c93a2368fbcf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004609"
---
# <span data-ttu-id="12630-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="12630-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="12630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12630-102">SYNOPSIS</span></span>
<span data-ttu-id="12630-103">Pobiera profil CDN.</span><span class="sxs-lookup"><span data-stu-id="12630-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="12630-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12630-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12630-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="12630-105">DESCRIPTION</span></span>
<span data-ttu-id="12630-106">Polecenie **cmdlet Get-AzCdnProfile** pobiera profil usługi Azure Content Delivery Network (CDN) i powiązane z nim informacje.</span><span class="sxs-lookup"><span data-stu-id="12630-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="12630-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12630-107">EXAMPLES</span></span>

## <span data-ttu-id="12630-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12630-108">PARAMETERS</span></span>

### <span data-ttu-id="12630-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12630-109">-DefaultProfile</span></span>
<span data-ttu-id="12630-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="12630-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12630-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="12630-111">-ProfileName</span></span>
<span data-ttu-id="12630-112">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="12630-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12630-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12630-113">-ResourceGroupName</span></span>
<span data-ttu-id="12630-114">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="12630-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12630-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12630-115">CommonParameters</span></span>
<span data-ttu-id="12630-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12630-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12630-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12630-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12630-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12630-118">INPUTS</span></span>

### <span data-ttu-id="12630-119">System.String</span><span class="sxs-lookup"><span data-stu-id="12630-119">System.String</span></span>

## <span data-ttu-id="12630-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12630-120">OUTPUTS</span></span>

### <span data-ttu-id="12630-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="12630-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="12630-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12630-122">NOTES</span></span>

## <span data-ttu-id="12630-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12630-123">RELATED LINKS</span></span>

[<span data-ttu-id="12630-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="12630-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="12630-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="12630-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="12630-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="12630-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


