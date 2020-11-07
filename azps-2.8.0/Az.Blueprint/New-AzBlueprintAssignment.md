---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 6adc5674674de903b30993b09d5bb680f8569398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706603"
---
# <span data-ttu-id="63370-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="63370-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="63370-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63370-102">SYNOPSIS</span></span>
<span data-ttu-id="63370-103">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="63370-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="63370-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63370-104">SYNTAX</span></span>

### <span data-ttu-id="63370-105">CreateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63370-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63370-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="63370-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63370-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63370-107">DESCRIPTION</span></span>
<span data-ttu-id="63370-108">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="63370-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="63370-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63370-109">EXAMPLES</span></span>

### <span data-ttu-id="63370-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63370-110">Example 1</span></span>
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

<span data-ttu-id="63370-111">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="63370-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="63370-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="63370-112">Uses system-assigned identity.</span></span> <span data-ttu-id="63370-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="63370-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="63370-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="63370-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="63370-115">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grupy zasobów oraz konfigurowania blokowania zasobów na **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="63370-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="63370-116">Domyślnie jest używana tożsamość przypisana przez system.</span><span class="sxs-lookup"><span data-stu-id="63370-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="63370-117">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="63370-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="63370-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="63370-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="63370-119">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów przy użyciu określonego przez użytkownika identyfikatora tożsamości przypisanego do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="63370-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="63370-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="63370-120">Example 4</span></span>
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

<span data-ttu-id="63370-121">Tworzenie zadania tworzenia planów za pośrednictwem pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="63370-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="63370-122">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="63370-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="63370-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63370-123">PARAMETERS</span></span>

### <span data-ttu-id="63370-124">-Plan</span><span class="sxs-lookup"><span data-stu-id="63370-124">-Blueprint</span></span>
<span data-ttu-id="63370-125">Obiekt definicji plany.</span><span class="sxs-lookup"><span data-stu-id="63370-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63370-126">-DefaultProfile</span></span>
<span data-ttu-id="63370-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63370-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63370-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="63370-128">-Location</span></span>
<span data-ttu-id="63370-129">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="63370-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="63370-130">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="63370-130">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="63370-131">-Lock</span></span>
<span data-ttu-id="63370-132">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="63370-132">Lock resources.</span></span>
<span data-ttu-id="63370-133">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="63370-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63370-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63370-134">-Name</span></span>
<span data-ttu-id="63370-135">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="63370-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="63370-136">-Parameter</span></span>
<span data-ttu-id="63370-137">Parametry artefaktu.</span><span class="sxs-lookup"><span data-stu-id="63370-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="63370-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="63370-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="63370-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="63370-140">-SecureStringParameter</span></span>
<span data-ttu-id="63370-141">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="63370-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63370-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="63370-142">-SubscriptionId</span></span>
<span data-ttu-id="63370-143">Identyfikator abonamentu umożliwiający przypisanie definicji plany.</span><span class="sxs-lookup"><span data-stu-id="63370-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="63370-144">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="63370-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="63370-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="63370-146">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="63370-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="63370-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="63370-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="63370-148">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="63370-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63370-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63370-149">-Confirm</span></span>
<span data-ttu-id="63370-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63370-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63370-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63370-151">-WhatIf</span></span>
<span data-ttu-id="63370-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63370-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63370-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63370-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63370-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63370-154">CommonParameters</span></span>
<span data-ttu-id="63370-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63370-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63370-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63370-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63370-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63370-157">INPUTS</span></span>

### <span data-ttu-id="63370-158">System. String</span><span class="sxs-lookup"><span data-stu-id="63370-158">System.String</span></span>

### <span data-ttu-id="63370-159">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="63370-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="63370-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="63370-160">System.String[]</span></span>

### <span data-ttu-id="63370-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63370-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="63370-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63370-162">OUTPUTS</span></span>

### <span data-ttu-id="63370-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="63370-163">System.Object</span></span>
## <span data-ttu-id="63370-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63370-164">NOTES</span></span>

## <span data-ttu-id="63370-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63370-165">RELATED LINKS</span></span>
