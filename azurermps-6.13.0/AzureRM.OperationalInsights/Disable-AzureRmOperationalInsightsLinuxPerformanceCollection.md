---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: e6a77e8e89f710e1f8f827a27b1e1709ca8e3f1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527809"
---
# <span data-ttu-id="f3e4e-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f3e4e-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="f3e4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e4e-103">Zatrzymuje zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3e4e-104">SYNTAX</span></span>

### <span data-ttu-id="f3e4e-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3e4e-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3e4e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3e4e-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3e4e-107">DESCRIPTION</span></span>
<span data-ttu-id="f3e4e-108">Polecenie cmdlet **disable-AzureRmOperationalInsightsLinuxPerformanceCollection** zatrzymuje zbieranie liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="f3e4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3e4e-109">EXAMPLES</span></span>

## <span data-ttu-id="f3e4e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3e4e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e4e-111">-DefaultProfile</span></span>
<span data-ttu-id="f3e4e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f3e4e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3e4e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e4e-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3e4e-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="f3e4e-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="f3e4e-115">-Workspace</span></span>
<span data-ttu-id="f3e4e-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f3e4e-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f3e4e-117">-WorkspaceName</span></span>
<span data-ttu-id="f3e4e-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f3e4e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3e4e-119">-Confirm</span></span>
<span data-ttu-id="f3e4e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e4e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e4e-121">-WhatIf</span></span>
<span data-ttu-id="f3e4e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e4e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e4e-124">CommonParameters</span></span>
<span data-ttu-id="f3e4e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e4e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e4e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e4e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3e4e-127">INPUTS</span></span>

### <span data-ttu-id="f3e4e-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3e4e-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="f3e4e-129">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3e4e-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="f3e4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e4e-130">System.String</span></span>

## <span data-ttu-id="f3e4e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3e4e-131">OUTPUTS</span></span>

### <span data-ttu-id="f3e4e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f3e4e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f3e4e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3e4e-133">NOTES</span></span>
* <span data-ttu-id="f3e4e-134">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="f3e4e-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f3e4e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3e4e-135">RELATED LINKS</span></span>

[<span data-ttu-id="f3e4e-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f3e4e-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="f3e4e-137">Nowe — AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="f3e4e-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


