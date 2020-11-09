---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304560"
---
# <span data-ttu-id="9e38a-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="9e38a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e38a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e38a-103">Tworzy nowy lub ustawia istniejący alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="9e38a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e38a-104">SYNTAX</span></span>

### <span data-ttu-id="9e38a-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e38a-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e38a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e38a-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e38a-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e38a-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e38a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9e38a-108">DESCRIPTION</span></span>
<span data-ttu-id="9e38a-109">Polecenie cmdlet **Set-AzActivityLogAlert** tworzy nowy lub ustawia istniejący alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="9e38a-110">W przypadku tagów, warunków i akcji obiekty muszą być utworzone z wyprzedzeniem i przenoszone jako parametry w tej rozmowie jako oddzielone przecinkami (Zobacz przykład poniżej).</span><span class="sxs-lookup"><span data-stu-id="9e38a-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="9e38a-111">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem/zmodyfikowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e38a-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="9e38a-112">**Uwaga** : to polecenie cmdlet i powiązane z nim polecenia zastępują przestarzałe (listopad 2017) **Add-AzLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="9e38a-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="9e38a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e38a-113">EXAMPLES</span></span>

### <span data-ttu-id="9e38a-114">Przykład 1: Tworzenie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="9e38a-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="9e38a-115">Pierwsze cztery polecenia tworzą warunek liścia i grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="9e38a-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="9e38a-116">Ostatnie polecenie tworzy alert dziennika aktywności przy użyciu warunku i grupy Actions.</span><span class="sxs-lookup"><span data-stu-id="9e38a-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="9e38a-117">Przykład 2: wyłączono tworzenie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="9e38a-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="9e38a-118">Pierwsze cztery polecenia tworzą warunek liścia i grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="9e38a-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="9e38a-119">Ostatnie polecenie tworzy alert dziennika aktywności przy użyciu warunku i grupy Actions, ale powoduje utworzenie alertu wyłączonego.</span><span class="sxs-lookup"><span data-stu-id="9e38a-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="9e38a-120">Przykład 3: Ustawianie alertu dotyczącego dziennika aktywności opartego na wartości z parametru Pipe lub Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e38a-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="9e38a-121">Pierwsze polecenie jest podobne do NOP, ale powoduje, że alert ma te same wartości, które zawierały pozostałe polecenia pobierając regułę alertu, zmieni opis i wyłącz go, a następnie użyj parametru Inputobject, aby zachować te zmiany</span><span class="sxs-lookup"><span data-stu-id="9e38a-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="9e38a-122">Przykład 4: Ustawianie alertu dotyczącego dziennika aktywności opartego na wartości ResourceId z potoku</span><span class="sxs-lookup"><span data-stu-id="9e38a-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="9e38a-123">Jeśli ta reguła alertu dziennika istnieje, to polecenie je wyłącza.</span><span class="sxs-lookup"><span data-stu-id="9e38a-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="9e38a-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e38a-124">PARAMETERS</span></span>

### <span data-ttu-id="9e38a-125">-Action</span><span class="sxs-lookup"><span data-stu-id="9e38a-125">-Action</span></span>
<span data-ttu-id="9e38a-126">Lista grup akcji dla alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-127">-Warunek</span><span class="sxs-lookup"><span data-stu-id="9e38a-127">-Condition</span></span>
<span data-ttu-id="9e38a-128">Lista warunków alertu dotyczącego dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="9e38a-129">**Uwaga** : na liście warunków musi być co najmniej jedno pole równe "Kategoria".</span><span class="sxs-lookup"><span data-stu-id="9e38a-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="9e38a-130">W przypadku nieobecności tego warunku wewnętrzna baza danych odpowiada za pomocą usługi 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="9e38a-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e38a-131">-DefaultProfile</span></span>
<span data-ttu-id="9e38a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e38a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e38a-133">— Opis</span><span class="sxs-lookup"><span data-stu-id="9e38a-133">-Description</span></span>
<span data-ttu-id="9e38a-134">Opis zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="9e38a-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-135">-DisableAlert</span></span>
<span data-ttu-id="9e38a-136">Umożliwia użytkownikowi utworzenie wyłączanego alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="9e38a-137">Jeśli nie podano, alerty są tworzone.</span><span class="sxs-lookup"><span data-stu-id="9e38a-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e38a-138">-InputObject</span></span>
<span data-ttu-id="9e38a-139">Ustawia właściwość Inputobject dla połączenia, aby wyodrębnić nazwę wymaganą, oraz właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e38a-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9e38a-140">-Location</span></span>
<span data-ttu-id="9e38a-141">Lokalizacja, w której będzie istnieć alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e38a-142">-Name</span></span>
<span data-ttu-id="9e38a-143">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e38a-144">-ResourceGroupName</span></span>
<span data-ttu-id="9e38a-145">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="9e38a-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e38a-146">-ResourceId</span></span>
<span data-ttu-id="9e38a-147">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e38a-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-148">-Zakres</span><span class="sxs-lookup"><span data-stu-id="9e38a-148">-Scope</span></span>
<span data-ttu-id="9e38a-149">Lista zakresów alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e38a-150">-Tag</span></span>
<span data-ttu-id="9e38a-151">Ustawia właściwość Tagi dla zasobu alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="9e38a-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e38a-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e38a-152">-Confirm</span></span>
<span data-ttu-id="9e38a-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e38a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e38a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e38a-154">-WhatIf</span></span>
<span data-ttu-id="9e38a-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e38a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e38a-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e38a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e38a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e38a-157">CommonParameters</span></span>
<span data-ttu-id="9e38a-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e38a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e38a-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e38a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e38a-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e38a-160">INPUTS</span></span>

### <span data-ttu-id="9e38a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9e38a-161">System.String</span></span>

### <span data-ttu-id="9e38a-162">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e38a-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e38a-163">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Monitor. Management.. ActivityLogAlertLeafCondition; Microsoft. Azure. PowerShell. cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9e38a-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e38a-164">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Monitor. Management.. ActivityLogAlertActionGroup; Microsoft. Azure. PowerShell. cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9e38a-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e38a-165">System. Collections. Generic. dictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e38a-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e38a-166">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9e38a-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9e38a-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e38a-167">OUTPUTS</span></span>

### <span data-ttu-id="9e38a-168">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9e38a-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9e38a-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e38a-169">NOTES</span></span>

## <span data-ttu-id="9e38a-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e38a-170">RELATED LINKS</span></span>

[<span data-ttu-id="9e38a-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="9e38a-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="9e38a-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="9e38a-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e38a-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="9e38a-175">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9e38a-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="9e38a-176">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9e38a-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
