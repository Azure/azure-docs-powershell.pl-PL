---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200891"
---
# <span data-ttu-id="241cc-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="241cc-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="241cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="241cc-102">SYNOPSIS</span></span>
<span data-ttu-id="241cc-103">Aktualizowanie istniejącego przydziału planu.</span><span class="sxs-lookup"><span data-stu-id="241cc-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="241cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="241cc-104">SYNTAX</span></span>

### <span data-ttu-id="241cc-105">UpdateBlueprintAssignment (domyślne)</span><span class="sxs-lookup"><span data-stu-id="241cc-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="241cc-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="241cc-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241cc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="241cc-107">DESCRIPTION</span></span>
<span data-ttu-id="241cc-108">Aktualizowanie istniejącego przydziału planu.</span><span class="sxs-lookup"><span data-stu-id="241cc-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="241cc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="241cc-109">EXAMPLES</span></span>

### <span data-ttu-id="241cc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="241cc-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="241cc-111">Zaktualizuj istniejące przypisanie planu definicji planu w `$blueprintObject` ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="241cc-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="241cc-112">Używa tożsamości przypisanej przez system.</span><span class="sxs-lookup"><span data-stu-id="241cc-112">Uses system-assigned identity.</span></span> <span data-ttu-id="241cc-113">Lokalizacja definiuje region tworzenia tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="241cc-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="241cc-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="241cc-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="241cc-115">Zaktualizuj istniejące zadanie planu za pomocą pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="241cc-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="241cc-116">Format pliku zadania można znaleźć w przykładach żądań/odpowiedzi pod: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="241cc-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="241cc-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="241cc-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="241cc-118">Zaktualizuj istniejące przypisanie planu definicji planu docelowej określonej subskrypcji w określonej grupie zarządzania przy `$blueprintObject` użyciu zdefiniowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="241cc-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="241cc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="241cc-119">PARAMETERS</span></span>

### <span data-ttu-id="241cc-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="241cc-120">-AssignmentFile</span></span>
<span data-ttu-id="241cc-121">Lokalizacja pliku zadania w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="241cc-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-122">—Plan</span><span class="sxs-lookup"><span data-stu-id="241cc-122">-Blueprint</span></span>
<span data-ttu-id="241cc-123">Obiekt Plan.</span><span class="sxs-lookup"><span data-stu-id="241cc-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241cc-124">-DefaultProfile</span></span>
<span data-ttu-id="241cc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="241cc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="241cc-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="241cc-126">-Location</span></span>
<span data-ttu-id="241cc-127">Region dla tożsamości zarządzanej, w którym mają zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="241cc-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="241cc-128">Dowiedz się więcej na aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="241cc-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-129">— Blokada</span><span class="sxs-lookup"><span data-stu-id="241cc-129">-Lock</span></span>
<span data-ttu-id="241cc-130">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="241cc-130">Lock resources.</span></span>
<span data-ttu-id="241cc-131">Dowiedz się więcej na aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="241cc-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="241cc-132">-ManagementGroupId</span></span>
<span data-ttu-id="241cc-133">Identyfikator grupy zarządzania, w której zostaną zapisane przydziały Planu.</span><span class="sxs-lookup"><span data-stu-id="241cc-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="241cc-134">-Name</span></span>
<span data-ttu-id="241cc-135">Nazwa zadania planu.</span><span class="sxs-lookup"><span data-stu-id="241cc-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-136">- Parametr</span><span class="sxs-lookup"><span data-stu-id="241cc-136">-Parameter</span></span>
<span data-ttu-id="241cc-137">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="241cc-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-138">-ResourceGroupParameters</span><span class="sxs-lookup"><span data-stu-id="241cc-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="241cc-139">Hashtable of parameters to pass to the resource group artifact.</span><span class="sxs-lookup"><span data-stu-id="241cc-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-140">-SecureStringParameters</span><span class="sxs-lookup"><span data-stu-id="241cc-140">-SecureStringParameter</span></span>
<span data-ttu-id="241cc-141">Parametr bezpiecznego ciągu dla identyfikatora zasobu KeyVault, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="241cc-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-142">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="241cc-142">-SubscriptionId</span></span>
<span data-ttu-id="241cc-143">SubscriptionId to assign the Blueprint.</span><span class="sxs-lookup"><span data-stu-id="241cc-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="241cc-144">Może być rozdzielaną przecinkami listą ciągów subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="241cc-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="241cc-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="241cc-146">System przypisał tożsamość (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="241cc-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="241cc-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="241cc-148">Tożsamość przypisana przez użytkownika (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="241cc-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241cc-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="241cc-149">-Confirm</span></span>
<span data-ttu-id="241cc-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="241cc-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241cc-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241cc-151">-WhatIf</span></span>
<span data-ttu-id="241cc-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241cc-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241cc-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="241cc-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241cc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241cc-154">CommonParameters</span></span>
<span data-ttu-id="241cc-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241cc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241cc-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="241cc-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241cc-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="241cc-157">INPUTS</span></span>

### <span data-ttu-id="241cc-158">System.String</span><span class="sxs-lookup"><span data-stu-id="241cc-158">System.String</span></span>

### <span data-ttu-id="241cc-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="241cc-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="241cc-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="241cc-160">System.String[]</span></span>

### <span data-ttu-id="241cc-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="241cc-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="241cc-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="241cc-162">OUTPUTS</span></span>

### <span data-ttu-id="241cc-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="241cc-163">System.Object</span></span>
## <span data-ttu-id="241cc-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="241cc-164">NOTES</span></span>

## <span data-ttu-id="241cc-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="241cc-165">RELATED LINKS</span></span>
