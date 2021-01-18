---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504298"
---
# <span data-ttu-id="01ad1-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="01ad1-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="01ad1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="01ad1-103">Usuwa informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="01ad1-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="01ad1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01ad1-104">SYNTAX</span></span>

### <span data-ttu-id="01ad1-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="01ad1-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ad1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="01ad1-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ad1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="01ad1-107">DESCRIPTION</span></span>
<span data-ttu-id="01ad1-108">Polecenie cmdlet **Remove-AzOperationalInsightsStorageInsight** usuwa informacje o magazynowaniu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="01ad1-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="01ad1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01ad1-109">EXAMPLES</span></span>

### <span data-ttu-id="01ad1-110">Przykład 1: usunięcie szczegółowego miejsca do magazynowania według nazwy</span><span class="sxs-lookup"><span data-stu-id="01ad1-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="01ad1-111">To polecenie umożliwia usunięcie szczegółowego miejsca do magazynowania o nazwie MyStorageInsight z obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="01ad1-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="01ad1-112">Polecenie nie określa parametru *Force* , więc wyświetla monit o potwierdzenie przed usunięciem gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="01ad1-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="01ad1-113">Przykład 2: usunięcie szczegółowego miejsca do magazynowania bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="01ad1-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="01ad1-114">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace. Drugie polecenie usunie miejsce do magazynowania o nazwie MyStorageInsight z $Workspace bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01ad1-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="01ad1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01ad1-115">PARAMETERS</span></span>

### <span data-ttu-id="01ad1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ad1-116">-DefaultProfile</span></span>
<span data-ttu-id="01ad1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01ad1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ad1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01ad1-118">-Force</span></span>
<span data-ttu-id="01ad1-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="01ad1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01ad1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01ad1-120">-Name</span></span>
<span data-ttu-id="01ad1-121">Określa nazwę szczegółowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="01ad1-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ad1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ad1-122">-ResourceGroupName</span></span>
<span data-ttu-id="01ad1-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01ad1-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="01ad1-124">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="01ad1-124">-Workspace</span></span>
<span data-ttu-id="01ad1-125">Określa obszar roboczy zawierający szczegółowe dane dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="01ad1-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="01ad1-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="01ad1-126">-WorkspaceName</span></span>
<span data-ttu-id="01ad1-127">Określa nazwę obszaru roboczego, który zawiera informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="01ad1-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="01ad1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01ad1-128">-Confirm</span></span>
<span data-ttu-id="01ad1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01ad1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ad1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ad1-130">-WhatIf</span></span>
<span data-ttu-id="01ad1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01ad1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ad1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01ad1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ad1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ad1-133">CommonParameters</span></span>
<span data-ttu-id="01ad1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ad1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ad1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ad1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ad1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01ad1-136">INPUTS</span></span>

### <span data-ttu-id="01ad1-137">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="01ad1-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="01ad1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="01ad1-138">System.String</span></span>

## <span data-ttu-id="01ad1-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01ad1-139">OUTPUTS</span></span>

### <span data-ttu-id="01ad1-140">System. void</span><span class="sxs-lookup"><span data-stu-id="01ad1-140">System.Void</span></span>

## <span data-ttu-id="01ad1-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01ad1-141">NOTES</span></span>

## <span data-ttu-id="01ad1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01ad1-142">RELATED LINKS</span></span>

[<span data-ttu-id="01ad1-143">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="01ad1-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="01ad1-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="01ad1-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


