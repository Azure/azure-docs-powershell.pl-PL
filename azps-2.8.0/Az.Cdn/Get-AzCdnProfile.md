---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: a833d542bd72392ef56e5a8bde086247f1f2c299
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706566"
---
# <span data-ttu-id="f66ad-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="f66ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f66ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f66ad-103">Pobiera profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="f66ad-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="f66ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f66ad-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f66ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f66ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f66ad-106">Polecenie cmdlet **Get-AzCdnProfile** pobiera profil sieciowej usługi dostarczania zawartości (CDN, Content Delivery Network) i informacje powiązane z informacjami.</span><span class="sxs-lookup"><span data-stu-id="f66ad-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="f66ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f66ad-107">EXAMPLES</span></span>

## <span data-ttu-id="f66ad-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f66ad-108">PARAMETERS</span></span>

### <span data-ttu-id="f66ad-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-109">-DefaultProfile</span></span>
<span data-ttu-id="f66ad-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f66ad-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f66ad-111">-Refilename</span><span class="sxs-lookup"><span data-stu-id="f66ad-111">-ProfileName</span></span>
<span data-ttu-id="f66ad-112">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="f66ad-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f66ad-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66ad-113">-ResourceGroupName</span></span>
<span data-ttu-id="f66ad-114">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="f66ad-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f66ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66ad-115">CommonParameters</span></span>
<span data-ttu-id="f66ad-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66ad-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f66ad-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66ad-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66ad-118">INPUTS</span></span>

### <span data-ttu-id="f66ad-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f66ad-119">System.String</span></span>

## <span data-ttu-id="f66ad-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f66ad-120">OUTPUTS</span></span>

### <span data-ttu-id="f66ad-121">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f66ad-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f66ad-122">NOTES</span></span>

## <span data-ttu-id="f66ad-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f66ad-123">RELATED LINKS</span></span>

[<span data-ttu-id="f66ad-124">Nowe — AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="f66ad-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="f66ad-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f66ad-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)

