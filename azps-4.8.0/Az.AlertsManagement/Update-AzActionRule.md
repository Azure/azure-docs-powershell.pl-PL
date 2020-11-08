---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063744"
---
# <span data-ttu-id="2230c-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="2230c-101">Update-AzActionRule</span></span>

## <span data-ttu-id="2230c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2230c-102">SYNOPSIS</span></span>
<span data-ttu-id="2230c-103">Aktualizuje właściwości reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="2230c-103">Updates action rule properties.</span></span>

## <span data-ttu-id="2230c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2230c-104">SYNTAX</span></span>

### <span data-ttu-id="2230c-105">ByNameSimplifiedPatch (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2230c-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2230c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2230c-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2230c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2230c-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2230c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2230c-108">DESCRIPTION</span></span>
<span data-ttu-id="2230c-109">Polecenie cmdlet **Update-AzActionRule** umożliwia aktualizowanie właściwości reguł akcji — stan i znaczniki.</span><span class="sxs-lookup"><span data-stu-id="2230c-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="2230c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2230c-110">EXAMPLES</span></span>

### <span data-ttu-id="2230c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2230c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="2230c-112">To polecenie cmdlet wyłącza regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="2230c-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="2230c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2230c-113">PARAMETERS</span></span>

### <span data-ttu-id="2230c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2230c-114">-DefaultProfile</span></span>
<span data-ttu-id="2230c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2230c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2230c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2230c-116">-InputObject</span></span>
<span data-ttu-id="2230c-117">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2230c-118">-Name</span></span>
<span data-ttu-id="2230c-119">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2230c-120">-ResourceGroupName</span></span>
<span data-ttu-id="2230c-121">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2230c-122">-ResourceId</span></span>
<span data-ttu-id="2230c-123">Identyfikator zasobu reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-124">-Status</span><span class="sxs-lookup"><span data-stu-id="2230c-124">-Status</span></span>
<span data-ttu-id="2230c-125">Stan reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2230c-126">-Tag</span></span>
<span data-ttu-id="2230c-127">Tagi reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2230c-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2230c-128">-Confirm</span></span>
<span data-ttu-id="2230c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2230c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2230c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2230c-130">-WhatIf</span></span>
<span data-ttu-id="2230c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2230c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2230c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2230c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2230c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2230c-133">CommonParameters</span></span>
<span data-ttu-id="2230c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2230c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2230c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2230c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2230c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2230c-136">INPUTS</span></span>

### <span data-ttu-id="2230c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2230c-137">System.String</span></span>

### <span data-ttu-id="2230c-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2230c-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2230c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2230c-139">OUTPUTS</span></span>

### <span data-ttu-id="2230c-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2230c-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2230c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2230c-141">NOTES</span></span>

## <span data-ttu-id="2230c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2230c-142">RELATED LINKS</span></span>
