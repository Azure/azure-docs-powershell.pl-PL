---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327381"
---
# <span data-ttu-id="8e9fd-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8e9fd-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="8e9fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9fd-103">Pobiera użycie zasobu w profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="8e9fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e9fd-104">SYNTAX</span></span>

### <span data-ttu-id="8e9fd-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e9fd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9fd-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9fd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8e9fd-107">DESCRIPTION</span></span>
<span data-ttu-id="8e9fd-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="8e9fd-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8e9fd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e9fd-109">EXAMPLES</span></span>

### <span data-ttu-id="8e9fd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e9fd-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8e9fd-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="8e9fd-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="8e9fd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e9fd-112">PARAMETERS</span></span>

### <span data-ttu-id="8e9fd-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8e9fd-113">-CdnProfile</span></span>
<span data-ttu-id="8e9fd-114">Obiekt profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="8e9fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9fd-115">-DefaultProfile</span></span>
<span data-ttu-id="8e9fd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8e9fd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9fd-117">-Refilename</span><span class="sxs-lookup"><span data-stu-id="8e9fd-117">-ProfileName</span></span>
<span data-ttu-id="8e9fd-118">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-118">The name of the profile.</span></span>

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

### <span data-ttu-id="8e9fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e9fd-120">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="8e9fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9fd-121">CommonParameters</span></span>
<span data-ttu-id="8e9fd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9fd-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e9fd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9fd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e9fd-124">INPUTS</span></span>

### <span data-ttu-id="8e9fd-125">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="8e9fd-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8e9fd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e9fd-126">OUTPUTS</span></span>

### <span data-ttu-id="8e9fd-127">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8e9fd-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="8e9fd-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e9fd-128">NOTES</span></span>

## <span data-ttu-id="8e9fd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e9fd-129">RELATED LINKS</span></span>
