---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062370"
---
# <span data-ttu-id="f932c-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="f932c-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="f932c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f932c-102">SYNOPSIS</span></span>
<span data-ttu-id="f932c-103">Przypisz definicję plany do subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f932c-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="f932c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f932c-104">SYNTAX</span></span>

### <span data-ttu-id="f932c-105">CreateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f932c-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f932c-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="f932c-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f932c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f932c-107">DESCRIPTION</span></span>
<span data-ttu-id="f932c-108">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f932c-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="f932c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f932c-109">EXAMPLES</span></span>

### <span data-ttu-id="f932c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f932c-110">Example 1</span></span>
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

<span data-ttu-id="f932c-111">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="f932c-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="f932c-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="f932c-112">Uses system-assigned identity.</span></span> <span data-ttu-id="f932c-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f932c-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="f932c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f932c-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="f932c-115">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grupy zasobów oraz konfigurowania blokowania zasobów na **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="f932c-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="f932c-116">Domyślnie jest używana tożsamość przypisana przez system.</span><span class="sxs-lookup"><span data-stu-id="f932c-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="f932c-117">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f932c-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="f932c-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f932c-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="f932c-119">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów przy użyciu określonego przez użytkownika identyfikatora tożsamości przypisanego do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f932c-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="f932c-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f932c-120">Example 4</span></span>
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

<span data-ttu-id="f932c-121">Tworzenie zadania tworzenia planów za pośrednictwem pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="f932c-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="f932c-122">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="f932c-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="f932c-123">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="f932c-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="f932c-124">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` ukierunkowanego na określoną subskrypcję w określonej grupie zarządzania przy użyciu zdefiniowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="f932c-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="f932c-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f932c-125">PARAMETERS</span></span>

### <span data-ttu-id="f932c-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="f932c-126">-AssignmentFile</span></span>
<span data-ttu-id="f932c-127">Lokalizacja pliku przydziału w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="f932c-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="f932c-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="f932c-128">-Blueprint</span></span>
<span data-ttu-id="f932c-129">Obiekt definicji plany.</span><span class="sxs-lookup"><span data-stu-id="f932c-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="f932c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f932c-130">-DefaultProfile</span></span>
<span data-ttu-id="f932c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f932c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f932c-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f932c-132">-Location</span></span>
<span data-ttu-id="f932c-133">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="f932c-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="f932c-134">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="f932c-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="f932c-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="f932c-135">-Lock</span></span>
<span data-ttu-id="f932c-136">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f932c-136">Lock resources.</span></span>
<span data-ttu-id="f932c-137">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="f932c-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="f932c-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f932c-138">-ManagementGroupId</span></span>
<span data-ttu-id="f932c-139">Identyfikator grupy zarządzania, w której zostaną zapisane zadania dotyczące planów.</span><span class="sxs-lookup"><span data-stu-id="f932c-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="f932c-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f932c-140">-Name</span></span>
<span data-ttu-id="f932c-141">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="f932c-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="f932c-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f932c-142">-Parameter</span></span>
<span data-ttu-id="f932c-143">Parametry artefaktu.</span><span class="sxs-lookup"><span data-stu-id="f932c-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="f932c-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="f932c-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="f932c-145">Hashtable parametrów, które zostaną przekazane do artefaktu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f932c-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="f932c-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="f932c-146">-SecureStringParameter</span></span>
<span data-ttu-id="f932c-147">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="f932c-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="f932c-148">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f932c-148">-SubscriptionId</span></span>
<span data-ttu-id="f932c-149">Identyfikator abonamentu umożliwiający przypisanie definicji plany.</span><span class="sxs-lookup"><span data-stu-id="f932c-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="f932c-150">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="f932c-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="f932c-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f932c-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="f932c-152">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="f932c-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="f932c-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f932c-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="f932c-154">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="f932c-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="f932c-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f932c-155">-Confirm</span></span>
<span data-ttu-id="f932c-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f932c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f932c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f932c-157">-WhatIf</span></span>
<span data-ttu-id="f932c-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f932c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f932c-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f932c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f932c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f932c-160">CommonParameters</span></span>
<span data-ttu-id="f932c-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f932c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f932c-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f932c-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f932c-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f932c-163">INPUTS</span></span>

### <span data-ttu-id="f932c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f932c-164">System.String</span></span>

### <span data-ttu-id="f932c-165">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="f932c-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="f932c-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="f932c-166">System.String[]</span></span>

### <span data-ttu-id="f932c-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f932c-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f932c-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f932c-168">OUTPUTS</span></span>

### <span data-ttu-id="f932c-169">System. Object</span><span class="sxs-lookup"><span data-stu-id="f932c-169">System.Object</span></span>
## <span data-ttu-id="f932c-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f932c-170">NOTES</span></span>

## <span data-ttu-id="f932c-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f932c-171">RELATED LINKS</span></span>
