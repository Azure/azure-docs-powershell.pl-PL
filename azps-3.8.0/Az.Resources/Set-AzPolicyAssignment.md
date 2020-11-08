---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050702"
---
# <span data-ttu-id="fe28d-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fe28d-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="fe28d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe28d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe28d-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="fe28d-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="fe28d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe28d-104">SYNTAX</span></span>

### <span data-ttu-id="fe28d-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe28d-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe28d-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe28d-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe28d-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe28d-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe28d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe28d-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe28d-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe28d-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe28d-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe28d-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe28d-111">Opis</span><span class="sxs-lookup"><span data-stu-id="fe28d-111">DESCRIPTION</span></span>
<span data-ttu-id="fe28d-112">Polecenie cmdlet **Set-AzPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="fe28d-113">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="fe28d-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="fe28d-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe28d-114">EXAMPLES</span></span>

### <span data-ttu-id="fe28d-115">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="fe28d-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="fe28d-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="fe28d-117">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fe28d-118">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="fe28d-119">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fe28d-120">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="fe28d-121">Przykład 2: Dodawanie zarządzanej tożsamości do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="fe28d-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="fe28d-122">Pierwsze polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="fe28d-123">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fe28d-124">Polecenie ostatnie przypisuje zarządzaną tożsamość do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="fe28d-125">Przykład 3: aktualizowanie parametrów przypisywania zasad przy użyciu nowego obiektu parametru zasad</span><span class="sxs-lookup"><span data-stu-id="fe28d-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="fe28d-126">Pierwsze i drugie polecenie tworzy obiekt zawierający wszystkie regiony platformy Azure, których nazwy zaczynają się od nazw "Francja" lub "Wielka Brytania".</span><span class="sxs-lookup"><span data-stu-id="fe28d-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="fe28d-127">Drugie polecenie zapisuje ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="fe28d-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="fe28d-128">Trzecia komenda uzyskuje przypisanie zasad o nazwie "PolicyAssignment", to polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fe28d-129">Ostatnie polecenie aktualizuje wartości parametrów w przydziale zasad o nazwie PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="fe28d-130">Przykład 4: aktualizowanie parametrów przypisywania zasad przy użyciu pliku parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="fe28d-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="fe28d-131">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="fe28d-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="fe28d-132">Polecenie aktualizuje przypisanie zasad o nazwie "PolicyAssignment" przy użyciu pliku z parametrem zasad, AllowedLocations.jsz lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="fe28d-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="fe28d-133">Przykład 5: aktualizowanie elementu wymuszania</span><span class="sxs-lookup"><span data-stu-id="fe28d-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="fe28d-134">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="fe28d-135">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fe28d-136">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="fe28d-137">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fe28d-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fe28d-138">Polecenie ostatnie umożliwia zaktualizowanie właściwości wymuszenia w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe28d-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="fe28d-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe28d-139">PARAMETERS</span></span>

### <span data-ttu-id="fe28d-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe28d-140">-ApiVersion</span></span>
<span data-ttu-id="fe28d-141">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="fe28d-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe28d-142">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="fe28d-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fe28d-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fe28d-143">-AssignIdentity</span></span>
<span data-ttu-id="fe28d-144">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="fe28d-145">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="fe28d-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="fe28d-146">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="fe28d-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="fe28d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe28d-147">-DefaultProfile</span></span>
<span data-ttu-id="fe28d-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe28d-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe28d-149">— Opis</span><span class="sxs-lookup"><span data-stu-id="fe28d-149">-Description</span></span>
<span data-ttu-id="fe28d-150">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="fe28d-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="fe28d-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe28d-151">-DisplayName</span></span>
<span data-ttu-id="fe28d-152">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="fe28d-153">-Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fe28d-153">-EnforcementMode</span></span>
<span data-ttu-id="fe28d-154">Tryb wymuszania dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="fe28d-155">Obecnie prawidłowymi wartościami są domyślne DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="fe28d-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="fe28d-156">-ID</span><span class="sxs-lookup"><span data-stu-id="fe28d-156">-Id</span></span>
<span data-ttu-id="fe28d-157">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="fe28d-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fe28d-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fe28d-158">-Location</span></span>
<span data-ttu-id="fe28d-159">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="fe28d-160">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="fe28d-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="fe28d-161">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fe28d-161">-Metadata</span></span>
<span data-ttu-id="fe28d-162">Zaktualizowane metadane przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="fe28d-163">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="fe28d-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="fe28d-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe28d-164">-Name</span></span>
<span data-ttu-id="fe28d-165">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe28d-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fe28d-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="fe28d-166">-NotScope</span></span>
<span data-ttu-id="fe28d-167">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="fe28d-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="fe28d-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="fe28d-168">-PolicyParameter</span></span>
<span data-ttu-id="fe28d-169">Nowa ścieżka pliku parametrów zasad lub ciąg określający przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-169">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="fe28d-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe28d-170">-PolicyParameterObject</span></span>
<span data-ttu-id="fe28d-171">Nowy obiekt parametrów zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="fe28d-171">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="fe28d-172">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe28d-172">-Pre</span></span>
<span data-ttu-id="fe28d-173">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="fe28d-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fe28d-174">-Zakres</span><span class="sxs-lookup"><span data-stu-id="fe28d-174">-Scope</span></span>
<span data-ttu-id="fe28d-175">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="fe28d-175">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="fe28d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe28d-176">CommonParameters</span></span>
<span data-ttu-id="fe28d-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe28d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe28d-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe28d-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe28d-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe28d-179">INPUTS</span></span>

### <span data-ttu-id="fe28d-180">System. String</span><span class="sxs-lookup"><span data-stu-id="fe28d-180">System.String</span></span>

### <span data-ttu-id="fe28d-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="fe28d-181">System.String[]</span></span>

## <span data-ttu-id="fe28d-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe28d-182">OUTPUTS</span></span>

### <span data-ttu-id="fe28d-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fe28d-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fe28d-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe28d-184">NOTES</span></span>

## <span data-ttu-id="fe28d-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe28d-185">RELATED LINKS</span></span>

[<span data-ttu-id="fe28d-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fe28d-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="fe28d-187">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fe28d-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="fe28d-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fe28d-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


