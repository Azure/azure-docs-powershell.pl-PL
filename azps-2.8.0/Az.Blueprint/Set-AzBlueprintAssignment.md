---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706594"
---
# <span data-ttu-id="9c8df-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="9c8df-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="9c8df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c8df-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8df-103">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="9c8df-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9c8df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c8df-104">SYNTAX</span></span>

### <span data-ttu-id="9c8df-105">UpdateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c8df-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8df-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="9c8df-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c8df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9c8df-107">DESCRIPTION</span></span>
<span data-ttu-id="9c8df-108">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="9c8df-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9c8df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c8df-109">EXAMPLES</span></span>

### <span data-ttu-id="9c8df-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c8df-110">Example 1</span></span>
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

<span data-ttu-id="9c8df-111">Zaktualizuj istniejące zadanie tworzenia planów w definicji plany `$blueprintObject` w ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="9c8df-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="9c8df-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="9c8df-112">Uses system-assigned identity.</span></span> <span data-ttu-id="9c8df-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9c8df-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="9c8df-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9c8df-114">Example 2</span></span>
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

<span data-ttu-id="9c8df-115">Zaktualizuj istniejące zadanie tworzenia planów za pomocą pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="9c8df-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="9c8df-116">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="9c8df-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="9c8df-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c8df-117">PARAMETERS</span></span>

### <span data-ttu-id="9c8df-118">-Plan</span><span class="sxs-lookup"><span data-stu-id="9c8df-118">-Blueprint</span></span>
<span data-ttu-id="9c8df-119">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="9c8df-119">Blueprint object.</span></span>

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

### <span data-ttu-id="9c8df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8df-120">-DefaultProfile</span></span>
<span data-ttu-id="9c8df-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c8df-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9c8df-122">-Location</span></span>
<span data-ttu-id="9c8df-123">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="9c8df-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="9c8df-124">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="9c8df-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="9c8df-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="9c8df-125">-Lock</span></span>
<span data-ttu-id="9c8df-126">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c8df-126">Lock resources.</span></span>
<span data-ttu-id="9c8df-127">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="9c8df-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="9c8df-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c8df-128">-Name</span></span>
<span data-ttu-id="9c8df-129">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="9c8df-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="9c8df-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9c8df-130">-Parameter</span></span>
<span data-ttu-id="9c8df-131">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="9c8df-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="9c8df-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="9c8df-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="9c8df-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="9c8df-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="9c8df-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="9c8df-134">-SecureStringParameter</span></span>
<span data-ttu-id="9c8df-135">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="9c8df-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="9c8df-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9c8df-136">-SubscriptionId</span></span>
<span data-ttu-id="9c8df-137">Aby przypisać plan, należy uzyskać identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c8df-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="9c8df-138">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="9c8df-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="9c8df-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9c8df-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9c8df-140">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="9c8df-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="9c8df-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9c8df-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="9c8df-142">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="9c8df-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8df-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c8df-143">-Confirm</span></span>
<span data-ttu-id="9c8df-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8df-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c8df-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8df-145">-WhatIf</span></span>
<span data-ttu-id="9c8df-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8df-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8df-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c8df-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c8df-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8df-148">CommonParameters</span></span>
<span data-ttu-id="9c8df-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8df-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8df-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8df-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8df-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c8df-151">INPUTS</span></span>

### <span data-ttu-id="9c8df-152">System. String</span><span class="sxs-lookup"><span data-stu-id="9c8df-152">System.String</span></span>

### <span data-ttu-id="9c8df-153">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="9c8df-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="9c8df-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="9c8df-154">System.String[]</span></span>

### <span data-ttu-id="9c8df-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c8df-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c8df-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c8df-156">OUTPUTS</span></span>

### <span data-ttu-id="9c8df-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="9c8df-157">System.Object</span></span>
## <span data-ttu-id="9c8df-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c8df-158">NOTES</span></span>

## <span data-ttu-id="9c8df-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c8df-159">RELATED LINKS</span></span>
