---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717838"
---
# <span data-ttu-id="7f152-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="7f152-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f152-102">SYNOPSIS</span></span>
<span data-ttu-id="7f152-103">Tworzy nowy lub ustawia istniejący alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f152-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f152-104">SYNTAX</span></span>

### <span data-ttu-id="7f152-105">Parametry domyślne dla alertu dotyczącego ustawiania dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="7f152-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f152-106">Parametry umożliwiające ustawienie alertów dziennika aktywności przyjmujących wartość ResourceId z potoku</span><span class="sxs-lookup"><span data-stu-id="7f152-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f152-107">Parametry umożliwiające ustawienie alertów dziennika aktywności z przeprowadzoną wartością z potoku</span><span class="sxs-lookup"><span data-stu-id="7f152-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f152-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7f152-108">DESCRIPTION</span></span>
<span data-ttu-id="7f152-109">Polecenie cmdlet **Set-AzureRmActivityLogAlert** tworzy nowy lub ustawia istniejący alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="7f152-110">W przypadku tagów, warunków i akcji obiekty muszą być utworzone z wyprzedzeniem i przenoszone jako parametry w tej rozmowie jako oddzielone przecinkami (Zobacz przykład poniżej).</span><span class="sxs-lookup"><span data-stu-id="7f152-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="7f152-111">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem/zmodyfikowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f152-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="7f152-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f152-112">EXAMPLES</span></span>

### <span data-ttu-id="7f152-113">Przykład 1: Tworzenie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="7f152-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="7f152-114">Pierwsze cztery polecenia tworzą warunek liścia i grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="7f152-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="7f152-115">Ostatnie polecenie tworzy alert dziennika aktywności przy użyciu warunku i grupy Actions.</span><span class="sxs-lookup"><span data-stu-id="7f152-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="7f152-116">Przykład 2: wyłączono tworzenie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="7f152-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="7f152-117">Pierwsze cztery polecenia tworzą warunek liścia i grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="7f152-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="7f152-118">Ostatnie polecenie tworzy alert dziennika aktywności przy użyciu warunku i grupy Actions, ale powoduje utworzenie alertu wyłączonego.</span><span class="sxs-lookup"><span data-stu-id="7f152-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="7f152-119">Przykład 3: Ustawianie alertu dotyczącego dziennika aktywności opartego na wartości z parametru Pipe lub Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f152-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="7f152-120">Pierwsze polecenie jest podobne do NOP, ale powoduje, że alert ma te same wartości, które zawierały pozostałe polecenia pobierając regułę alertu, zmieni opis i wyłącz go, a następnie użyj parametru Inputobject, aby zachować te zmiany</span><span class="sxs-lookup"><span data-stu-id="7f152-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="7f152-121">Przykład 4: Ustawianie alertu dotyczącego dziennika aktywności opartego na wartości ResourceId z potoku</span><span class="sxs-lookup"><span data-stu-id="7f152-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="7f152-122">Jeśli ta reguła alertu dziennika istnieje, to polecenie je wyłącza.</span><span class="sxs-lookup"><span data-stu-id="7f152-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="7f152-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f152-123">PARAMETERS</span></span>

### <span data-ttu-id="7f152-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f152-124">-Location</span></span>
<span data-ttu-id="7f152-125">Lokalizacja, w której będzie istnieć alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f152-126">-Name</span></span>
<span data-ttu-id="7f152-127">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f152-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f152-129">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="7f152-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-130">-Zakres</span><span class="sxs-lookup"><span data-stu-id="7f152-130">-Scope</span></span>
<span data-ttu-id="7f152-131">Lista zakresów alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-132">-Warunek</span><span class="sxs-lookup"><span data-stu-id="7f152-132">-Condition</span></span>
<span data-ttu-id="7f152-133">Lista warunków alertu dotyczącego dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="7f152-134">**Uwaga** : na liście warunków musi być co najmniej jedno pole równe "Kategoria".</span><span class="sxs-lookup"><span data-stu-id="7f152-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="7f152-135">W przypadku nieobecności tego warunku wewnętrzna baza danych odpowiada za pomocą usługi 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="7f152-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-136">-Action</span><span class="sxs-lookup"><span data-stu-id="7f152-136">-Action</span></span>
<span data-ttu-id="7f152-137">Lista grup akcji dla alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-138">-DisableAlert</span></span>
<span data-ttu-id="7f152-139">Umożliwia użytkownikowi utworzenie wyłączanego alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="7f152-140">Jeśli nie podano, alerty są tworzone.</span><span class="sxs-lookup"><span data-stu-id="7f152-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-141">— Opis</span><span class="sxs-lookup"><span data-stu-id="7f152-141">-Description</span></span>
<span data-ttu-id="7f152-142">Opis zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="7f152-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f152-143">-Tag</span></span>
<span data-ttu-id="7f152-144">Ustawia właściwość Tagi dla zasobu alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="7f152-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f152-145">-InputObject</span></span>
<span data-ttu-id="7f152-146">Ustawia właściwość Inputobject dla połączenia, aby wyodrębnić nazwę wymaganą, oraz właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f152-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f152-147">-ResourceId</span></span>
<span data-ttu-id="7f152-148">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f152-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f152-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f152-149">-Confirm</span></span>
<span data-ttu-id="7f152-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f152-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f152-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f152-151">-DefaultProfile</span></span>
<span data-ttu-id="7f152-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f152-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f152-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f152-153">-WhatIf</span></span>
<span data-ttu-id="7f152-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f152-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f152-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f152-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f152-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f152-156">CommonParameters</span></span>
<span data-ttu-id="7f152-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f152-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f152-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f152-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f152-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f152-159">INPUTS</span></span>

## <span data-ttu-id="7f152-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f152-160">OUTPUTS</span></span>

### <span data-ttu-id="7f152-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="7f152-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="7f152-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f152-162">NOTES</span></span>

## <span data-ttu-id="7f152-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f152-163">RELATED LINKS</span></span>

[<span data-ttu-id="7f152-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f152-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f152-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f152-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f152-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f152-168">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f152-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="7f152-169">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="7f152-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
