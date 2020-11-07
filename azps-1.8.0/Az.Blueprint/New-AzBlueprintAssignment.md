---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869244"
---
# <span data-ttu-id="2cbfc-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2cbfc-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2cbfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbfc-103">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="2cbfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cbfc-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2cbfc-105">DESCRIPTION</span></span>
<span data-ttu-id="2cbfc-106">Przypisywanie definicji planów do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="2cbfc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cbfc-107">EXAMPLES</span></span>

### <span data-ttu-id="2cbfc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2cbfc-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="2cbfc-109">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="2cbfc-110">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-110">Uses system-assigned identity.</span></span> <span data-ttu-id="2cbfc-111">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="2cbfc-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2cbfc-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="2cbfc-113">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grupy zasobów oraz konfigurowania blokowania zasobów na **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="2cbfc-114">Domyślnie jest używana tożsamość przypisana przez system.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="2cbfc-115">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="2cbfc-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2cbfc-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="2cbfc-117">Utwórz nowe zadanie tworzenia zadania w definicji plany `$blueprintObject` w ramach określonej subskrypcji przy użyciu zdefiniowanego parametru i słownika grup zasobów przy użyciu określonego przez użytkownika identyfikatora tożsamości przypisanego do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="2cbfc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cbfc-118">PARAMETERS</span></span>

### <span data-ttu-id="2cbfc-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="2cbfc-119">-Blueprint</span></span>
<span data-ttu-id="2cbfc-120">Obiekt definicji plany.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="2cbfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbfc-121">-DefaultProfile</span></span>
<span data-ttu-id="2cbfc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cbfc-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2cbfc-123">-Location</span></span>
<span data-ttu-id="2cbfc-124">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="2cbfc-125">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="2cbfc-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="2cbfc-126">-Lock</span><span class="sxs-lookup"><span data-stu-id="2cbfc-126">-Lock</span></span>
<span data-ttu-id="2cbfc-127">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-127">Lock resources.</span></span>
<span data-ttu-id="2cbfc-128">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="2cbfc-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="2cbfc-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cbfc-129">-Name</span></span>
<span data-ttu-id="2cbfc-130">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2cbfc-131">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2cbfc-131">-Parameter</span></span>
<span data-ttu-id="2cbfc-132">Parametry artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="2cbfc-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="2cbfc-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="2cbfc-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="2cbfc-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="2cbfc-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="2cbfc-135">-SecureStringParameter</span></span>
<span data-ttu-id="2cbfc-136">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="2cbfc-137">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2cbfc-137">-SubscriptionId</span></span>
<span data-ttu-id="2cbfc-138">Identyfikator abonamentu umożliwiający przypisanie definicji plany.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="2cbfc-139">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="2cbfc-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2cbfc-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2cbfc-141">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2cbfc-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2cbfc-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="2cbfc-143">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2cbfc-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cbfc-144">-Confirm</span></span>
<span data-ttu-id="2cbfc-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbfc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbfc-146">-WhatIf</span></span>
<span data-ttu-id="2cbfc-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cbfc-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbfc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbfc-149">CommonParameters</span></span>
<span data-ttu-id="2cbfc-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbfc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbfc-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbfc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbfc-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cbfc-152">INPUTS</span></span>

### <span data-ttu-id="2cbfc-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2cbfc-153">System.String</span></span>

### <span data-ttu-id="2cbfc-154">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2cbfc-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2cbfc-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="2cbfc-155">System.String[]</span></span>

### <span data-ttu-id="2cbfc-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2cbfc-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2cbfc-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cbfc-157">OUTPUTS</span></span>

### <span data-ttu-id="2cbfc-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="2cbfc-158">System.Object</span></span>
## <span data-ttu-id="2cbfc-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cbfc-159">NOTES</span></span>

## <span data-ttu-id="2cbfc-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cbfc-160">RELATED LINKS</span></span>
