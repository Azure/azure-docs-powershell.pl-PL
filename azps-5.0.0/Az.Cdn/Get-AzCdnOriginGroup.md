---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234004"
---
# <span data-ttu-id="da260-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="da260-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="da260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da260-102">SYNOPSIS</span></span>
<span data-ttu-id="da260-103">Pobiera grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="da260-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="da260-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da260-104">SYNTAX</span></span>

### <span data-ttu-id="da260-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da260-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da260-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da260-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da260-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da260-107">DESCRIPTION</span></span>
<span data-ttu-id="da260-108">Polecenie cmdlet Get-AzCdnOriginGroup pobiera grupę pochodzenie z sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="da260-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="da260-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da260-109">EXAMPLES</span></span>

### <span data-ttu-id="da260-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da260-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="da260-111">To polecenie spowoduje pobranie grupy źródłowej w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="da260-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="da260-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da260-112">PARAMETERS</span></span>

### <span data-ttu-id="da260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da260-113">-DefaultProfile</span></span>
<span data-ttu-id="da260-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da260-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da260-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="da260-115">-EndpointName</span></span>
<span data-ttu-id="da260-116">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="da260-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="da260-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="da260-117">-OriginGroupName</span></span>
<span data-ttu-id="da260-118">Nazwa grupy pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="da260-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="da260-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="da260-119">-ProfileName</span></span>
<span data-ttu-id="da260-120">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="da260-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="da260-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da260-121">-ResourceGroupName</span></span>
<span data-ttu-id="da260-122">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="da260-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="da260-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da260-123">-ResourceId</span></span>
<span data-ttu-id="da260-124">Identyfikator zasobu grupy źródłowej</span><span class="sxs-lookup"><span data-stu-id="da260-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da260-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da260-125">CommonParameters</span></span>
<span data-ttu-id="da260-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da260-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da260-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da260-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da260-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da260-128">INPUTS</span></span>

### <span data-ttu-id="da260-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="da260-129">None</span></span>

## <span data-ttu-id="da260-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da260-130">OUTPUTS</span></span>

### <span data-ttu-id="da260-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="da260-131">System.Object</span></span>

## <span data-ttu-id="da260-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da260-132">NOTES</span></span>

## <span data-ttu-id="da260-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da260-133">RELATED LINKS</span></span>
