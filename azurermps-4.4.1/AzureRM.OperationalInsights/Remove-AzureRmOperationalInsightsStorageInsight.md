---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cbbbd23a42f2922273811a7925cbae6f6fd867f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543103"
---
# <span data-ttu-id="5c5da-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5c5da-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="5c5da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c5da-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5da-103">Usuwa informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="5c5da-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c5da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c5da-104">SYNTAX</span></span>

### <span data-ttu-id="5c5da-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c5da-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c5da-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5c5da-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c5da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5c5da-107">DESCRIPTION</span></span>
<span data-ttu-id="5c5da-108">Polecenie cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** usuwa informacje o magazynowaniu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5c5da-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="5c5da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c5da-109">EXAMPLES</span></span>

### <span data-ttu-id="5c5da-110">Przykład 1: usunięcie szczegółowego miejsca do magazynowania według nazwy</span><span class="sxs-lookup"><span data-stu-id="5c5da-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="5c5da-111">To polecenie umożliwia usunięcie szczegółowego miejsca do magazynowania o nazwie MyStorageInsight z obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c5da-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="5c5da-112">Polecenie nie określa parametru *Force* , więc wyświetla monit o potwierdzenie przed usunięciem gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="5c5da-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="5c5da-113">Przykład 2: usunięcie szczegółowego miejsca do magazynowania bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="5c5da-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="5c5da-114">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace. Drugie polecenie usunie miejsce do magazynowania o nazwie MyStorageInsight z $Workspace bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5c5da-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="5c5da-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c5da-115">PARAMETERS</span></span>

### <span data-ttu-id="5c5da-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5c5da-116">-Force</span></span>
<span data-ttu-id="5c5da-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5c5da-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c5da-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c5da-118">-Name</span></span>
<span data-ttu-id="5c5da-119">Określa nazwę szczegółowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="5c5da-119">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="5c5da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5da-120">-ResourceGroupName</span></span>
<span data-ttu-id="5c5da-121">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5da-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="5c5da-122">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="5c5da-122">-Workspace</span></span>
<span data-ttu-id="5c5da-123">Określa obszar roboczy zawierający szczegółowe dane dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="5c5da-123">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5c5da-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5c5da-124">-WorkspaceName</span></span>
<span data-ttu-id="5c5da-125">Określa nazwę obszaru roboczego, który zawiera informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="5c5da-125">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5c5da-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c5da-126">-Confirm</span></span>
<span data-ttu-id="5c5da-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c5da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c5da-128">-WhatIf</span></span>
<span data-ttu-id="5c5da-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5da-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c5da-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c5da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c5da-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5da-131">-DefaultProfile</span></span>
<span data-ttu-id="5c5da-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5da-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5da-133">CommonParameters</span></span>
<span data-ttu-id="5c5da-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5da-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5da-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c5da-136">INPUTS</span></span>

### <span data-ttu-id="5c5da-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c5da-137">PSWorkspace</span></span>
<span data-ttu-id="5c5da-138">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="5c5da-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5c5da-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c5da-139">OUTPUTS</span></span>

## <span data-ttu-id="5c5da-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c5da-140">NOTES</span></span>

## <span data-ttu-id="5c5da-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c5da-141">RELATED LINKS</span></span>

[<span data-ttu-id="5c5da-142">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="5c5da-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="5c5da-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c5da-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


