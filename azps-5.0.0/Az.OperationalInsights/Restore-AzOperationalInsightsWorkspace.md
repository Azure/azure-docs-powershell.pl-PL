---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224891"
---
# <span data-ttu-id="74367-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="74367-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="74367-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74367-102">SYNOPSIS</span></span>
<span data-ttu-id="74367-103">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="74367-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="74367-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74367-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74367-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74367-105">DESCRIPTION</span></span>
<span data-ttu-id="74367-106">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="74367-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="74367-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74367-107">EXAMPLES</span></span>

### <span data-ttu-id="74367-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74367-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="74367-109">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="74367-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="74367-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74367-110">PARAMETERS</span></span>

### <span data-ttu-id="74367-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74367-111">-DefaultProfile</span></span>
<span data-ttu-id="74367-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74367-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74367-113">-Force</span><span class="sxs-lookup"><span data-stu-id="74367-113">-Force</span></span>
<span data-ttu-id="74367-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74367-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74367-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74367-115">-Location</span></span>
<span data-ttu-id="74367-116">Region geograficzny, w którym zostanie utworzony obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="74367-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74367-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74367-117">-Name</span></span>
<span data-ttu-id="74367-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="74367-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74367-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74367-119">-ResourceGroupName</span></span>
<span data-ttu-id="74367-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74367-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74367-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74367-121">-Confirm</span></span>
<span data-ttu-id="74367-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74367-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74367-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74367-123">-WhatIf</span></span>
<span data-ttu-id="74367-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74367-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74367-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74367-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74367-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74367-126">CommonParameters</span></span>
<span data-ttu-id="74367-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74367-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74367-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74367-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74367-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74367-129">INPUTS</span></span>

### <span data-ttu-id="74367-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74367-130">System.String</span></span>

## <span data-ttu-id="74367-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74367-131">OUTPUTS</span></span>

### <span data-ttu-id="74367-132">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="74367-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="74367-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74367-133">NOTES</span></span>

## <span data-ttu-id="74367-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74367-134">RELATED LINKS</span></span>
