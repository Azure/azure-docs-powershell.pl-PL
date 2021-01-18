---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502994"
---
# <span data-ttu-id="0fc67-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc67-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="0fc67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fc67-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc67-103">Pobiera analityczne (regułę alertu).</span><span class="sxs-lookup"><span data-stu-id="0fc67-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="0fc67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fc67-104">SYNTAX</span></span>

### <span data-ttu-id="0fc67-105">WorkspaceScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0fc67-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fc67-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0fc67-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fc67-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0fc67-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fc67-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0fc67-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc67-109">Polecenie cmdlet **Get-AzSentinelAlertRule** pobiera dane analityczne (regułę alertu) z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0fc67-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="0fc67-110">Jeśli określisz parametr *AlertRuleId* , zostanie zwrócony jeden obiekt **AlertRule** .</span><span class="sxs-lookup"><span data-stu-id="0fc67-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="0fc67-111">Jeśli nie określisz parametru *AlertRuleId* , zostanie zwrócona tablica zawierająca wszystkie reguły alertów w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="0fc67-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="0fc67-112">Za pomocą obiektu **AlertRule** można zaktualizować AlertRule, na przykład można wyłączyć **AlertRule**.</span><span class="sxs-lookup"><span data-stu-id="0fc67-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="0fc67-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fc67-113">EXAMPLES</span></span>

### <span data-ttu-id="0fc67-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0fc67-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="0fc67-115">W tym przykładzie są pobierane wszystkie **AlertRules** w określonym obszarze roboczym, a następnie zostanie on zapisany w zmiennej $AlertRules.</span><span class="sxs-lookup"><span data-stu-id="0fc67-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="0fc67-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0fc67-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="0fc67-117">W tym przykładzie jest pobierany **AlertRule** w określonym obszarze roboczym, a następnie przechowywany w zmiennej $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="0fc67-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="0fc67-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fc67-118">PARAMETERS</span></span>

### <span data-ttu-id="0fc67-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0fc67-119">-AlertRuleId</span></span>
<span data-ttu-id="0fc67-120">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="0fc67-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc67-121">-DefaultProfile</span></span>
<span data-ttu-id="0fc67-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc67-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc67-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fc67-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fc67-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fc67-125">-ResourceId</span></span>
<span data-ttu-id="0fc67-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fc67-126">Resource Id.</span></span>

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

### <span data-ttu-id="0fc67-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="0fc67-127">-WorkspaceName</span></span>
<span data-ttu-id="0fc67-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0fc67-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc67-129">CommonParameters</span></span>
<span data-ttu-id="0fc67-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc67-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc67-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fc67-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc67-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fc67-132">INPUTS</span></span>

### <span data-ttu-id="0fc67-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0fc67-133">System.String</span></span>
## <span data-ttu-id="0fc67-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fc67-134">OUTPUTS</span></span>

### <span data-ttu-id="0fc67-135">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc67-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="0fc67-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fc67-136">NOTES</span></span>

## <span data-ttu-id="0fc67-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fc67-137">RELATED LINKS</span></span>
