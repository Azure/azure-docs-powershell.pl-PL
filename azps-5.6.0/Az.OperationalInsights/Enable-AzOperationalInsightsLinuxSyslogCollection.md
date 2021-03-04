---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 2a007a2695141d0772afeb025644f8a3dbf4efb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997536"
---
# <span data-ttu-id="87593-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="87593-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="87593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87593-102">SYNOPSIS</span></span>
<span data-ttu-id="87593-103">Uruchamia zbieranie danych syslogu z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="87593-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="87593-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87593-104">SYNTAX</span></span>

### <span data-ttu-id="87593-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="87593-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87593-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="87593-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87593-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="87593-107">DESCRIPTION</span></span>
<span data-ttu-id="87593-108">Polecenie cmdlet **Enable-AzOperationalInsightsLinuxSyslogCollection** uruchamia kolekcję danych syslogu z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="87593-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="87593-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87593-109">EXAMPLES</span></span>

## <span data-ttu-id="87593-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87593-110">PARAMETERS</span></span>

### <span data-ttu-id="87593-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87593-111">-DefaultProfile</span></span>
<span data-ttu-id="87593-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="87593-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87593-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87593-113">-ResourceGroupName</span></span>
<span data-ttu-id="87593-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="87593-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="87593-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="87593-115">-Workspace</span></span>
<span data-ttu-id="87593-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87593-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87593-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="87593-117">-WorkspaceName</span></span>
<span data-ttu-id="87593-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87593-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87593-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87593-119">-Confirm</span></span>
<span data-ttu-id="87593-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87593-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87593-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87593-121">-WhatIf</span></span>
<span data-ttu-id="87593-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87593-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87593-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87593-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87593-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87593-124">CommonParameters</span></span>
<span data-ttu-id="87593-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87593-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87593-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87593-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87593-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87593-127">INPUTS</span></span>

### <span data-ttu-id="87593-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="87593-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="87593-129">System.String</span><span class="sxs-lookup"><span data-stu-id="87593-129">System.String</span></span>

## <span data-ttu-id="87593-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87593-130">OUTPUTS</span></span>

### <span data-ttu-id="87593-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="87593-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="87593-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87593-132">NOTES</span></span>
* <span data-ttu-id="87593-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="87593-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="87593-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87593-134">RELATED LINKS</span></span>

[<span data-ttu-id="87593-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="87593-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="87593-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="87593-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


