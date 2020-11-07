---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869248"
---
# <span data-ttu-id="e5b0c-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b0c-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e5b0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b0c-103">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e5b0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5b0c-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5b0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b0c-106">Zaktualizuj istniejące zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e5b0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b0c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5b0c-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="e5b0c-109">Zaktualizuj istniejące zadanie tworzenia planów w definicji plany `$blueprintObject` w ramach określonej subskrypcji, aktualizując parametry.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="e5b0c-110">Używa tożsamości przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-110">Uses system-assigned identity.</span></span> <span data-ttu-id="e5b0c-111">Lokalizacja określa region tworzenia zarządzanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="e5b0c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="e5b0c-113">-Plan</span><span class="sxs-lookup"><span data-stu-id="e5b0c-113">-Blueprint</span></span>
<span data-ttu-id="e5b0c-114">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-114">Blueprint object.</span></span>

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

### <span data-ttu-id="e5b0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b0c-115">-DefaultProfile</span></span>
<span data-ttu-id="e5b0c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b0c-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e5b0c-117">-Location</span></span>
<span data-ttu-id="e5b0c-118">Region, w którym ma zostać utworzona zarządzana tożsamość.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e5b0c-119">Dowiedz się więcej pod adresem aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e5b0c-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e5b0c-120">-Lock</span><span class="sxs-lookup"><span data-stu-id="e5b0c-120">-Lock</span></span>
<span data-ttu-id="e5b0c-121">Blokowanie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-121">Lock resources.</span></span>
<span data-ttu-id="e5b0c-122">Dowiedz się więcej pod adresem aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e5b0c-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e5b0c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5b0c-123">-Name</span></span>
<span data-ttu-id="e5b0c-124">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e5b0c-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e5b0c-125">-Parameter</span></span>
<span data-ttu-id="e5b0c-126">Parametr artefaktu.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="e5b0c-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e5b0c-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="e5b0c-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="e5b0c-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="e5b0c-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e5b0c-129">-SecureStringParameter</span></span>
<span data-ttu-id="e5b0c-130">Parametr Secure String dla identyfikatora zasobu magazynu, nazwy i wersji.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e5b0c-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e5b0c-131">-SubscriptionId</span></span>
<span data-ttu-id="e5b0c-132">Aby przypisać plan, należy uzyskać identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="e5b0c-133">Może być listą rozdzielanych przecinkami ciągów.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e5b0c-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e5b0c-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e5b0c-135">Tożsamość przypisana przez system (MSI), aby wdrożyć artefakty.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e5b0c-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e5b0c-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="e5b0c-137">Tożsamość użytkownika została przypisana (MSI) w celu wdrożenia artefaktów.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e5b0c-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5b0c-138">-Confirm</span></span>
<span data-ttu-id="e5b0c-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b0c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b0c-140">-WhatIf</span></span>
<span data-ttu-id="e5b0c-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b0c-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b0c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b0c-143">CommonParameters</span></span>
<span data-ttu-id="e5b0c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b0c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b0c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b0c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5b0c-146">INPUTS</span></span>

### <span data-ttu-id="e5b0c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b0c-147">System.String</span></span>

### <span data-ttu-id="e5b0c-148">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e5b0c-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e5b0c-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="e5b0c-149">System.String[]</span></span>

### <span data-ttu-id="e5b0c-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5b0c-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5b0c-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5b0c-151">OUTPUTS</span></span>

### <span data-ttu-id="e5b0c-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="e5b0c-152">System.Object</span></span>
## <span data-ttu-id="e5b0c-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5b0c-153">NOTES</span></span>

## <span data-ttu-id="e5b0c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5b0c-154">RELATED LINKS</span></span>
