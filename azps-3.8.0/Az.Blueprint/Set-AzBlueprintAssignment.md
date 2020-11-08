---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049952"
---
# <span data-ttu-id="2bd1f-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2bd1f-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2bd1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd1f-103">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2bd1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bd1f-104">SYNTAX</span></span>

### <span data-ttu-id="2bd1f-105">UpdateBlueprintAssignment (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2bd1f-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd1f-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="2bd1f-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bd1f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2bd1f-107">DESCRIPTION</span></span>
<span data-ttu-id="2bd1f-108">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2bd1f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bd1f-109">EXAMPLES</span></span>

### <span data-ttu-id="2bd1f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bd1f-110">Example 1</span></span>
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

<span data-ttu-id="2bd1f-111">Zaktualizuj istniejące zadanie tworzenia planów w definicji plany `$blueprintObject` w ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="2bd1f-112">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-112">Uses system-assigned identity.</span></span> <span data-ttu-id="2bd1f-113">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="2bd1f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2bd1f-114">Example 2</span></span>
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

<span data-ttu-id="2bd1f-115">Zaktualizuj istniejące zadanie tworzenia planów za pomocą pliku przydziału.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="2bd1f-116">Format pliku przydziału można znaleźć w przykładach żądania/odpowiedzi: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="2bd1f-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="2bd1f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bd1f-117">PARAMETERS</span></span>

### <span data-ttu-id="2bd1f-118">-Plan</span><span class="sxs-lookup"><span data-stu-id="2bd1f-118">-Blueprint</span></span>
<span data-ttu-id="2bd1f-119">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-119">Blueprint object.</span></span>

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

### <span data-ttu-id="2bd1f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd1f-120">-DefaultProfile</span></span>
<span data-ttu-id="2bd1f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd1f-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2bd1f-122">-Location</span></span>
<span data-ttu-id="2bd1f-123">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="2bd1f-124">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="2bd1f-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="2bd1f-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="2bd1f-125">-Lock</span></span>
<span data-ttu-id="2bd1f-126">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-126">Lock resources.</span></span>
<span data-ttu-id="2bd1f-127">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="2bd1f-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="2bd1f-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2bd1f-128">-Name</span></span>
<span data-ttu-id="2bd1f-129">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2bd1f-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd1f-130">-Parameter</span></span>
<span data-ttu-id="2bd1f-131">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="2bd1f-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="2bd1f-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="2bd1f-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="2bd1f-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="2bd1f-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="2bd1f-134">-SecureStringParameter</span></span>
<span data-ttu-id="2bd1f-135">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="2bd1f-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2bd1f-136">-SubscriptionId</span></span>
<span data-ttu-id="2bd1f-137">Aby przypisać plan, należy uzyskać identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="2bd1f-138">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="2bd1f-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2bd1f-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2bd1f-140">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2bd1f-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2bd1f-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="2bd1f-142">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2bd1f-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2bd1f-143">-Confirm</span></span>
<span data-ttu-id="2bd1f-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd1f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd1f-145">-WhatIf</span></span>
<span data-ttu-id="2bd1f-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd1f-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd1f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd1f-148">CommonParameters</span></span>
<span data-ttu-id="2bd1f-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd1f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd1f-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd1f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd1f-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bd1f-151">INPUTS</span></span>

### <span data-ttu-id="2bd1f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd1f-152">System.String</span></span>

### <span data-ttu-id="2bd1f-153">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2bd1f-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2bd1f-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="2bd1f-154">System.String[]</span></span>

### <span data-ttu-id="2bd1f-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2bd1f-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2bd1f-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bd1f-156">OUTPUTS</span></span>

### <span data-ttu-id="2bd1f-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="2bd1f-157">System.Object</span></span>
## <span data-ttu-id="2bd1f-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bd1f-158">NOTES</span></span>

## <span data-ttu-id="2bd1f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bd1f-159">RELATED LINKS</span></span>
