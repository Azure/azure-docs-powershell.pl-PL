---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219570"
---
# <span data-ttu-id="a65b0-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a65b0-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a65b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a65b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a65b0-103">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a65b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a65b0-104">SYNTAX</span></span>

### <span data-ttu-id="a65b0-105">UpdateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a65b0-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65b0-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="a65b0-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a65b0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a65b0-107">DESCRIPTION</span></span>
<span data-ttu-id="a65b0-108">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a65b0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a65b0-109">EXAMPLES</span></span>

### <span data-ttu-id="a65b0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a65b0-110">Example 1</span></span>
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

<span data-ttu-id="a65b0-111">Zaktualizuj istniejące zadanie tworzenia planów w definicji plany `$blueprintObject` w ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="a65b0-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="a65b0-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="a65b0-112">Uses system-assigned identity.</span></span> <span data-ttu-id="a65b0-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a65b0-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="a65b0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a65b0-114">Example 2</span></span>
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

<span data-ttu-id="a65b0-115">Zaktualizuj istniejące zadanie tworzenia planów za pomocą pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="a65b0-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="a65b0-116">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="a65b0-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="a65b0-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a65b0-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="a65b0-118">Zaktualizuj istniejące zadanie tworzenia planów dotyczące definicji planów `$blueprintObject` ukierunkowanej na określoną subskrypcję w określonej grupie zarządzania przy użyciu zdefiniowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="a65b0-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="a65b0-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a65b0-119">PARAMETERS</span></span>

### <span data-ttu-id="a65b0-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="a65b0-120">-AssignmentFile</span></span>
<span data-ttu-id="a65b0-121">Lokalizacja pliku przydziału w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="a65b0-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="a65b0-122">-Plan</span><span class="sxs-lookup"><span data-stu-id="a65b0-122">-Blueprint</span></span>
<span data-ttu-id="a65b0-123">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="a65b0-123">Blueprint object.</span></span>

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

### <span data-ttu-id="a65b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65b0-124">-DefaultProfile</span></span>
<span data-ttu-id="a65b0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a65b0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65b0-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a65b0-126">-Location</span></span>
<span data-ttu-id="a65b0-127">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="a65b0-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="a65b0-128">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="a65b0-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="a65b0-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="a65b0-129">-Lock</span></span>
<span data-ttu-id="a65b0-130">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-130">Lock resources.</span></span>
<span data-ttu-id="a65b0-131">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="a65b0-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="a65b0-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a65b0-132">-ManagementGroupId</span></span>
<span data-ttu-id="a65b0-133">Identyfikator grupy zarządzania, w której zostaną zapisane zadania dotyczące planów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="a65b0-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a65b0-134">-Name</span></span>
<span data-ttu-id="a65b0-135">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="a65b0-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="a65b0-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a65b0-136">-Parameter</span></span>
<span data-ttu-id="a65b0-137">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="a65b0-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="a65b0-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a65b0-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="a65b0-139">Hashtable parametrów, które zostaną przekazane do artefaktu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="a65b0-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="a65b0-140">-SecureStringParameter</span></span>
<span data-ttu-id="a65b0-141">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="a65b0-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="a65b0-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a65b0-142">-SubscriptionId</span></span>
<span data-ttu-id="a65b0-143">Aby przypisać plan, należy uzyskać identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a65b0-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="a65b0-144">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="a65b0-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a65b0-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a65b0-146">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="a65b0-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a65b0-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a65b0-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="a65b0-148">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="a65b0-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a65b0-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a65b0-149">-Confirm</span></span>
<span data-ttu-id="a65b0-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a65b0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65b0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65b0-151">-WhatIf</span></span>
<span data-ttu-id="a65b0-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a65b0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65b0-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a65b0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65b0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65b0-154">CommonParameters</span></span>
<span data-ttu-id="a65b0-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65b0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65b0-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a65b0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65b0-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a65b0-157">INPUTS</span></span>

### <span data-ttu-id="a65b0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="a65b0-158">System.String</span></span>

### <span data-ttu-id="a65b0-159">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a65b0-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a65b0-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="a65b0-160">System.String[]</span></span>

### <span data-ttu-id="a65b0-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a65b0-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a65b0-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a65b0-162">OUTPUTS</span></span>

### <span data-ttu-id="a65b0-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="a65b0-163">System.Object</span></span>
## <span data-ttu-id="a65b0-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a65b0-164">NOTES</span></span>

## <span data-ttu-id="a65b0-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a65b0-165">RELATED LINKS</span></span>
