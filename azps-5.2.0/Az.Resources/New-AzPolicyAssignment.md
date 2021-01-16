---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357987"
---
# <span data-ttu-id="c945e-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c945e-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="c945e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c945e-102">SYNOPSIS</span></span>
<span data-ttu-id="c945e-103">Tworzy przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="c945e-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="c945e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c945e-104">SYNTAX</span></span>

### <span data-ttu-id="c945e-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c945e-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c945e-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c945e-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c945e-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c945e-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c945e-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c945e-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c945e-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c945e-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c945e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="c945e-110">DESCRIPTION</span></span>
<span data-ttu-id="c945e-111">Polecenie cmdlet **New-AzPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="c945e-112">Określ zasady i zakres.</span><span class="sxs-lookup"><span data-stu-id="c945e-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="c945e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c945e-113">EXAMPLES</span></span>

### <span data-ttu-id="c945e-114">Przykład 1: przydział zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c945e-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="c945e-115">Pierwsze polecenie pobiera abonament o nazwie Subscription01 przy użyciu polecenia cmdlet Get-AzSubscription i zapisuje go w zmiennej $Subscription.</span><span class="sxs-lookup"><span data-stu-id="c945e-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="c945e-116">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c945e-117">Polecenie ostatnie przypisuje zasady w $Policy na poziomie subskrypcji określonego przez ciąg zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c945e-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="c945e-118">Przykład 2: przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c945e-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c945e-119">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c945e-120">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c945e-121">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="c945e-122">Przykład 3: przydział zasad na poziomie grupy zasobów z obiektem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="c945e-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c945e-123">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c945e-124">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c945e-125">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c945e-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c945e-126">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="c945e-127">Trzecia i czwarta komenda Utwórz obiekt zawierający wszystkie regiony platformy Azure z nazwą "Wschód".</span><span class="sxs-lookup"><span data-stu-id="c945e-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="c945e-128">Te polecenia przechowują ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c945e-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="c945e-129">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu obiektu parametru zasad w $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c945e-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="c945e-130">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c945e-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c945e-131">Przykład 4: przydział zasad na poziomie grupy zasobów z plikiem parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="c945e-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="c945e-132">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="c945e-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="c945e-133">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c945e-134">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c945e-135">Polecenie ostatnie przypisuje zasady w $Policy w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup przy użyciu pliku z parametrem zasad AllowedLocations.jsna podstawie lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="c945e-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="c945e-136">Przykład 5: przypisanie zasad z tożsamością zarządzaną</span><span class="sxs-lookup"><span data-stu-id="c945e-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="c945e-137">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c945e-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c945e-138">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c945e-139">Polecenie ostatnie umożliwia przypisanie zasad w $Policy do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c945e-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="c945e-140">Zarządzana tożsamość zostanie automatycznie utworzona i przypisana do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="c945e-141">Przykład 6: przypisanie zasad z właściwością trybu wymuszania</span><span class="sxs-lookup"><span data-stu-id="c945e-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="c945e-142">Pierwsze polecenie pobiera abonament o nazwie Subscription01 przy użyciu polecenia cmdlet Get-AzSubscription i zapisuje go w zmiennej $Subscription.</span><span class="sxs-lookup"><span data-stu-id="c945e-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="c945e-143">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="c945e-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c945e-144">Polecenie ostatnie przypisuje zasady w $Policy na poziomie subskrypcji określonego przez ciąg zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c945e-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="c945e-145">Zadanie jest ustawione z wartością _DoNotEnforcemode_ , co oznacza, że efekt zasady nie jest wymuszany podczas tworzenia lub aktualizowania zasobu.</span><span class="sxs-lookup"><span data-stu-id="c945e-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="c945e-146">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c945e-146">PARAMETERS</span></span>

### <span data-ttu-id="c945e-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c945e-147">-ApiVersion</span></span>
<span data-ttu-id="c945e-148">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c945e-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c945e-149">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c945e-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c945e-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c945e-150">-AssignIdentity</span></span>
<span data-ttu-id="c945e-151">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="c945e-152">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="c945e-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="c945e-153">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c945e-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="c945e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c945e-154">-DefaultProfile</span></span>
<span data-ttu-id="c945e-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c945e-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c945e-156">— Opis</span><span class="sxs-lookup"><span data-stu-id="c945e-156">-Description</span></span>
<span data-ttu-id="c945e-157">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="c945e-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="c945e-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c945e-158">-DisplayName</span></span>
<span data-ttu-id="c945e-159">Określa nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="c945e-160">-Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c945e-160">-EnforcementMode</span></span>
<span data-ttu-id="c945e-161">Tryb wymuszania dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="c945e-162">Obecnie prawidłowymi wartościami są domyślne DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="c945e-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c945e-163">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c945e-163">-Location</span></span>
<span data-ttu-id="c945e-164">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="c945e-165">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="c945e-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="c945e-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c945e-166">-Metadata</span></span>
<span data-ttu-id="c945e-167">Metadane nowego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="c945e-168">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="c945e-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c945e-169">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c945e-169">-Name</span></span>
<span data-ttu-id="c945e-170">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="c945e-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c945e-171">-NotScope</span></span>
<span data-ttu-id="c945e-172">Nie zakresy przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="c945e-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c945e-173">-PolicyDefinition</span></span>
<span data-ttu-id="c945e-174">Określa zasadę, jako obiekt **PsPolicyDefinition** , który zawiera regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c945e-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c945e-175">-PolicyParameter</span></span>
<span data-ttu-id="c945e-176">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c945e-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c945e-177">-PolicyParameterObject</span></span>
<span data-ttu-id="c945e-178">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c945e-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c945e-179">-PolicySetDefinition</span></span>
<span data-ttu-id="c945e-180">Obiekt definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c945e-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c945e-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="c945e-181">-Pre</span></span>
<span data-ttu-id="c945e-182">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c945e-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c945e-183">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c945e-183">-Scope</span></span>
<span data-ttu-id="c945e-184">Określa zakres, do którego należy przypisać zasady.</span><span class="sxs-lookup"><span data-stu-id="c945e-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="c945e-185">Aby na przykład przypisać zasadę do grupy zasobów, określ następujące dane: `/subscriptions/` `/resourcegroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c945e-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="c945e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c945e-186">CommonParameters</span></span>
<span data-ttu-id="c945e-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c945e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c945e-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c945e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c945e-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c945e-189">INPUTS</span></span>

### <span data-ttu-id="c945e-190">System. String</span><span class="sxs-lookup"><span data-stu-id="c945e-190">System.String</span></span>

### <span data-ttu-id="c945e-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="c945e-191">System.String[]</span></span>

### <span data-ttu-id="c945e-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c945e-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c945e-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c945e-193">OUTPUTS</span></span>

### <span data-ttu-id="c945e-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c945e-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c945e-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c945e-195">NOTES</span></span>

## <span data-ttu-id="c945e-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c945e-196">RELATED LINKS</span></span>

[<span data-ttu-id="c945e-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c945e-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c945e-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c945e-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c945e-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c945e-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="c945e-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c945e-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


