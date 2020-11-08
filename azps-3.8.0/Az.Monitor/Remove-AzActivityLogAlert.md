---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 5a0841a3cb2cd01ebb7f44b41e89d0b30404dfd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049347"
---
# <span data-ttu-id="83c31-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83c31-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="83c31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83c31-102">SYNOPSIS</span></span>
<span data-ttu-id="83c31-103">Usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="83c31-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="83c31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83c31-104">SYNTAX</span></span>

### <span data-ttu-id="83c31-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83c31-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c31-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="83c31-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c31-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="83c31-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83c31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83c31-108">DESCRIPTION</span></span>
<span data-ttu-id="83c31-109">Polecenie cmdlet **Remove-AzActivityLogAlert** usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="83c31-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="83c31-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="83c31-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="83c31-111">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="83c31-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="83c31-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83c31-112">EXAMPLES</span></span>

### <span data-ttu-id="83c31-113">Przykład 1: Usuwanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="83c31-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="83c31-114">Usuwa alert dziennika aktywności przy użyciu nazw i grup zasobów jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="83c31-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="83c31-115">Przykład 2: Usuwanie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="83c31-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="83c31-116">Umożliwia usunięcie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="83c31-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="83c31-117">Przykład 3: usuwanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="83c31-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="83c31-118">To polecenie usuwa ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="83c31-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="83c31-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83c31-119">PARAMETERS</span></span>

### <span data-ttu-id="83c31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c31-120">-DefaultProfile</span></span>
<span data-ttu-id="83c31-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="83c31-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83c31-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83c31-122">-InputObject</span></span>
<span data-ttu-id="83c31-123">Ustawia właściwość Inputobject dla połączenia, aby wyodrębnić nazwę wymaganą, oraz właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83c31-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83c31-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83c31-124">-Name</span></span>
<span data-ttu-id="83c31-125">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="83c31-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c31-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c31-126">-ResourceGroupName</span></span>
<span data-ttu-id="83c31-127">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="83c31-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c31-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83c31-128">-ResourceId</span></span>
<span data-ttu-id="83c31-129">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83c31-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c31-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83c31-130">-Confirm</span></span>
<span data-ttu-id="83c31-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83c31-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c31-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c31-132">-WhatIf</span></span>
<span data-ttu-id="83c31-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83c31-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83c31-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83c31-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83c31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c31-135">CommonParameters</span></span>
<span data-ttu-id="83c31-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c31-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83c31-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c31-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83c31-138">INPUTS</span></span>

### <span data-ttu-id="83c31-139">System. String</span><span class="sxs-lookup"><span data-stu-id="83c31-139">System.String</span></span>

### <span data-ttu-id="83c31-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="83c31-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="83c31-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83c31-141">OUTPUTS</span></span>

### <span data-ttu-id="83c31-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="83c31-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="83c31-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83c31-143">NOTES</span></span>

## <span data-ttu-id="83c31-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83c31-144">RELATED LINKS</span></span>

[<span data-ttu-id="83c31-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83c31-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="83c31-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83c31-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="83c31-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83c31-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="83c31-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83c31-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="83c31-149">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="83c31-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="83c31-150">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="83c31-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

