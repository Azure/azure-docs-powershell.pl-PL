---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549567"
---
# <span data-ttu-id="1f14a-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f14a-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="1f14a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f14a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f14a-103">Tworzy przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="1f14a-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f14a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f14a-104">SYNTAX</span></span>

### <span data-ttu-id="1f14a-105">CreateWithoutParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f14a-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f14a-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1f14a-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f14a-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="1f14a-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f14a-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="1f14a-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f14a-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="1f14a-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1f14a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1f14a-110">DESCRIPTION</span></span>
<span data-ttu-id="1f14a-111">Polecenie cmdlet **New-AzureRmPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="1f14a-112">Określ zasady i zakres.</span><span class="sxs-lookup"><span data-stu-id="1f14a-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="1f14a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f14a-113">EXAMPLES</span></span>

### <span data-ttu-id="1f14a-114">Przykład 1: przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1f14a-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1f14a-115">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="1f14a-116">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="1f14a-117">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1f14a-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1f14a-118">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1f14a-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="1f14a-119">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f14a-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="1f14a-120">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f14a-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1f14a-121">Przykład 2: przydział zasad na poziomie grupy zasobów z obiektem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="1f14a-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1f14a-122">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="1f14a-123">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="1f14a-124">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1f14a-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1f14a-125">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1f14a-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="1f14a-126">Trzecia i czwarta komenda Utwórz obiekt zawierający wszystkie regiony platformy Azure z nazwą "Wschód".</span><span class="sxs-lookup"><span data-stu-id="1f14a-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="1f14a-127">Te polecenia przechowują ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="1f14a-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="1f14a-128">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu obiektu parametru zasad w $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="1f14a-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="1f14a-129">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f14a-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1f14a-130">Przykład 3: przydział zasad na poziomie grupy zasobów z plikiem parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="1f14a-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="1f14a-131">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="1f14a-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="1f14a-132">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="1f14a-133">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f14a-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="1f14a-134">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1f14a-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1f14a-135">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1f14a-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="1f14a-136">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu pliku z parametrem zasad AllowedLocations.jsna podstawie lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="1f14a-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="1f14a-137">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f14a-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="1f14a-138">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f14a-138">PARAMETERS</span></span>

### <span data-ttu-id="1f14a-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f14a-139">-ApiVersion</span></span>
<span data-ttu-id="1f14a-140">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1f14a-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f14a-141">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="1f14a-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f14a-142">-DefaultProfile</span></span>
<span data-ttu-id="1f14a-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1f14a-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-144">— Opis</span><span class="sxs-lookup"><span data-stu-id="1f14a-144">-Description</span></span>
<span data-ttu-id="1f14a-145">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="1f14a-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f14a-146">-DisplayName</span></span>
<span data-ttu-id="1f14a-147">Określa nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1f14a-148">-InformationAction</span></span>
<span data-ttu-id="1f14a-149">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1f14a-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1f14a-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1f14a-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f14a-151">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1f14a-151">Continue</span></span>
- <span data-ttu-id="1f14a-152">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1f14a-152">Ignore</span></span>
- <span data-ttu-id="1f14a-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="1f14a-153">Inquire</span></span>
- <span data-ttu-id="1f14a-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1f14a-154">SilentlyContinue</span></span>
- <span data-ttu-id="1f14a-155">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1f14a-155">Stop</span></span>
- <span data-ttu-id="1f14a-156">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1f14a-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1f14a-157">-InformationVariable</span></span>
<span data-ttu-id="1f14a-158">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1f14a-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f14a-159">-Name</span></span>
<span data-ttu-id="1f14a-160">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1f14a-161">-NotScope</span></span>
<span data-ttu-id="1f14a-162">Nie zakresy przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f14a-163">-PolicyDefinition</span></span>
<span data-ttu-id="1f14a-164">Określa zasadę, jako obiekt **PSObject** , który zawiera regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1f14a-165">-PolicyParameter</span></span>
<span data-ttu-id="1f14a-166">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1f14a-167">-PolicyParameterObject</span></span>
<span data-ttu-id="1f14a-168">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1f14a-169">-PolicySetDefinition</span></span>
<span data-ttu-id="1f14a-170">Obiekt definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1f14a-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f14a-171">-Pre</span></span>
<span data-ttu-id="1f14a-172">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="1f14a-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-173">-Zakres</span><span class="sxs-lookup"><span data-stu-id="1f14a-173">-Scope</span></span>
<span data-ttu-id="1f14a-174">Określa zakres, do którego należy przypisać zasady.</span><span class="sxs-lookup"><span data-stu-id="1f14a-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="1f14a-175">Aby na przykład przypisać zasadę do grupy zasobów, określ następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="1f14a-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="1f14a-176">`/subscriptions/``/resourcegroups/`Nazwa grupy zasobów identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1f14a-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="1f14a-177">-Sku</span></span>
<span data-ttu-id="1f14a-178">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="1f14a-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="1f14a-179">Domyślnie jest to bezpłatna wersja jednostki SKU: Nazwa = a0, warstwa = FRE</span><span class="sxs-lookup"><span data-stu-id="1f14a-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f14a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f14a-180">CommonParameters</span></span>
<span data-ttu-id="1f14a-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f14a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f14a-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f14a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f14a-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f14a-183">INPUTS</span></span>

### <span data-ttu-id="1f14a-184">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f14a-184">None</span></span>
<span data-ttu-id="1f14a-185">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1f14a-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f14a-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f14a-186">OUTPUTS</span></span>

### <span data-ttu-id="1f14a-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1f14a-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f14a-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f14a-188">NOTES</span></span>

## <span data-ttu-id="1f14a-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f14a-189">RELATED LINKS</span></span>

[<span data-ttu-id="1f14a-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f14a-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1f14a-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f14a-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1f14a-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f14a-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1f14a-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f14a-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


