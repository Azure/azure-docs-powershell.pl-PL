---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 4bb969e0d18aca0f05663003c0fe78edf5b0e99d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541639"
---
# <span data-ttu-id="43680-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="43680-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="43680-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43680-102">SYNOPSIS</span></span>
<span data-ttu-id="43680-103">Rozpoczyna zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="43680-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43680-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43680-104">SYNTAX</span></span>

### <span data-ttu-id="43680-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43680-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43680-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="43680-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43680-107">Opis</span><span class="sxs-lookup"><span data-stu-id="43680-107">DESCRIPTION</span></span>
<span data-ttu-id="43680-108">Polecenie cmdlet **enable-AzureRmOperationalInsightsLinuxPerformanceCollection** rozpoczyna zbieranie liczników wydajności z podłączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="43680-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="43680-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43680-109">EXAMPLES</span></span>

## <span data-ttu-id="43680-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43680-110">PARAMETERS</span></span>

### <span data-ttu-id="43680-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43680-111">-DefaultProfile</span></span>
<span data-ttu-id="43680-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="43680-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43680-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43680-113">-ResourceGroupName</span></span>
<span data-ttu-id="43680-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="43680-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="43680-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="43680-115">-Workspace</span></span>
<span data-ttu-id="43680-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43680-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="43680-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="43680-117">-WorkspaceName</span></span>
<span data-ttu-id="43680-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43680-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="43680-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43680-119">-Confirm</span></span>
<span data-ttu-id="43680-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43680-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43680-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43680-121">-WhatIf</span></span>
<span data-ttu-id="43680-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43680-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43680-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43680-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43680-124">CommonParameters</span></span>
<span data-ttu-id="43680-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43680-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43680-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43680-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43680-127">INPUTS</span></span>

### <span data-ttu-id="43680-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="43680-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="43680-129">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43680-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="43680-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43680-130">System.String</span></span>

## <span data-ttu-id="43680-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43680-131">OUTPUTS</span></span>

### <span data-ttu-id="43680-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="43680-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="43680-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43680-133">NOTES</span></span>
* <span data-ttu-id="43680-134">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="43680-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="43680-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43680-135">RELATED LINKS</span></span>

[<span data-ttu-id="43680-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="43680-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


