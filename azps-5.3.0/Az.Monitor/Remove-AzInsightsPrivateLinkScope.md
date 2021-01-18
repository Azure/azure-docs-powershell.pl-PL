---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499682"
---
# <span data-ttu-id="b1c05-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b1c05-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="b1c05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1c05-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c05-103">Usuwanie zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="b1c05-103">delete private link scope</span></span>

## <span data-ttu-id="b1c05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1c05-104">SYNTAX</span></span>

### <span data-ttu-id="b1c05-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1c05-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c05-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c05-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c05-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c05-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c05-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1c05-108">DESCRIPTION</span></span>
<span data-ttu-id="b1c05-109">Usuwanie zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="b1c05-109">delete private link scope</span></span>

## <span data-ttu-id="b1c05-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1c05-110">EXAMPLES</span></span>

### <span data-ttu-id="b1c05-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1c05-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="b1c05-112">Usuwanie zakresu linków prywatnych o nazwie "scope_name" w grupie zasób "rg_name"</span><span class="sxs-lookup"><span data-stu-id="b1c05-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="b1c05-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b1c05-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="b1c05-114">Usuwanie zakresu linków prywatnych z identyfikatorem zasobu</span><span class="sxs-lookup"><span data-stu-id="b1c05-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="b1c05-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b1c05-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="b1c05-116">Usuwanie zakresu linków prywatnych z wejściowym obiektem zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="b1c05-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="b1c05-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1c05-117">PARAMETERS</span></span>

### <span data-ttu-id="b1c05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c05-118">-DefaultProfile</span></span>
<span data-ttu-id="b1c05-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c05-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1c05-120">-InputObject</span></span>
<span data-ttu-id="b1c05-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b1c05-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c05-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1c05-122">-Name</span></span>
<span data-ttu-id="b1c05-123">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="b1c05-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="b1c05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c05-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1c05-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b1c05-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b1c05-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1c05-126">-ResourceId</span></span>
<span data-ttu-id="b1c05-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="b1c05-127">Resource Id</span></span>

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

### <span data-ttu-id="b1c05-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1c05-128">-Confirm</span></span>
<span data-ttu-id="b1c05-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c05-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c05-130">-WhatIf</span></span>
<span data-ttu-id="b1c05-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c05-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c05-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1c05-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c05-133">CommonParameters</span></span>
<span data-ttu-id="b1c05-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c05-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1c05-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c05-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1c05-136">INPUTS</span></span>

### <span data-ttu-id="b1c05-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b1c05-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="b1c05-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c05-138">System.String</span></span>

## <span data-ttu-id="b1c05-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1c05-139">OUTPUTS</span></span>

### <span data-ttu-id="b1c05-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1c05-140">System.Boolean</span></span>

## <span data-ttu-id="b1c05-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1c05-141">NOTES</span></span>

## <span data-ttu-id="b1c05-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1c05-142">RELATED LINKS</span></span>
