---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975498"
---
# <span data-ttu-id="87e4e-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="87e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="87e4e-103">Aktualizuje profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="87e4e-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="87e4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87e4e-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87e4e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="87e4e-106">Polecenie **cmdlet Set-AzCdnProfile** aktualizuje profil usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="87e4e-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="87e4e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87e4e-107">EXAMPLES</span></span>

## <span data-ttu-id="87e4e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87e4e-108">PARAMETERS</span></span>

### <span data-ttu-id="87e4e-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-109">-CdnProfile</span></span>
<span data-ttu-id="87e4e-110">Określa profil, który będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87e4e-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-111">-DefaultProfile</span></span>
<span data-ttu-id="87e4e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="87e4e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87e4e-113">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87e4e-113">-Confirm</span></span>
<span data-ttu-id="87e4e-114">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87e4e-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e4e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e4e-115">-WhatIf</span></span>
<span data-ttu-id="87e4e-116">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87e4e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e4e-117">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87e4e-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e4e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e4e-118">CommonParameters</span></span>
<span data-ttu-id="87e4e-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e4e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e4e-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87e4e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e4e-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87e4e-121">INPUTS</span></span>

### <span data-ttu-id="87e4e-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="87e4e-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87e4e-123">OUTPUTS</span></span>

### <span data-ttu-id="87e4e-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="87e4e-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87e4e-125">NOTES</span></span>

## <span data-ttu-id="87e4e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87e4e-126">RELATED LINKS</span></span>

[<span data-ttu-id="87e4e-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="87e4e-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="87e4e-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87e4e-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


