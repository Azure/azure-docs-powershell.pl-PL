---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552183"
---
# <span data-ttu-id="e38f1-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="e38f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e38f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e38f1-103">Pobiera profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e38f1-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e38f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e38f1-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e38f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e38f1-105">DESCRIPTION</span></span>
<span data-ttu-id="e38f1-106">Polecenie cmdlet **Get-AzureRMCdnProfile** pobiera profil sieciowej usługi dostarczania zawartości (CDN, Content Delivery Network) i informacje powiązane z informacjami.</span><span class="sxs-lookup"><span data-stu-id="e38f1-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="e38f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e38f1-107">EXAMPLES</span></span>

## <span data-ttu-id="e38f1-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e38f1-108">PARAMETERS</span></span>

### <span data-ttu-id="e38f1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-109">-DefaultProfile</span></span>
<span data-ttu-id="e38f1-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e38f1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e38f1-111">-Refilename</span><span class="sxs-lookup"><span data-stu-id="e38f1-111">-ProfileName</span></span>
<span data-ttu-id="e38f1-112">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="e38f1-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e38f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="e38f1-114">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="e38f1-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e38f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38f1-115">CommonParameters</span></span>
<span data-ttu-id="e38f1-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38f1-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38f1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38f1-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e38f1-118">INPUTS</span></span>

### <span data-ttu-id="e38f1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e38f1-119">System.String</span></span>

## <span data-ttu-id="e38f1-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e38f1-120">OUTPUTS</span></span>

### <span data-ttu-id="e38f1-121">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e38f1-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e38f1-122">NOTES</span></span>

## <span data-ttu-id="e38f1-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e38f1-123">RELATED LINKS</span></span>

[<span data-ttu-id="e38f1-124">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="e38f1-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="e38f1-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e38f1-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)

