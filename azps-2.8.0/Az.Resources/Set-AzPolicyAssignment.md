---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873283"
---
# <span data-ttu-id="37787-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37787-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="37787-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37787-102">SYNOPSIS</span></span>
<span data-ttu-id="37787-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="37787-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="37787-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37787-104">SYNTAX</span></span>

### <span data-ttu-id="37787-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37787-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37787-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37787-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37787-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="37787-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37787-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37787-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37787-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37787-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37787-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="37787-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37787-111">Opis</span><span class="sxs-lookup"><span data-stu-id="37787-111">DESCRIPTION</span></span>
<span data-ttu-id="37787-112">Polecenie cmdlet **Set-AzPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="37787-113">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="37787-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="37787-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37787-114">EXAMPLES</span></span>

### <span data-ttu-id="37787-115">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="37787-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="37787-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37787-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="37787-117">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37787-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="37787-118">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="37787-119">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="37787-120">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37787-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="37787-121">Przykład 2: Dodawanie zarządzanej tożsamości do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="37787-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="37787-122">Pierwsze polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="37787-123">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="37787-124">Polecenie ostatnie przypisuje zarządzaną tożsamość do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="37787-125">Przykład 3: aktualizowanie parametrów przypisywania zasad przy użyciu nowego obiektu parametru zasad</span><span class="sxs-lookup"><span data-stu-id="37787-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="37787-126">Pierwsze i drugie polecenie tworzy obiekt zawierający wszystkie regiony platformy Azure, których nazwy zaczynają się od nazw "Francja" lub "Wielka Brytania".</span><span class="sxs-lookup"><span data-stu-id="37787-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="37787-127">Drugie polecenie zapisuje ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="37787-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="37787-128">Trzecia komenda uzyskuje przypisanie zasad o nazwie "PolicyAssignment", to polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="37787-129">Ostatnie polecenie aktualizuje wartości parametrów w przydziale zasad o nazwie PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37787-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="37787-130">Przykład 4: aktualizowanie parametrów przypisywania zasad przy użyciu pliku parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="37787-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="37787-131">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="37787-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="37787-132">Polecenie aktualizuje przypisanie zasad o nazwie "PolicyAssignment" przy użyciu pliku z parametrem zasad, AllowedLocations.jsz lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="37787-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="37787-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37787-133">PARAMETERS</span></span>

### <span data-ttu-id="37787-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37787-134">-ApiVersion</span></span>
<span data-ttu-id="37787-135">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="37787-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="37787-136">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="37787-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="37787-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="37787-137">-AssignIdentity</span></span>
<span data-ttu-id="37787-138">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="37787-139">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="37787-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="37787-140">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="37787-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="37787-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37787-141">-DefaultProfile</span></span>
<span data-ttu-id="37787-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="37787-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37787-143">— Opis</span><span class="sxs-lookup"><span data-stu-id="37787-143">-Description</span></span>
<span data-ttu-id="37787-144">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="37787-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="37787-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37787-145">-DisplayName</span></span>
<span data-ttu-id="37787-146">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="37787-147">-ID</span><span class="sxs-lookup"><span data-stu-id="37787-147">-Id</span></span>
<span data-ttu-id="37787-148">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="37787-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="37787-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="37787-149">-Location</span></span>
<span data-ttu-id="37787-150">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="37787-151">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="37787-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="37787-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="37787-152">-Metadata</span></span>
<span data-ttu-id="37787-153">Zaktualizowane metadane przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="37787-154">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="37787-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="37787-155">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37787-155">-Name</span></span>
<span data-ttu-id="37787-156">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37787-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="37787-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="37787-157">-NotScope</span></span>
<span data-ttu-id="37787-158">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="37787-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="37787-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="37787-159">-PolicyParameter</span></span>
<span data-ttu-id="37787-160">Nowa ścieżka pliku parametrów zasad lub ciąg określający przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="37787-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="37787-161">-PolicyParameterObject</span></span>
<span data-ttu-id="37787-162">Nowy obiekt parametrów zasad dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="37787-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="37787-163">-Pre</span><span class="sxs-lookup"><span data-stu-id="37787-163">-Pre</span></span>
<span data-ttu-id="37787-164">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="37787-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="37787-165">-Zakres</span><span class="sxs-lookup"><span data-stu-id="37787-165">-Scope</span></span>
<span data-ttu-id="37787-166">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="37787-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="37787-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37787-167">CommonParameters</span></span>
<span data-ttu-id="37787-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37787-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37787-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37787-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37787-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37787-170">INPUTS</span></span>

### <span data-ttu-id="37787-171">System. String</span><span class="sxs-lookup"><span data-stu-id="37787-171">System.String</span></span>

### <span data-ttu-id="37787-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="37787-172">System.String[]</span></span>

## <span data-ttu-id="37787-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37787-173">OUTPUTS</span></span>

### <span data-ttu-id="37787-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="37787-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="37787-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37787-175">NOTES</span></span>

## <span data-ttu-id="37787-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37787-176">RELATED LINKS</span></span>

[<span data-ttu-id="37787-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37787-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="37787-178">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37787-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="37787-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37787-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


