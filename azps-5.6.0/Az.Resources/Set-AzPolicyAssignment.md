---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: dcfc63c1dbf36cf7c592fe8fc7eb5afae09dc4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011770"
---
# <span data-ttu-id="6552b-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6552b-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="6552b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6552b-102">SYNOPSIS</span></span>
<span data-ttu-id="6552b-103">Modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="6552b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6552b-104">SYNTAX</span></span>

### <span data-ttu-id="6552b-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6552b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-106">PolicyParametersNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-107">PolicyParametersNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6552b-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6552b-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6552b-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="6552b-112">DESCRIPTION</span></span>
<span data-ttu-id="6552b-113">Polecenie **cmdlet Set-AzPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="6552b-114">Określanie zadania według identyfikatora lub nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="6552b-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="6552b-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6552b-115">EXAMPLES</span></span>

### <span data-ttu-id="6552b-116">Przykład 1. Aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="6552b-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="6552b-117">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6552b-118">Polecenie przechowuje ten obiekt w $ResourceGroup zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6552b-119">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment przy użyciu Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6552b-120">Polecenie przechowuje ten obiekt w $PolicyAssignment zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6552b-121">Ostatnie polecenie aktualizuje nazwę wyświetlaną przydziału zasad w grupie zasobów wskazanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6552b-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="6552b-122">Przykład 2. Dodawanie tożsamości zarządzanej do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="6552b-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="6552b-123">Pierwsze polecenie pobiera przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji za pomocą Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6552b-124">Polecenie przechowuje ten obiekt w $PolicyAssignment zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6552b-125">Ostatnie polecenie przypisuje tożsamość zarządzaną do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="6552b-126">Przykład 3. Aktualizowanie parametrów przypisywania zasad za pomocą nowego obiektu parametru zasad</span><span class="sxs-lookup"><span data-stu-id="6552b-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="6552b-127">Pierwsze i drugie polecenia tworzą obiekt zawierający wszystkie regiony platformy Azure, których nazwy zaczynają się od "france" lub "uk".</span><span class="sxs-lookup"><span data-stu-id="6552b-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="6552b-128">Drugie polecenie przechowuje ten obiekt w $AllowedLocations zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="6552b-129">Trzecie polecenie pobiera przypisanie zasad o nazwie "PolicyAssignment" Polecenie przechowuje ten obiekt w $PolicyAssignment zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6552b-130">Ostatnie polecenie aktualizuje wartości parametrów w przypisaniu zasad o nazwie PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="6552b-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="6552b-131">Przykład 4. Aktualizowanie parametrów przypisywania zasad za pomocą pliku parametru zasad</span><span class="sxs-lookup"><span data-stu-id="6552b-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="6552b-132">Utwórz plik o _nazwieAllowedLocations.jsw_ lokalnym katalogu pracy z następującą zawartością.</span><span class="sxs-lookup"><span data-stu-id="6552b-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="6552b-133">Polecenie aktualizuje przypisanie zasad o nazwie "PolicyAssignment" przy użyciu pliku parametru zasadAllowedLocations.jswł. z lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="6552b-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="6552b-134">Przykład 5. Aktualizowanie trybu wymuszania</span><span class="sxs-lookup"><span data-stu-id="6552b-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="6552b-135">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6552b-136">Polecenie przechowuje ten obiekt w $ResourceGroup zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6552b-137">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment przy użyciu Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6552b-138">Polecenie przechowuje ten obiekt w $PolicyAssignment zmienną.</span><span class="sxs-lookup"><span data-stu-id="6552b-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6552b-139">Ostatnie polecenie aktualizuje właściwość EnforcementMode przydziału zasad dla grupy zasobów wskazanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6552b-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="6552b-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6552b-140">PARAMETERS</span></span>

### <span data-ttu-id="6552b-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6552b-141">-ApiVersion</span></span>
<span data-ttu-id="6552b-142">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="6552b-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6552b-143">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="6552b-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6552b-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6552b-144">-AssignIdentity</span></span>
<span data-ttu-id="6552b-145">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="6552b-146">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="6552b-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="6552b-147">Podczas przypisywania tożsamości wymagana jest lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="6552b-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="6552b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6552b-148">-DefaultProfile</span></span>
<span data-ttu-id="6552b-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6552b-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6552b-150">— Opis</span><span class="sxs-lookup"><span data-stu-id="6552b-150">-Description</span></span>
<span data-ttu-id="6552b-151">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="6552b-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="6552b-152">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="6552b-152">-DisplayName</span></span>
<span data-ttu-id="6552b-153">Określa nową nazwę wyświetlaną dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="6552b-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="6552b-154">-EnforcementMode</span></span>
<span data-ttu-id="6552b-155">Tryb wymuszania przypisywania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="6552b-156">Obecnie prawidłowe wartości to Domyślne (DoNotEnforce).</span><span class="sxs-lookup"><span data-stu-id="6552b-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="6552b-157">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="6552b-157">-Id</span></span>
<span data-ttu-id="6552b-158">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="6552b-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6552b-159">-InputObject</span></span>
<span data-ttu-id="6552b-160">Obiekt przypisywania zasad do aktualizowania danych wyjściowych z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6552b-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-161">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6552b-161">-Location</span></span>
<span data-ttu-id="6552b-162">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="6552b-163">Jest to wymagane, gdy jest używany przełącznik -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="6552b-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="6552b-164">— Metadane</span><span class="sxs-lookup"><span data-stu-id="6552b-164">-Metadata</span></span>
<span data-ttu-id="6552b-165">Zaktualizowane metadane dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="6552b-166">Może to być ścieżka do nazwy pliku zawierającej metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="6552b-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="6552b-167">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6552b-167">-Name</span></span>
<span data-ttu-id="6552b-168">Określa nazwę przydziału zasad, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="6552b-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="6552b-169">-NotScope</span></span>
<span data-ttu-id="6552b-170">Przydział zasad nie ma zakresów.</span><span class="sxs-lookup"><span data-stu-id="6552b-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="6552b-171">-PolicyParameters</span><span class="sxs-lookup"><span data-stu-id="6552b-171">-PolicyParameter</span></span>
<span data-ttu-id="6552b-172">Ścieżka pliku nowych parametrów zasad lub ciąg dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="6552b-173">-PolicyParameterObject</span></span>
<span data-ttu-id="6552b-174">Obiekt parametrów nowych zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-175">— Przed</span><span class="sxs-lookup"><span data-stu-id="6552b-175">-Pre</span></span>
<span data-ttu-id="6552b-176">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="6552b-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6552b-177">— Zakres</span><span class="sxs-lookup"><span data-stu-id="6552b-177">-Scope</span></span>
<span data-ttu-id="6552b-178">Określa zakres stosowania zasad.</span><span class="sxs-lookup"><span data-stu-id="6552b-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6552b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6552b-179">CommonParameters</span></span>
<span data-ttu-id="6552b-180">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6552b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6552b-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6552b-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6552b-182">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6552b-182">INPUTS</span></span>

### <span data-ttu-id="6552b-183">System.String</span><span class="sxs-lookup"><span data-stu-id="6552b-183">System.String</span></span>

### <span data-ttu-id="6552b-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6552b-184">System.String[]</span></span>

## <span data-ttu-id="6552b-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6552b-185">OUTPUTS</span></span>

### <span data-ttu-id="6552b-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6552b-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6552b-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6552b-187">NOTES</span></span>

## <span data-ttu-id="6552b-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6552b-188">RELATED LINKS</span></span>

[<span data-ttu-id="6552b-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6552b-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="6552b-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6552b-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="6552b-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6552b-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


