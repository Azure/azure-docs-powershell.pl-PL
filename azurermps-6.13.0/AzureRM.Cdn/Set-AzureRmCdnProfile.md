---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547516"
---
# <span data-ttu-id="eeef9-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="eeef9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eeef9-102">SYNOPSIS</span></span>
<span data-ttu-id="eeef9-103">Aktualizuje profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="eeef9-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeef9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eeef9-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeef9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eeef9-105">DESCRIPTION</span></span>
<span data-ttu-id="eeef9-106">Polecenie cmdlet **Set-AzureRmCdnProfile** aktualizuje profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="eeef9-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="eeef9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eeef9-107">EXAMPLES</span></span>

## <span data-ttu-id="eeef9-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eeef9-108">PARAMETERS</span></span>

### <span data-ttu-id="eeef9-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-109">-CdnProfile</span></span>
<span data-ttu-id="eeef9-110">Określa profil, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeef9-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="eeef9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-111">-DefaultProfile</span></span>
<span data-ttu-id="eeef9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eeef9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeef9-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eeef9-113">-Confirm</span></span>
<span data-ttu-id="eeef9-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeef9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeef9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeef9-115">-WhatIf</span></span>
<span data-ttu-id="eeef9-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeef9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeef9-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eeef9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeef9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeef9-118">CommonParameters</span></span>
<span data-ttu-id="eeef9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeef9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeef9-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeef9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeef9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eeef9-121">INPUTS</span></span>

### <span data-ttu-id="eeef9-122">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="eeef9-123">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eeef9-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="eeef9-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eeef9-124">OUTPUTS</span></span>

### <span data-ttu-id="eeef9-125">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="eeef9-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eeef9-126">NOTES</span></span>

## <span data-ttu-id="eeef9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eeef9-127">RELATED LINKS</span></span>

[<span data-ttu-id="eeef9-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="eeef9-129">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="eeef9-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeef9-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


