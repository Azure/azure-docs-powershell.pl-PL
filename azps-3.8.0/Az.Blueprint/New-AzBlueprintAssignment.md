---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049602"
---
# <span data-ttu-id="34838-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="34838-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="34838-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34838-102">SYNOPSIS</span></span>
<span data-ttu-id="34838-103">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34838-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="34838-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34838-104">SYNTAX</span></span>

### <span data-ttu-id="34838-105">CreateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34838-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34838-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="34838-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34838-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34838-107">DESCRIPTION</span></span>
<span data-ttu-id="34838-108">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34838-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="34838-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34838-109">EXAMPLES</span></span>

### <span data-ttu-id="34838-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34838-110">Example 1</span></span>
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

<span data-ttu-id="34838-111">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="34838-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="34838-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="34838-112">Uses system-assigned identity.</span></span> <span data-ttu-id="34838-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="34838-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="34838-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="34838-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="34838-115">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grupy zasobów oraz konfigurowania blokowania zasobów na **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="34838-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="34838-116">Domyślnie jest używana tożsamość przypisana przez system.</span><span class="sxs-lookup"><span data-stu-id="34838-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="34838-117">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="34838-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="34838-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="34838-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="34838-119">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów przy użyciu określonego przez użytkownika identyfikatora tożsamości przypisanego do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34838-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="34838-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="34838-120">Example 4</span></span>
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

<span data-ttu-id="34838-121">Tworzenie zadania tworzenia planów za pośrednictwem pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="34838-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="34838-122">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="34838-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="34838-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34838-123">PARAMETERS</span></span>

### <span data-ttu-id="34838-124">-Plan</span><span class="sxs-lookup"><span data-stu-id="34838-124">-Blueprint</span></span>
<span data-ttu-id="34838-125">Obiekt definicji plany.</span><span class="sxs-lookup"><span data-stu-id="34838-125">Blueprint definition object.</span></span>

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

### <span data-ttu-id="34838-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34838-126">-DefaultProfile</span></span>
<span data-ttu-id="34838-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34838-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34838-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34838-128">-Location</span></span>
<span data-ttu-id="34838-129">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="34838-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="34838-130">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="34838-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="34838-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="34838-131">-Lock</span></span>
<span data-ttu-id="34838-132">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="34838-132">Lock resources.</span></span>
<span data-ttu-id="34838-133">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="34838-133">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="34838-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34838-134">-Name</span></span>
<span data-ttu-id="34838-135">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="34838-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="34838-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="34838-136">-Parameter</span></span>
<span data-ttu-id="34838-137">Parametry artefaktu.</span><span class="sxs-lookup"><span data-stu-id="34838-137">Artifact parameters.</span></span>

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

### <span data-ttu-id="34838-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="34838-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="34838-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="34838-139">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="34838-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="34838-140">-SecureStringParameter</span></span>
<span data-ttu-id="34838-141">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="34838-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="34838-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34838-142">-SubscriptionId</span></span>
<span data-ttu-id="34838-143">Identyfikator abonamentu umożliwiający przypisanie definicji plany.</span><span class="sxs-lookup"><span data-stu-id="34838-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="34838-144">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="34838-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="34838-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="34838-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="34838-146">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="34838-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="34838-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="34838-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="34838-148">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="34838-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="34838-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34838-149">-Confirm</span></span>
<span data-ttu-id="34838-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34838-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34838-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34838-151">-WhatIf</span></span>
<span data-ttu-id="34838-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34838-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34838-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34838-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34838-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34838-154">CommonParameters</span></span>
<span data-ttu-id="34838-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34838-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34838-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34838-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34838-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34838-157">INPUTS</span></span>

### <span data-ttu-id="34838-158">System. String</span><span class="sxs-lookup"><span data-stu-id="34838-158">System.String</span></span>

### <span data-ttu-id="34838-159">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="34838-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="34838-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="34838-160">System.String[]</span></span>

### <span data-ttu-id="34838-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34838-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="34838-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34838-162">OUTPUTS</span></span>

### <span data-ttu-id="34838-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="34838-163">System.Object</span></span>
## <span data-ttu-id="34838-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34838-164">NOTES</span></span>

## <span data-ttu-id="34838-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34838-165">RELATED LINKS</span></span>
