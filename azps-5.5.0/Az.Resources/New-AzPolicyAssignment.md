---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242530"
---
# <span data-ttu-id="8a431-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8a431-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="8a431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a431-102">SYNOPSIS</span></span>
<span data-ttu-id="8a431-103">Tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="8a431-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a431-104">SYNTAX</span></span>

### <span data-ttu-id="8a431-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8a431-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a431-106">PolicyParametersObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a431-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a431-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a431-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a431-108">PolicySetParametersObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a431-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a431-109">PolicySetParametersStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a431-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a431-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a431-110">DESCRIPTION</span></span>
<span data-ttu-id="8a431-111">Polecenie **cmdlet New-AzPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="8a431-112">Określanie zasad i zakresu.</span><span class="sxs-lookup"><span data-stu-id="8a431-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="8a431-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a431-113">EXAMPLES</span></span>

### <span data-ttu-id="8a431-114">Przykład 1. Przypisanie zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8a431-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="8a431-115">Pierwsze polecenie otrzymuje subskrypcję o nazwie Subscription01 przy użyciu polecenia cmdlet Get-AzSubscription i zapisuje je w $Subscription danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="8a431-116">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy, używając polecenia cmdlet Get-AzPolicyDefinition i przechowuje je w $Policy danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="8a431-117">Ostatnie polecenie przypisuje zasady w $Policy na poziomie subskrypcji wskazanym przez ciąg zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a431-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="8a431-118">Przykład 2. Przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8a431-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="8a431-119">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje je w zmiennej $ResourceGroup zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8a431-120">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy, używając polecenia cmdlet Get-AzPolicyDefinition i przechowuje je w $Policy danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="8a431-121">Ostatnie polecenie przypisuje zasady w $Policy na poziomie grupy zasobów wskazanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a431-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="8a431-122">Przykład 3. Przypisanie zasad na poziomie grupy zasobów z obiektem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="8a431-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="8a431-123">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a431-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8a431-124">Polecenie przechowuje ten obiekt w $ResourceGroup zmienną.</span><span class="sxs-lookup"><span data-stu-id="8a431-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8a431-125">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a431-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8a431-126">Polecenie przechowuje ten obiekt w $Policy zmienną.</span><span class="sxs-lookup"><span data-stu-id="8a431-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="8a431-127">Trzecie i czwarte polecenia tworzą obiekt zawierający wszystkie regiony platformy Azure o nazwie "wschód".</span><span class="sxs-lookup"><span data-stu-id="8a431-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="8a431-128">Polecenia przechowują ten obiekt w $AllowedLocations zmienną.</span><span class="sxs-lookup"><span data-stu-id="8a431-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="8a431-129">Ostatnie polecenie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu obiektu parametru zasad w $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="8a431-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="8a431-130">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="8a431-131">Przykład 4. Przydział zasad na poziomie grupy zasobów z plikiem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="8a431-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="8a431-132">Utwórz plik o _nazwieAllowedLocations.jsw_ lokalnym katalogu pracy z następującą zawartością.</span><span class="sxs-lookup"><span data-stu-id="8a431-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="8a431-133">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje je w zmiennej $ResourceGroup zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8a431-134">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w $Policy danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="8a431-135">Ostatnie polecenie przypisuje zasady w programie $Policy w grupie zasobów wskazanej przez właściwość **ResourceId** programu $ResourceGroup przy użyciu pliku parametru zasad, który AllowedLocations.jsz lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="8a431-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="8a431-136">Przykład 5. Przypisanie zasad z tożsamością zarządzaną</span><span class="sxs-lookup"><span data-stu-id="8a431-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="8a431-137">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje je w zmiennej $ResourceGroup zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8a431-138">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy, używając polecenia cmdlet Get-AzPolicyDefinition i przechowuje je w $Policy danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="8a431-139">Ostatnie polecenie przypisuje zasady w $Policy do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="8a431-140">Tożsamość zarządzana jest tworzona automatycznie i przypisywana do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="8a431-141">Przykład 6. Przypisanie zasad z właściwością trybu wymuszania</span><span class="sxs-lookup"><span data-stu-id="8a431-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="8a431-142">Pierwsze polecenie otrzymuje subskrypcję o nazwie Subscription01 przy użyciu polecenia cmdlet Get-AzSubscription i zapisuje je w $Subscription danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="8a431-143">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy, używając polecenia cmdlet Get-AzPolicyDefinition i przechowuje je w $Policy danych.</span><span class="sxs-lookup"><span data-stu-id="8a431-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="8a431-144">Ostatnie polecenie przypisuje zasady w $Policy na poziomie subskrypcji wskazanym przez ciąg zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a431-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="8a431-145">Przypisanie jest ustawiane z wartością EnforcementMode (Tryb wymuszania) usługi _DoNotEnforce,_ czyli efekt zasad nie jest wymuszany podczas tworzenia lub aktualizowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a431-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="8a431-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a431-146">PARAMETERS</span></span>

### <span data-ttu-id="8a431-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a431-147">-ApiVersion</span></span>
<span data-ttu-id="8a431-148">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="8a431-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8a431-149">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="8a431-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8a431-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8a431-150">-AssignIdentity</span></span>
<span data-ttu-id="8a431-151">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="8a431-152">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="8a431-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="8a431-153">Podczas przypisywania tożsamości wymagana jest lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="8a431-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="8a431-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a431-154">-DefaultProfile</span></span>
<span data-ttu-id="8a431-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8a431-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a431-156">— Opis</span><span class="sxs-lookup"><span data-stu-id="8a431-156">-Description</span></span>
<span data-ttu-id="8a431-157">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="8a431-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="8a431-158">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a431-158">-DisplayName</span></span>
<span data-ttu-id="8a431-159">Określa nazwę wyświetlaną przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="8a431-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="8a431-160">-EnforcementMode</span></span>
<span data-ttu-id="8a431-161">Tryb wymuszania przypisywania zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="8a431-162">Obecnie prawidłowe wartości to Domyślne (DoNotEnforce).</span><span class="sxs-lookup"><span data-stu-id="8a431-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="8a431-163">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8a431-163">-Location</span></span>
<span data-ttu-id="8a431-164">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="8a431-165">Jest to wymagane, gdy jest używany przełącznik -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="8a431-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="8a431-166">— Metadane</span><span class="sxs-lookup"><span data-stu-id="8a431-166">-Metadata</span></span>
<span data-ttu-id="8a431-167">Metadane dla nowego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="8a431-168">Może to być ścieżka do nazwy pliku zawierającej metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="8a431-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="8a431-169">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a431-169">-Name</span></span>
<span data-ttu-id="8a431-170">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="8a431-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="8a431-171">-NotScope</span></span>
<span data-ttu-id="8a431-172">Zakresy nie przypisywania zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="8a431-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a431-173">-PolicyDefinition</span></span>
<span data-ttu-id="8a431-174">Określa zasady jako obiekt **PsPolicyDefinition** zawierający regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="8a431-175">-PolicyParameters</span><span class="sxs-lookup"><span data-stu-id="8a431-175">-PolicyParameter</span></span>
<span data-ttu-id="8a431-176">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="8a431-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="8a431-177">-PolicyParameterObject</span></span>
<span data-ttu-id="8a431-178">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="8a431-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="8a431-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8a431-179">-PolicySetDefinition</span></span>
<span data-ttu-id="8a431-180">Obiekt definicji ustawiany przez zasady.</span><span class="sxs-lookup"><span data-stu-id="8a431-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="8a431-181">— Przed</span><span class="sxs-lookup"><span data-stu-id="8a431-181">-Pre</span></span>
<span data-ttu-id="8a431-182">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="8a431-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a431-183">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8a431-183">-Scope</span></span>
<span data-ttu-id="8a431-184">Określa zakres, do którego mają zostać przypisane zasady.</span><span class="sxs-lookup"><span data-stu-id="8a431-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="8a431-185">Aby na przykład przypisać zasady do grupy zasobów, określ następujące elementy: nazwa grupy zasobów identyfikatora `/subscriptions/` `/resourcegroups/` subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8a431-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="8a431-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a431-186">CommonParameters</span></span>
<span data-ttu-id="8a431-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a431-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a431-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a431-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a431-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a431-189">INPUTS</span></span>

### <span data-ttu-id="8a431-190">System.String</span><span class="sxs-lookup"><span data-stu-id="8a431-190">System.String</span></span>

### <span data-ttu-id="8a431-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8a431-191">System.String[]</span></span>

### <span data-ttu-id="8a431-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8a431-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8a431-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a431-193">OUTPUTS</span></span>

### <span data-ttu-id="8a431-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8a431-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8a431-195">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a431-195">NOTES</span></span>

## <span data-ttu-id="8a431-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a431-196">RELATED LINKS</span></span>

[<span data-ttu-id="8a431-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a431-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8a431-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8a431-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="8a431-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8a431-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="8a431-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8a431-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


