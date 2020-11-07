---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: bec39b242de14da944496a4371fa661d95ce9c59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873359"
---
# <span data-ttu-id="3eae9-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3eae9-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="3eae9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3eae9-102">SYNOPSIS</span></span>
<span data-ttu-id="3eae9-103">Tworzy przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="3eae9-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="3eae9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3eae9-104">SYNTAX</span></span>

### <span data-ttu-id="3eae9-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3eae9-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eae9-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eae9-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eae9-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eae9-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eae9-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eae9-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eae9-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eae9-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eae9-110">Opis</span><span class="sxs-lookup"><span data-stu-id="3eae9-110">DESCRIPTION</span></span>
<span data-ttu-id="3eae9-111">Polecenie cmdlet **New-AzPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="3eae9-112">Określ zasady i zakres.</span><span class="sxs-lookup"><span data-stu-id="3eae9-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="3eae9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3eae9-113">EXAMPLES</span></span>

### <span data-ttu-id="3eae9-114">Przykład 1: przydział zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3eae9-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="3eae9-115">Pierwsze polecenie pobiera abonament o nazwie Subscription01 przy użyciu polecenia cmdlet Get-AzSubscription i zapisuje go w zmiennej $Subscription.</span><span class="sxs-lookup"><span data-stu-id="3eae9-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="3eae9-116">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="3eae9-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3eae9-117">Polecenie ostatnie przypisuje zasady w $Policy na poziomie subskrypcji określonego przez ciąg zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3eae9-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="3eae9-118">Przykład 2: przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3eae9-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="3eae9-119">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3eae9-120">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="3eae9-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3eae9-121">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="3eae9-122">Przykład 3: przydział zasad na poziomie grupy zasobów z obiektem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="3eae9-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="3eae9-123">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3eae9-124">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3eae9-125">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3eae9-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3eae9-126">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="3eae9-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="3eae9-127">Trzecia i czwarta komenda Utwórz obiekt zawierający wszystkie regiony platformy Azure z nazwą "Wschód".</span><span class="sxs-lookup"><span data-stu-id="3eae9-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="3eae9-128">Te polecenia przechowują ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="3eae9-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="3eae9-129">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu obiektu parametru zasad w $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="3eae9-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="3eae9-130">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="3eae9-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3eae9-131">Przykład 4: przydział zasad na poziomie grupy zasobów z plikiem parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="3eae9-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="3eae9-132">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="3eae9-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="3eae9-133">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3eae9-134">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="3eae9-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3eae9-135">Polecenie ostatnie przypisuje zasady w $Policy w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup przy użyciu pliku z parametrem zasad AllowedLocations.jsna podstawie lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="3eae9-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="3eae9-136">Przykład 5: przypisanie zasad z tożsamością zarządzaną</span><span class="sxs-lookup"><span data-stu-id="3eae9-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="3eae9-137">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3eae9-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3eae9-138">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="3eae9-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3eae9-139">Polecenie ostatnie umożliwia przypisanie zasad w $Policy do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3eae9-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="3eae9-140">Zarządzana tożsamość zostanie automatycznie utworzona i przypisana do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="3eae9-141">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3eae9-141">PARAMETERS</span></span>

### <span data-ttu-id="3eae9-142">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3eae9-142">-ApiVersion</span></span>
<span data-ttu-id="3eae9-143">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3eae9-143">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3eae9-144">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="3eae9-144">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3eae9-145">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3eae9-145">-AssignIdentity</span></span>
<span data-ttu-id="3eae9-146">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-146">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="3eae9-147">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="3eae9-147">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="3eae9-148">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="3eae9-148">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="3eae9-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eae9-149">-DefaultProfile</span></span>
<span data-ttu-id="3eae9-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3eae9-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eae9-151">— Opis</span><span class="sxs-lookup"><span data-stu-id="3eae9-151">-Description</span></span>
<span data-ttu-id="3eae9-152">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="3eae9-152">The description for policy assignment</span></span>

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

### <span data-ttu-id="3eae9-153">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3eae9-153">-DisplayName</span></span>
<span data-ttu-id="3eae9-154">Określa nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-154">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="3eae9-155">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3eae9-155">-Location</span></span>
<span data-ttu-id="3eae9-156">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-156">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="3eae9-157">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="3eae9-157">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="3eae9-158">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3eae9-158">-Metadata</span></span>
<span data-ttu-id="3eae9-159">Metadane nowego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-159">The metadata for the new policy assignment.</span></span> <span data-ttu-id="3eae9-160">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="3eae9-160">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="3eae9-161">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3eae9-161">-Name</span></span>
<span data-ttu-id="3eae9-162">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-162">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="3eae9-163">-NotScope</span><span class="sxs-lookup"><span data-stu-id="3eae9-163">-NotScope</span></span>
<span data-ttu-id="3eae9-164">Nie zakresy przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-164">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="3eae9-165">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3eae9-165">-PolicyDefinition</span></span>
<span data-ttu-id="3eae9-166">Określa zasadę, jako obiekt **PsPolicyDefinition** , który zawiera regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-166">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eae9-167">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="3eae9-167">-PolicyParameter</span></span>
<span data-ttu-id="3eae9-168">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-168">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="3eae9-169">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3eae9-169">-PolicyParameterObject</span></span>
<span data-ttu-id="3eae9-170">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-170">The policy parameter object.</span></span>

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

### <span data-ttu-id="3eae9-171">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3eae9-171">-PolicySetDefinition</span></span>
<span data-ttu-id="3eae9-172">Obiekt definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="3eae9-172">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eae9-173">-Pre</span><span class="sxs-lookup"><span data-stu-id="3eae9-173">-Pre</span></span>
<span data-ttu-id="3eae9-174">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="3eae9-174">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3eae9-175">-Zakres</span><span class="sxs-lookup"><span data-stu-id="3eae9-175">-Scope</span></span>
<span data-ttu-id="3eae9-176">Określa zakres, do którego należy przypisać zasady.</span><span class="sxs-lookup"><span data-stu-id="3eae9-176">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="3eae9-177">Aby na przykład przypisać zasadę do grupy zasobów, określ następujące dane: `/subscriptions/` `/resourcegroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3eae9-177">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="3eae9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eae9-178">CommonParameters</span></span>
<span data-ttu-id="3eae9-179">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eae9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eae9-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3eae9-180">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eae9-181">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3eae9-181">INPUTS</span></span>

### <span data-ttu-id="3eae9-182">System. String</span><span class="sxs-lookup"><span data-stu-id="3eae9-182">System.String</span></span>

### <span data-ttu-id="3eae9-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="3eae9-183">System.String[]</span></span>

### <span data-ttu-id="3eae9-184">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3eae9-184">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3eae9-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3eae9-185">OUTPUTS</span></span>

### <span data-ttu-id="3eae9-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3eae9-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3eae9-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3eae9-187">NOTES</span></span>

## <span data-ttu-id="3eae9-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3eae9-188">RELATED LINKS</span></span>

[<span data-ttu-id="3eae9-189">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3eae9-189">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="3eae9-190">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3eae9-190">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="3eae9-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3eae9-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="3eae9-192">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3eae9-192">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


