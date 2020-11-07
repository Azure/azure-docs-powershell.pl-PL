---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: be7528f33bc51732c9345bbf7c9b718f590a8a5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710376"
---
# <span data-ttu-id="7e018-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7e018-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="7e018-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e018-102">SYNOPSIS</span></span>
<span data-ttu-id="7e018-103">Pobiera obsługiwane typy optymalizacji dla profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="7e018-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7e018-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e018-104">SYNTAX</span></span>

### <span data-ttu-id="7e018-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e018-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e018-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e018-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e018-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e018-107">DESCRIPTION</span></span>
<span data-ttu-id="7e018-108">Polecenie cmdlet **Get-AzCdnProfileSupportedOptimizationType** pobiera obsługiwane typy optymalizacji dla bieżącego profilu.</span><span class="sxs-lookup"><span data-stu-id="7e018-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="7e018-109">Użytkownik może utworzyć punkt końcowy z typem optymalizacji na liście wartości.</span><span class="sxs-lookup"><span data-stu-id="7e018-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="7e018-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e018-110">EXAMPLES</span></span>

### <span data-ttu-id="7e018-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e018-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="7e018-112">Pobierz obsługiwane typy optymalizacji dla profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="7e018-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7e018-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e018-113">PARAMETERS</span></span>

### <span data-ttu-id="7e018-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7e018-114">-CdnProfile</span></span>
<span data-ttu-id="7e018-115">Obiekt profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="7e018-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="7e018-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e018-116">-DefaultProfile</span></span>
<span data-ttu-id="7e018-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e018-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e018-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="7e018-118">-ProfileName</span></span>
<span data-ttu-id="7e018-119">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="7e018-119">The name of the profile.</span></span>

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

### <span data-ttu-id="7e018-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e018-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e018-121">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="7e018-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7e018-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e018-122">CommonParameters</span></span>
<span data-ttu-id="7e018-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e018-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e018-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e018-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e018-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e018-125">INPUTS</span></span>

### <span data-ttu-id="7e018-126">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7e018-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7e018-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e018-127">OUTPUTS</span></span>

### <span data-ttu-id="7e018-128">Microsoft. Azure. Commands. CDN. models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7e018-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="7e018-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e018-129">NOTES</span></span>

## <span data-ttu-id="7e018-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e018-130">RELATED LINKS</span></span>