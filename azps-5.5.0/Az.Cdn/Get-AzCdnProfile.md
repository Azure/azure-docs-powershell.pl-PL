---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181851"
---
# <span data-ttu-id="cbf45-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="cbf45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf45-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf45-103">Pobiera profil CDN.</span><span class="sxs-lookup"><span data-stu-id="cbf45-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="cbf45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbf45-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbf45-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbf45-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf45-106">Polecenie **cmdlet Get-AzCdnProfile** pobiera profil usługi Azure Content Delivery Network (CDN) i powiązane z nim informacje.</span><span class="sxs-lookup"><span data-stu-id="cbf45-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="cbf45-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbf45-107">EXAMPLES</span></span>

## <span data-ttu-id="cbf45-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbf45-108">PARAMETERS</span></span>

### <span data-ttu-id="cbf45-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-109">-DefaultProfile</span></span>
<span data-ttu-id="cbf45-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cbf45-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbf45-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cbf45-111">-ProfileName</span></span>
<span data-ttu-id="cbf45-112">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="cbf45-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="cbf45-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf45-113">-ResourceGroupName</span></span>
<span data-ttu-id="cbf45-114">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="cbf45-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="cbf45-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf45-115">CommonParameters</span></span>
<span data-ttu-id="cbf45-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf45-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf45-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbf45-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf45-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbf45-118">INPUTS</span></span>

### <span data-ttu-id="cbf45-119">System.String</span><span class="sxs-lookup"><span data-stu-id="cbf45-119">System.String</span></span>

## <span data-ttu-id="cbf45-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbf45-120">OUTPUTS</span></span>

### <span data-ttu-id="cbf45-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cbf45-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbf45-122">NOTES</span></span>

## <span data-ttu-id="cbf45-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbf45-123">RELATED LINKS</span></span>

[<span data-ttu-id="cbf45-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="cbf45-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="cbf45-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbf45-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


