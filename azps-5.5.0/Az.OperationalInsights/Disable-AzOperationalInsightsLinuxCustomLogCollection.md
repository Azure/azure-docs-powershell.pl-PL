---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 94706768c6e5f222abe5a74ea32549f356abe1c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189434"
---
# <span data-ttu-id="7cf40-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="7cf40-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="7cf40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf40-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf40-103">Zatrzymuje zbieranie niestandardowych dzienników z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="7cf40-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="7cf40-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7cf40-104">SYNTAX</span></span>

### <span data-ttu-id="7cf40-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7cf40-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf40-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7cf40-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf40-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7cf40-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf40-108">Polecenie cmdlet **Disable-AzOperationalInsightsLinuxCustomLogCollection** zatrzymuje kolekcję niestandardowych dzienników z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7cf40-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="7cf40-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7cf40-109">EXAMPLES</span></span>

## <span data-ttu-id="7cf40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf40-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf40-111">-DefaultProfile</span></span>
<span data-ttu-id="7cf40-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7cf40-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cf40-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf40-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cf40-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="7cf40-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf40-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="7cf40-115">-Workspace</span></span>
<span data-ttu-id="7cf40-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf40-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf40-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7cf40-117">-WorkspaceName</span></span>
<span data-ttu-id="7cf40-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf40-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf40-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf40-119">-Confirm</span></span>
<span data-ttu-id="7cf40-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cf40-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf40-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf40-121">-WhatIf</span></span>
<span data-ttu-id="7cf40-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf40-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf40-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7cf40-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf40-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf40-124">CommonParameters</span></span>
<span data-ttu-id="7cf40-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf40-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf40-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf40-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf40-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf40-127">INPUTS</span></span>

### <span data-ttu-id="7cf40-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cf40-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7cf40-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf40-129">System.String</span></span>

## <span data-ttu-id="7cf40-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf40-130">OUTPUTS</span></span>

### <span data-ttu-id="7cf40-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7cf40-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7cf40-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7cf40-132">NOTES</span></span>
* <span data-ttu-id="7cf40-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="7cf40-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7cf40-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf40-134">RELATED LINKS</span></span>

[<span data-ttu-id="7cf40-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="7cf40-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


