---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181947"
---
# <span data-ttu-id="51bb2-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="51bb2-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="51bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="51bb2-103">Przypisywanie definicji planu do subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="51bb2-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="51bb2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51bb2-104">SYNTAX</span></span>

### <span data-ttu-id="51bb2-105">CreateBlueprintAssignment (domyślne)</span><span class="sxs-lookup"><span data-stu-id="51bb2-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51bb2-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="51bb2-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bb2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="51bb2-107">DESCRIPTION</span></span>
<span data-ttu-id="51bb2-108">Przypisywanie definicji planu do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51bb2-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="51bb2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="51bb2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51bb2-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="51bb2-111">Utwórz nowy przydział planu definicji planu w ramach określonej subskrypcji przy użyciu słownika zdefiniowanego `$blueprintObject` parametru i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51bb2-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="51bb2-112">Używa tożsamości przypisanej przez system.</span><span class="sxs-lookup"><span data-stu-id="51bb2-112">Uses system-assigned identity.</span></span> <span data-ttu-id="51bb2-113">Lokalizacja definiuje region tworzenia tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="51bb2-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="51bb2-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="51bb2-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="51bb2-115">Utwórz nowy przydział planu definicji planu w ramach określonej subskrypcji przy użyciu słownika zdefiniowanego parametru i grupy zasobów oraz konfigurując blokowanie zasobów `$blueprintObject` na **stronie AllResources.**</span><span class="sxs-lookup"><span data-stu-id="51bb2-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="51bb2-116">Domyślnie jest to używanie tożsamości przypisanej przez system.</span><span class="sxs-lookup"><span data-stu-id="51bb2-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="51bb2-117">Lokalizacja definiuje region tworzenia tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="51bb2-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="51bb2-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="51bb2-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="51bb2-119">Utwórz nowy przydział planu definicji planu w ramach określonej subskrypcji przy użyciu słownika zdefiniowanego parametru i grupy zasobów przy użyciu określonego identyfikatora tożsamości `$blueprintObject` przypisanego przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="51bb2-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="51bb2-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="51bb2-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="51bb2-121">Utwórz zadanie planu za pomocą pliku zadania.</span><span class="sxs-lookup"><span data-stu-id="51bb2-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="51bb2-122">Format pliku zadania można znaleźć w przykładach żądań/odpowiedzi pod: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="51bb2-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="51bb2-123">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="51bb2-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="51bb2-124">Utwórz nowy przydział planu definicji planu docelowej określonej subskrypcji w określonej grupie zarządzania przy `$blueprintObject` użyciu zdefiniowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="51bb2-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="51bb2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51bb2-125">PARAMETERS</span></span>

### <span data-ttu-id="51bb2-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="51bb2-126">-AssignmentFile</span></span>
<span data-ttu-id="51bb2-127">Lokalizacja pliku zadania w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="51bb2-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-128">—Plan</span><span class="sxs-lookup"><span data-stu-id="51bb2-128">-Blueprint</span></span>
<span data-ttu-id="51bb2-129">Obiekt definicji planu.</span><span class="sxs-lookup"><span data-stu-id="51bb2-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bb2-130">-DefaultProfile</span></span>
<span data-ttu-id="51bb2-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51bb2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51bb2-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="51bb2-132">-Location</span></span>
<span data-ttu-id="51bb2-133">Region dla tożsamości zarządzanej, w którym mają zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="51bb2-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="51bb2-134">Dowiedz się więcej na aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="51bb2-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-135">— Blokada</span><span class="sxs-lookup"><span data-stu-id="51bb2-135">-Lock</span></span>
<span data-ttu-id="51bb2-136">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="51bb2-136">Lock resources.</span></span>
<span data-ttu-id="51bb2-137">Dowiedz się więcej na aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="51bb2-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="51bb2-138">-ManagementGroupId</span></span>
<span data-ttu-id="51bb2-139">Identyfikator grupy zarządzania, w której zostaną zapisane przydziały Planu.</span><span class="sxs-lookup"><span data-stu-id="51bb2-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="51bb2-140">-Name</span></span>
<span data-ttu-id="51bb2-141">Nazwa zadania planu.</span><span class="sxs-lookup"><span data-stu-id="51bb2-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-142">- Parametr</span><span class="sxs-lookup"><span data-stu-id="51bb2-142">-Parameter</span></span>
<span data-ttu-id="51bb2-143">Parametry artefaktu.</span><span class="sxs-lookup"><span data-stu-id="51bb2-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-144">-ResourceGroupParameters</span><span class="sxs-lookup"><span data-stu-id="51bb2-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="51bb2-145">Hashtable of parameters to pass to the resource group artifact.</span><span class="sxs-lookup"><span data-stu-id="51bb2-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-146">-SecureStringParameters</span><span class="sxs-lookup"><span data-stu-id="51bb2-146">-SecureStringParameter</span></span>
<span data-ttu-id="51bb2-147">Parametr bezpiecznego ciągu dla identyfikatora zasobu KeyVault, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="51bb2-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-148">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51bb2-148">-SubscriptionId</span></span>
<span data-ttu-id="51bb2-149">Identyfikator subskrypcji do przypisania definicji planu.</span><span class="sxs-lookup"><span data-stu-id="51bb2-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="51bb2-150">Może być rozdzielaną przecinkami listą ciągów subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="51bb2-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="51bb2-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="51bb2-152">System przypisał tożsamość (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="51bb2-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="51bb2-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="51bb2-154">Tożsamość przypisana przez użytkownika (MSI, User Assigned Identity), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="51bb2-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bb2-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51bb2-155">-Confirm</span></span>
<span data-ttu-id="51bb2-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51bb2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51bb2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bb2-157">-WhatIf</span></span>
<span data-ttu-id="51bb2-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51bb2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51bb2-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51bb2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51bb2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bb2-160">CommonParameters</span></span>
<span data-ttu-id="51bb2-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bb2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bb2-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51bb2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bb2-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51bb2-163">INPUTS</span></span>

### <span data-ttu-id="51bb2-164">System.String</span><span class="sxs-lookup"><span data-stu-id="51bb2-164">System.String</span></span>

### <span data-ttu-id="51bb2-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="51bb2-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="51bb2-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="51bb2-166">System.String[]</span></span>

### <span data-ttu-id="51bb2-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="51bb2-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51bb2-168">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51bb2-168">OUTPUTS</span></span>

### <span data-ttu-id="51bb2-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="51bb2-169">System.Object</span></span>
## <span data-ttu-id="51bb2-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51bb2-170">NOTES</span></span>

## <span data-ttu-id="51bb2-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51bb2-171">RELATED LINKS</span></span>
