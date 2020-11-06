---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550344"
---
# <span data-ttu-id="24d7a-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="24d7a-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="24d7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="24d7a-103">Pobiera obsługiwane typy optymalizacji dla profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="24d7a-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24d7a-104">SYNTAX</span></span>

### <span data-ttu-id="24d7a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24d7a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24d7a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24d7a-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d7a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="24d7a-108">Polecenie cmdlet **Get-AzureRmCdnProfileSupportedOptimizationType** pobiera obsługiwane typy optymalizacji dla bieżącego profilu.</span><span class="sxs-lookup"><span data-stu-id="24d7a-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="24d7a-109">Użytkownik może utworzyć punkt końcowy z typem optymalizacji na liście wartości.</span><span class="sxs-lookup"><span data-stu-id="24d7a-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="24d7a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24d7a-110">EXAMPLES</span></span>

### <span data-ttu-id="24d7a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24d7a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="24d7a-112">Pobierz obsługiwane typy optymalizacji dla profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="24d7a-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="24d7a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24d7a-113">PARAMETERS</span></span>

### <span data-ttu-id="24d7a-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="24d7a-114">-CdnProfile</span></span>
<span data-ttu-id="24d7a-115">Obiekt profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="24d7a-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="24d7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d7a-116">-DefaultProfile</span></span>
<span data-ttu-id="24d7a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24d7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d7a-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="24d7a-118">-ProfileName</span></span>
<span data-ttu-id="24d7a-119">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="24d7a-119">The name of the profile.</span></span>

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

### <span data-ttu-id="24d7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="24d7a-121">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="24d7a-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="24d7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d7a-122">CommonParameters</span></span>
<span data-ttu-id="24d7a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d7a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d7a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d7a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24d7a-125">INPUTS</span></span>

### <span data-ttu-id="24d7a-126">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="24d7a-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="24d7a-127">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24d7a-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="24d7a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24d7a-128">OUTPUTS</span></span>

### <span data-ttu-id="24d7a-129">Microsoft. Azure. Commands. CDN. models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="24d7a-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="24d7a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24d7a-130">NOTES</span></span>

## <span data-ttu-id="24d7a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24d7a-131">RELATED LINKS</span></span>
