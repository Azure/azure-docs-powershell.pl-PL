---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372043"
---
# <span data-ttu-id="cd997-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cd997-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="cd997-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd997-102">SYNOPSIS</span></span>
<span data-ttu-id="cd997-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="cd997-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="cd997-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd997-104">SYNTAX</span></span>

### <span data-ttu-id="cd997-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd997-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd997-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd997-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd997-112">Opis</span><span class="sxs-lookup"><span data-stu-id="cd997-112">DESCRIPTION</span></span>
<span data-ttu-id="cd997-113">Polecenie cmdlet **Set-AzPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="cd997-114">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="cd997-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="cd997-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd997-115">EXAMPLES</span></span>

### <span data-ttu-id="cd997-116">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="cd997-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="cd997-117">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="cd997-118">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="cd997-119">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="cd997-120">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="cd997-121">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="cd997-122">Przykład 2: Dodawanie zarządzanej tożsamości do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="cd997-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="cd997-123">Pierwsze polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="cd997-124">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="cd997-125">Polecenie ostatnie przypisuje zarządzaną tożsamość do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="cd997-126">Przykład 3: aktualizowanie parametrów przypisywania zasad przy użyciu nowego obiektu parametru zasad</span><span class="sxs-lookup"><span data-stu-id="cd997-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="cd997-127">Pierwsze i drugie polecenie tworzy obiekt zawierający wszystkie regiony platformy Azure, których nazwy zaczynają się od nazw "Francja" lub "Wielka Brytania".</span><span class="sxs-lookup"><span data-stu-id="cd997-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="cd997-128">Drugie polecenie zapisuje ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="cd997-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="cd997-129">Trzecia komenda uzyskuje przypisanie zasad o nazwie "PolicyAssignment", to polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="cd997-130">Ostatnie polecenie aktualizuje wartości parametrów w przydziale zasad o nazwie PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="cd997-131">Przykład 4: aktualizowanie parametrów przypisywania zasad przy użyciu pliku parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="cd997-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="cd997-132">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="cd997-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="cd997-133">Polecenie aktualizuje przypisanie zasad o nazwie "PolicyAssignment" przy użyciu pliku z parametrem zasad, AllowedLocations.jsz lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="cd997-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="cd997-134">Przykład 5: aktualizowanie elementu wymuszania</span><span class="sxs-lookup"><span data-stu-id="cd997-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="cd997-135">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="cd997-136">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="cd997-137">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="cd997-138">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cd997-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="cd997-139">Polecenie ostatnie umożliwia zaktualizowanie właściwości wymuszenia w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd997-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="cd997-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd997-140">PARAMETERS</span></span>

### <span data-ttu-id="cd997-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cd997-141">-ApiVersion</span></span>
<span data-ttu-id="cd997-142">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="cd997-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cd997-143">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="cd997-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cd997-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd997-144">-AssignIdentity</span></span>
<span data-ttu-id="cd997-145">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="cd997-146">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="cd997-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="cd997-147">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cd997-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="cd997-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd997-148">-DefaultProfile</span></span>
<span data-ttu-id="cd997-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd997-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd997-150">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd997-150">-Description</span></span>
<span data-ttu-id="cd997-151">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="cd997-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="cd997-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd997-152">-DisplayName</span></span>
<span data-ttu-id="cd997-153">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="cd997-154">-Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cd997-154">-EnforcementMode</span></span>
<span data-ttu-id="cd997-155">Tryb wymuszania dla przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="cd997-156">Obecnie prawidłowymi wartościami są domyślne DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="cd997-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="cd997-157">-ID</span><span class="sxs-lookup"><span data-stu-id="cd997-157">-Id</span></span>
<span data-ttu-id="cd997-158">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="cd997-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd997-159">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd997-159">-InputObject</span></span>
<span data-ttu-id="cd997-160">Obiekt przydziału zasad umożliwiający zaktualizowanie danych wyjściowych z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd997-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="cd997-161">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd997-161">-Location</span></span>
<span data-ttu-id="cd997-162">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="cd997-163">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="cd997-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="cd997-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd997-164">-Metadata</span></span>
<span data-ttu-id="cd997-165">Zaktualizowane metadane przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="cd997-166">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="cd997-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="cd997-167">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd997-167">-Name</span></span>
<span data-ttu-id="cd997-168">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd997-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd997-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="cd997-169">-NotScope</span></span>
<span data-ttu-id="cd997-170">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="cd997-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="cd997-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="cd997-171">-PolicyParameter</span></span>
<span data-ttu-id="cd997-172">Nowa ścieżka pliku parametrów zasad lub ciąg określający przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="cd997-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="cd997-173">-PolicyParameterObject</span></span>
<span data-ttu-id="cd997-174">Nowy obiekt parametrów zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="cd997-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="cd997-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="cd997-175">-Pre</span></span>
<span data-ttu-id="cd997-176">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="cd997-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cd997-177">-Zakres</span><span class="sxs-lookup"><span data-stu-id="cd997-177">-Scope</span></span>
<span data-ttu-id="cd997-178">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="cd997-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="cd997-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd997-179">CommonParameters</span></span>
<span data-ttu-id="cd997-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd997-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd997-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd997-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd997-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd997-182">INPUTS</span></span>

### <span data-ttu-id="cd997-183">System. String</span><span class="sxs-lookup"><span data-stu-id="cd997-183">System.String</span></span>

### <span data-ttu-id="cd997-184">System. String []</span><span class="sxs-lookup"><span data-stu-id="cd997-184">System.String[]</span></span>

## <span data-ttu-id="cd997-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd997-185">OUTPUTS</span></span>

### <span data-ttu-id="cd997-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cd997-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cd997-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd997-187">NOTES</span></span>

## <span data-ttu-id="cd997-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd997-188">RELATED LINKS</span></span>

[<span data-ttu-id="cd997-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cd997-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="cd997-190">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cd997-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="cd997-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cd997-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


