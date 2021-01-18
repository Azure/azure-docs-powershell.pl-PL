---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502984"
---
# <span data-ttu-id="27bda-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="27bda-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="27bda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27bda-102">SYNOPSIS</span></span>
<span data-ttu-id="27bda-103">Pobierz szablon reguły analitycznej.</span><span class="sxs-lookup"><span data-stu-id="27bda-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="27bda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27bda-104">SYNTAX</span></span>

### <span data-ttu-id="27bda-105">WorkspaceScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27bda-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27bda-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="27bda-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27bda-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="27bda-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27bda-108">Opis</span><span class="sxs-lookup"><span data-stu-id="27bda-108">DESCRIPTION</span></span>
<span data-ttu-id="27bda-109">Polecenie cmdlet **Get-AzSentinelAlertRuleTemplate** pobiera szablon reguły alertu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="27bda-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="27bda-110">Jeśli określisz parametr *AlertRuleTemplateId* , zostanie zwrócony jeden obiekt **AlertRuleTemplate** .</span><span class="sxs-lookup"><span data-stu-id="27bda-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="27bda-111">Jeśli nie określisz parametru *AlertRuleTemplateId* , zostaną zwrócone tablica zawierająca wszystkie szablony reguł alertów w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="27bda-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="27bda-112">Za pomocą obiektu **AlertRuleTemplate** można utworzyć nową regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="27bda-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="27bda-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27bda-113">EXAMPLES</span></span>

### <span data-ttu-id="27bda-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27bda-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="27bda-115">W tym przykładzie są pobierane wszystkie **AlertRuleTemplates** w określonym obszarze roboczym, a następnie zostanie on zapisany w zmiennej $AlertRuleTemplates.</span><span class="sxs-lookup"><span data-stu-id="27bda-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="27bda-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="27bda-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="27bda-117">W tym przykładzie jest pobierany **AlertRuleTemplate** w określonym obszarze roboczym, a następnie przechowywany w zmiennej $AlertRuleTemplate.</span><span class="sxs-lookup"><span data-stu-id="27bda-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="27bda-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27bda-118">PARAMETERS</span></span>

### <span data-ttu-id="27bda-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="27bda-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="27bda-120">Identyfikator reguły alertu dla szablonu.</span><span class="sxs-lookup"><span data-stu-id="27bda-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bda-121">-DefaultProfile</span></span>
<span data-ttu-id="27bda-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27bda-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27bda-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27bda-123">-ResourceGroupName</span></span>
<span data-ttu-id="27bda-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27bda-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bda-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27bda-125">-ResourceId</span></span>
<span data-ttu-id="27bda-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="27bda-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bda-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="27bda-127">-WorkspaceName</span></span>
<span data-ttu-id="27bda-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="27bda-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bda-129">CommonParameters</span></span>
<span data-ttu-id="27bda-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27bda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bda-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27bda-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bda-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27bda-132">INPUTS</span></span>

### <span data-ttu-id="27bda-133">System. String</span><span class="sxs-lookup"><span data-stu-id="27bda-133">System.String</span></span>
## <span data-ttu-id="27bda-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27bda-134">OUTPUTS</span></span>

### <span data-ttu-id="27bda-135">Microsoft. Azure. Commands. SecurityInsights. models. AlertRuleTemplates. PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="27bda-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="27bda-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27bda-136">NOTES</span></span>

## <span data-ttu-id="27bda-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27bda-137">RELATED LINKS</span></span>
