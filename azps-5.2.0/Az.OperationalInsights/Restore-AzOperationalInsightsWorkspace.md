---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337573"
---
# <span data-ttu-id="68954-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="68954-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="68954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68954-102">SYNOPSIS</span></span>
<span data-ttu-id="68954-103">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68954-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="68954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68954-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68954-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68954-105">DESCRIPTION</span></span>
<span data-ttu-id="68954-106">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68954-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="68954-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68954-107">EXAMPLES</span></span>

### <span data-ttu-id="68954-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68954-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="68954-109">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68954-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="68954-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68954-110">PARAMETERS</span></span>

### <span data-ttu-id="68954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68954-111">-DefaultProfile</span></span>
<span data-ttu-id="68954-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68954-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68954-113">-Force</span><span class="sxs-lookup"><span data-stu-id="68954-113">-Force</span></span>
<span data-ttu-id="68954-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68954-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="68954-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="68954-115">-Location</span></span>
<span data-ttu-id="68954-116">Region geograficzny, w którym zostanie utworzony obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="68954-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="68954-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68954-117">-Name</span></span>
<span data-ttu-id="68954-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68954-118">The workspace name.</span></span>

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

### <span data-ttu-id="68954-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68954-119">-ResourceGroupName</span></span>
<span data-ttu-id="68954-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68954-120">The resource group name.</span></span>

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

### <span data-ttu-id="68954-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68954-121">-Confirm</span></span>
<span data-ttu-id="68954-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68954-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68954-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68954-123">-WhatIf</span></span>
<span data-ttu-id="68954-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68954-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68954-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68954-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68954-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68954-126">CommonParameters</span></span>
<span data-ttu-id="68954-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68954-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68954-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68954-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68954-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68954-129">INPUTS</span></span>

### <span data-ttu-id="68954-130">System. String</span><span class="sxs-lookup"><span data-stu-id="68954-130">System.String</span></span>

## <span data-ttu-id="68954-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68954-131">OUTPUTS</span></span>

### <span data-ttu-id="68954-132">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="68954-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="68954-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68954-133">NOTES</span></span>

## <span data-ttu-id="68954-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68954-134">RELATED LINKS</span></span>
