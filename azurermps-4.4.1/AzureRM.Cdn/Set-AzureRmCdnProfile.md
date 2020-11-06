---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 8e294b457d93c5e9aeb9f8391fccdedc3ccfd778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547015"
---
# <span data-ttu-id="ca709-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="ca709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca709-102">SYNOPSIS</span></span>
<span data-ttu-id="ca709-103">Aktualizuje profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ca709-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca709-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca709-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca709-105">DESCRIPTION</span></span>
<span data-ttu-id="ca709-106">Polecenie cmdlet **Set-AzureRmCdnProfile** aktualizuje profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="ca709-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="ca709-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca709-107">EXAMPLES</span></span>

## <span data-ttu-id="ca709-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca709-108">PARAMETERS</span></span>

### <span data-ttu-id="ca709-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-109">-CdnProfile</span></span>
<span data-ttu-id="ca709-110">Określa profil, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca709-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ca709-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca709-111">-Confirm</span></span>
<span data-ttu-id="ca709-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca709-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca709-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca709-113">-WhatIf</span></span>
<span data-ttu-id="ca709-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca709-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca709-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca709-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca709-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-116">-DefaultProfile</span></span>
<span data-ttu-id="ca709-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca709-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca709-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca709-118">CommonParameters</span></span>
<span data-ttu-id="ca709-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca709-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca709-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca709-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca709-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca709-121">INPUTS</span></span>

### <span data-ttu-id="ca709-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-122">PSProfile</span></span>
<span data-ttu-id="ca709-123">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ca709-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="ca709-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca709-124">OUTPUTS</span></span>

### <span data-ttu-id="ca709-125">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ca709-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca709-126">NOTES</span></span>

## <span data-ttu-id="ca709-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca709-127">RELATED LINKS</span></span>

[<span data-ttu-id="ca709-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="ca709-129">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="ca709-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca709-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


