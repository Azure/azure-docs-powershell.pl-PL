---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326541"
---
# <span data-ttu-id="cfb05-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="cfb05-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="cfb05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfb05-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb05-103">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="cfb05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfb05-104">SYNTAX</span></span>

### <span data-ttu-id="cfb05-105">UpdateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cfb05-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfb05-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="cfb05-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfb05-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cfb05-107">DESCRIPTION</span></span>
<span data-ttu-id="cfb05-108">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="cfb05-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfb05-109">EXAMPLES</span></span>

### <span data-ttu-id="cfb05-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cfb05-110">Example 1</span></span>
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

<span data-ttu-id="cfb05-111">Zaktualizuj istniejące zadanie tworzenia planów w definicji plany `$blueprintObject` w ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="cfb05-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="cfb05-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="cfb05-112">Uses system-assigned identity.</span></span> <span data-ttu-id="cfb05-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cfb05-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="cfb05-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cfb05-114">Example 2</span></span>
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

<span data-ttu-id="cfb05-115">Zaktualizuj istniejące zadanie tworzenia planów za pomocą pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="cfb05-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="cfb05-116">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="cfb05-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="cfb05-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cfb05-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="cfb05-118">Zaktualizuj istniejące zadanie tworzenia planów dotyczące definicji planów `$blueprintObject` ukierunkowanej na określoną subskrypcję w określonej grupie zarządzania przy użyciu zdefiniowanego parametru.</span><span class="sxs-lookup"><span data-stu-id="cfb05-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="cfb05-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfb05-119">PARAMETERS</span></span>

### <span data-ttu-id="cfb05-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="cfb05-120">-AssignmentFile</span></span>
<span data-ttu-id="cfb05-121">Lokalizacja pliku przydziału w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="cfb05-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="cfb05-122">-Plan</span><span class="sxs-lookup"><span data-stu-id="cfb05-122">-Blueprint</span></span>
<span data-ttu-id="cfb05-123">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="cfb05-123">Blueprint object.</span></span>

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

### <span data-ttu-id="cfb05-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb05-124">-DefaultProfile</span></span>
<span data-ttu-id="cfb05-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb05-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb05-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cfb05-126">-Location</span></span>
<span data-ttu-id="cfb05-127">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="cfb05-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="cfb05-128">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="cfb05-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="cfb05-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="cfb05-129">-Lock</span></span>
<span data-ttu-id="cfb05-130">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-130">Lock resources.</span></span>
<span data-ttu-id="cfb05-131">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="cfb05-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="cfb05-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="cfb05-132">-ManagementGroupId</span></span>
<span data-ttu-id="cfb05-133">Identyfikator grupy zarządzania, w której zostaną zapisane zadania dotyczące planów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="cfb05-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfb05-134">-Name</span></span>
<span data-ttu-id="cfb05-135">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="cfb05-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="cfb05-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb05-136">-Parameter</span></span>
<span data-ttu-id="cfb05-137">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="cfb05-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="cfb05-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="cfb05-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="cfb05-139">Hashtable parametrów, które zostaną przekazane do artefaktu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="cfb05-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="cfb05-140">-SecureStringParameter</span></span>
<span data-ttu-id="cfb05-141">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="cfb05-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="cfb05-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cfb05-142">-SubscriptionId</span></span>
<span data-ttu-id="cfb05-143">Aby przypisać plan, należy uzyskać identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cfb05-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="cfb05-144">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="cfb05-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cfb05-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="cfb05-146">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="cfb05-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="cfb05-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cfb05-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="cfb05-148">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="cfb05-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="cfb05-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfb05-149">-Confirm</span></span>
<span data-ttu-id="cfb05-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfb05-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb05-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb05-151">-WhatIf</span></span>
<span data-ttu-id="cfb05-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfb05-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfb05-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfb05-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb05-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb05-154">CommonParameters</span></span>
<span data-ttu-id="cfb05-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb05-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb05-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfb05-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb05-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfb05-157">INPUTS</span></span>

### <span data-ttu-id="cfb05-158">System. String</span><span class="sxs-lookup"><span data-stu-id="cfb05-158">System.String</span></span>

### <span data-ttu-id="cfb05-159">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="cfb05-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="cfb05-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="cfb05-160">System.String[]</span></span>

### <span data-ttu-id="cfb05-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfb05-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfb05-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfb05-162">OUTPUTS</span></span>

### <span data-ttu-id="cfb05-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="cfb05-163">System.Object</span></span>
## <span data-ttu-id="cfb05-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfb05-164">NOTES</span></span>

## <span data-ttu-id="cfb05-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfb05-165">RELATED LINKS</span></span>
