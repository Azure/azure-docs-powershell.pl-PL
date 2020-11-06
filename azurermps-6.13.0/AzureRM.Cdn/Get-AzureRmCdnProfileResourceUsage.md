---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526262"
---
# <span data-ttu-id="779a8-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="779a8-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="779a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="779a8-102">SYNOPSIS</span></span>
<span data-ttu-id="779a8-103">Pobiera użycie zasobu w profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="779a8-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="779a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="779a8-104">SYNTAX</span></span>

### <span data-ttu-id="779a8-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="779a8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="779a8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="779a8-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="779a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="779a8-107">DESCRIPTION</span></span>
<span data-ttu-id="779a8-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="779a8-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="779a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="779a8-109">EXAMPLES</span></span>

### <span data-ttu-id="779a8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="779a8-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="779a8-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="779a8-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="779a8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="779a8-112">PARAMETERS</span></span>

### <span data-ttu-id="779a8-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="779a8-113">-CdnProfile</span></span>
<span data-ttu-id="779a8-114">Obiekt profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="779a8-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="779a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779a8-115">-DefaultProfile</span></span>
<span data-ttu-id="779a8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="779a8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="779a8-117">-Refilename</span><span class="sxs-lookup"><span data-stu-id="779a8-117">-ProfileName</span></span>
<span data-ttu-id="779a8-118">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="779a8-118">The name of the profile.</span></span>

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

### <span data-ttu-id="779a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="779a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="779a8-120">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="779a8-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="779a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779a8-121">CommonParameters</span></span>
<span data-ttu-id="779a8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779a8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779a8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="779a8-124">INPUTS</span></span>

### <span data-ttu-id="779a8-125">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="779a8-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="779a8-126">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="779a8-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="779a8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="779a8-127">OUTPUTS</span></span>

### <span data-ttu-id="779a8-128">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="779a8-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="779a8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="779a8-129">NOTES</span></span>

## <span data-ttu-id="779a8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="779a8-130">RELATED LINKS</span></span>
