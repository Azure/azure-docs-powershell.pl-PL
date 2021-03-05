---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963297"
---
# <span data-ttu-id="6f0c0-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="6f0c0-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="6f0c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0c0-103">Pobiera adres URL logowania pojedynczego profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="6f0c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6f0c0-104">SYNTAX</span></span>

### <span data-ttu-id="6f0c0-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6f0c0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0c0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f0c0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f0c0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6f0c0-107">DESCRIPTION</span></span>
<span data-ttu-id="6f0c0-108">Polecenie **cmdlet Get-AzCdnProfileSsoUrl** pobiera adres URL logowania jednokrotnego profilu usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="6f0c0-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="6f0c0-109">Ten adres URL umożliwia użytkownikom łączenie się z portalem uzupełniającym i korzystanie z dodatkowych funkcji sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="6f0c0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6f0c0-110">EXAMPLES</span></span>

## <span data-ttu-id="6f0c0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f0c0-111">PARAMETERS</span></span>

### <span data-ttu-id="6f0c0-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="6f0c0-112">-CdnProfile</span></span>
<span data-ttu-id="6f0c0-113">Określa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f0c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0c0-114">-DefaultProfile</span></span>
<span data-ttu-id="6f0c0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6f0c0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f0c0-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6f0c0-116">-ProfileName</span></span>
<span data-ttu-id="6f0c0-117">Określa nazwę profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f0c0-118">-ResourceGroupName</span></span>
<span data-ttu-id="6f0c0-119">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0c0-120">CommonParameters</span></span>
<span data-ttu-id="6f0c0-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0c0-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f0c0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0c0-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f0c0-123">INPUTS</span></span>

### <span data-ttu-id="6f0c0-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="6f0c0-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="6f0c0-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f0c0-125">OUTPUTS</span></span>

### <span data-ttu-id="6f0c0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="6f0c0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="6f0c0-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6f0c0-127">NOTES</span></span>

## <span data-ttu-id="6f0c0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f0c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="6f0c0-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="6f0c0-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


