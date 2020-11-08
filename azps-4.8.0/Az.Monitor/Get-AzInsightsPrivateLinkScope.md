---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223405"
---
# <span data-ttu-id="8c448-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8c448-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="8c448-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c448-102">SYNOPSIS</span></span>
<span data-ttu-id="8c448-103">Uzyskaj zasięg linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="8c448-103">Get private link scope</span></span>

## <span data-ttu-id="8c448-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c448-104">SYNTAX</span></span>

### <span data-ttu-id="8c448-105">ByResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c448-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c448-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c448-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c448-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c448-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c448-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c448-108">DESCRIPTION</span></span>
<span data-ttu-id="8c448-109">Wyświetlanie lub uzyskiwanie prywatnego zakresu linków</span><span class="sxs-lookup"><span data-stu-id="8c448-109">List or get private link scope</span></span> 

## <span data-ttu-id="8c448-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c448-110">EXAMPLES</span></span>

### <span data-ttu-id="8c448-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c448-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="8c448-112">Wyświetlanie listy zakresów linków prywatnych w grupie zasób "rg_name"</span><span class="sxs-lookup"><span data-stu-id="8c448-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="8c448-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8c448-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="8c448-114">Pobierz zakres linków prywatnych o nazwie "scope_name" w grupie zasób "rg_name"</span><span class="sxs-lookup"><span data-stu-id="8c448-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="8c448-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c448-115">PARAMETERS</span></span>

### <span data-ttu-id="8c448-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c448-116">-DefaultProfile</span></span>
<span data-ttu-id="8c448-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c448-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c448-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c448-118">-Name</span></span>
<span data-ttu-id="8c448-119">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="8c448-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c448-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c448-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c448-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c448-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c448-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c448-122">-ResourceId</span></span>
<span data-ttu-id="8c448-123">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="8c448-123">Resource Id</span></span>

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

### <span data-ttu-id="8c448-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c448-124">CommonParameters</span></span>
<span data-ttu-id="8c448-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c448-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c448-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c448-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c448-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c448-127">INPUTS</span></span>

### <span data-ttu-id="8c448-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8c448-128">System.String</span></span>

## <span data-ttu-id="8c448-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c448-129">OUTPUTS</span></span>

### <span data-ttu-id="8c448-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8c448-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="8c448-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c448-131">NOTES</span></span>

## <span data-ttu-id="8c448-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c448-132">RELATED LINKS</span></span>
