---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 1ef047fa821a2eb74f0c06f82b42f51a1197dfc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550855"
---
# <span data-ttu-id="cd6e7-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="cd6e7-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="cd6e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6e7-103">Rozpoczyna zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd6e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd6e7-104">SYNTAX</span></span>

### <span data-ttu-id="cd6e7-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd6e7-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd6e7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cd6e7-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd6e7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd6e7-107">DESCRIPTION</span></span>
<span data-ttu-id="cd6e7-108">Polecenie cmdlet **enable-AzureRmOperationalInsightsLinuxPerformanceCollection** rozpoczyna zbieranie liczników wydajności z podłączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cd6e7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd6e7-109">EXAMPLES</span></span>

## <span data-ttu-id="cd6e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd6e7-110">PARAMETERS</span></span>

### <span data-ttu-id="cd6e7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6e7-111">-ResourceGroupName</span></span>
<span data-ttu-id="cd6e7-112">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="cd6e7-113">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cd6e7-113">-Workspace</span></span>
<span data-ttu-id="cd6e7-114">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cd6e7-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cd6e7-115">-WorkspaceName</span></span>
<span data-ttu-id="cd6e7-116">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cd6e7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd6e7-117">-Confirm</span></span>
<span data-ttu-id="cd6e7-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6e7-119">-WhatIf</span></span>
<span data-ttu-id="cd6e7-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd6e7-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6e7-122">-DefaultProfile</span></span>
<span data-ttu-id="cd6e7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd6e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6e7-124">CommonParameters</span></span>
<span data-ttu-id="cd6e7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6e7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6e7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd6e7-127">INPUTS</span></span>

### <span data-ttu-id="cd6e7-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd6e7-128">PSWorkspace</span></span>
<span data-ttu-id="cd6e7-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="cd6e7-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cd6e7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd6e7-130">OUTPUTS</span></span>

### <span data-ttu-id="cd6e7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cd6e7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cd6e7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd6e7-132">NOTES</span></span>
* <span data-ttu-id="cd6e7-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="cd6e7-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cd6e7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd6e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd6e7-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="cd6e7-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


