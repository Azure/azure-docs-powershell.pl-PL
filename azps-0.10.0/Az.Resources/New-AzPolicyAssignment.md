---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892498"
---
# <span data-ttu-id="1ca90-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ca90-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="1ca90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ca90-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca90-103">Tworzy przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="1ca90-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="1ca90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ca90-104">SYNTAX</span></span>

### <span data-ttu-id="1ca90-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ca90-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1ca90-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1ca90-110">DESCRIPTION</span></span>
<span data-ttu-id="1ca90-111">Polecenie cmdlet **New-AzPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="1ca90-112">Określ zasady i zakres.</span><span class="sxs-lookup"><span data-stu-id="1ca90-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="1ca90-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ca90-113">EXAMPLES</span></span>

### <span data-ttu-id="1ca90-114">Przykład 1: przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1ca90-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1ca90-115">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ca90-116">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1ca90-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ca90-117">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="1ca90-118">Przykład 2: przydział zasad na poziomie grupy zasobów z obiektem parametru zasad</span><span class="sxs-lookup"><span data-stu-id="1ca90-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1ca90-119">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1ca90-120">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ca90-121">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1ca90-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1ca90-122">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1ca90-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="1ca90-123">Trzecia i czwarta komenda Utwórz obiekt zawierający wszystkie regiony platformy Azure z nazwą "Wschód".</span><span class="sxs-lookup"><span data-stu-id="1ca90-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="1ca90-124">Te polecenia przechowują ten obiekt w zmiennej $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="1ca90-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="1ca90-125">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów przy użyciu obiektu parametru zasad w $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="1ca90-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="1ca90-126">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ca90-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1ca90-127">Przykład 3: przydział zasad na poziomie grupy zasobów z plikiem parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="1ca90-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="1ca90-128">Utwórz plik o nazwie _AllowedLocations.js_ w lokalnym katalogu roboczym z poniższą zawartością.</span><span class="sxs-lookup"><span data-stu-id="1ca90-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="1ca90-129">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ca90-130">Drugie polecenie pobiera wbudowaną definicję zasad dla dozwolonych lokalizacji za pomocą polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1ca90-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ca90-131">Polecenie ostatnie przypisuje zasady w $Policy w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup przy użyciu pliku z parametrem zasad AllowedLocations.jsna podstawie lokalnego katalogu roboczego.</span><span class="sxs-lookup"><span data-stu-id="1ca90-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="1ca90-132">Przykład 4: przypisanie zasad z tożsamością zarządzaną</span><span class="sxs-lookup"><span data-stu-id="1ca90-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="1ca90-133">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ca90-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1ca90-134">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzPolicyDefinition i zapisuje je w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="1ca90-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1ca90-135">Polecenie ostatnie umożliwia przypisanie zasad w $Policy do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ca90-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="1ca90-136">Zarządzana tożsamość zostanie automatycznie utworzona i przypisana do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="1ca90-137">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ca90-137">PARAMETERS</span></span>

### <span data-ttu-id="1ca90-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1ca90-138">-ApiVersion</span></span>
<span data-ttu-id="1ca90-139">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1ca90-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1ca90-140">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="1ca90-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1ca90-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1ca90-141">-AssignIdentity</span></span>
<span data-ttu-id="1ca90-142">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="1ca90-143">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="1ca90-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="1ca90-144">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="1ca90-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="1ca90-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca90-145">-DefaultProfile</span></span>
<span data-ttu-id="1ca90-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1ca90-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-147">— Opis</span><span class="sxs-lookup"><span data-stu-id="1ca90-147">-Description</span></span>
<span data-ttu-id="1ca90-148">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="1ca90-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="1ca90-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ca90-149">-DisplayName</span></span>
<span data-ttu-id="1ca90-150">Określa nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1ca90-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1ca90-151">-InformationAction</span></span>
<span data-ttu-id="1ca90-152">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1ca90-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="1ca90-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1ca90-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ca90-154">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1ca90-154">Continue</span></span>
- <span data-ttu-id="1ca90-155">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1ca90-155">Ignore</span></span>
- <span data-ttu-id="1ca90-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="1ca90-156">Inquire</span></span>
- <span data-ttu-id="1ca90-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1ca90-157">SilentlyContinue</span></span>
- <span data-ttu-id="1ca90-158">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1ca90-158">Stop</span></span>
- <span data-ttu-id="1ca90-159">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1ca90-159">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1ca90-160">-InformationVariable</span></span>
<span data-ttu-id="1ca90-161">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1ca90-161">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-162">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ca90-162">-Location</span></span>
<span data-ttu-id="1ca90-163">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="1ca90-164">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="1ca90-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="1ca90-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1ca90-165">-Metadata</span></span>
<span data-ttu-id="1ca90-166">Metadane nowego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="1ca90-167">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="1ca90-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="1ca90-168">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ca90-168">-Name</span></span>
<span data-ttu-id="1ca90-169">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="1ca90-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1ca90-170">-NotScope</span></span>
<span data-ttu-id="1ca90-171">Nie zakresy przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="1ca90-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1ca90-172">-PolicyDefinition</span></span>
<span data-ttu-id="1ca90-173">Określa zasadę, jako obiekt **PsPolicyDefinition** , który zawiera regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="1ca90-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1ca90-174">-PolicyParameter</span></span>
<span data-ttu-id="1ca90-175">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="1ca90-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ca90-176">-PolicyParameterObject</span></span>
<span data-ttu-id="1ca90-177">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="1ca90-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1ca90-178">-PolicySetDefinition</span></span>
<span data-ttu-id="1ca90-179">Obiekt definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="1ca90-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="1ca90-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ca90-180">-Pre</span></span>
<span data-ttu-id="1ca90-181">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="1ca90-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1ca90-182">-Zakres</span><span class="sxs-lookup"><span data-stu-id="1ca90-182">-Scope</span></span>
<span data-ttu-id="1ca90-183">Określa zakres, do którego należy przypisać zasady.</span><span class="sxs-lookup"><span data-stu-id="1ca90-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="1ca90-184">Aby na przykład przypisać zasadę do grupy zasobów, określ następujące dane: `/subscriptions/` `/resourcegroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1ca90-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="1ca90-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ca90-185">-Sku</span></span>
<span data-ttu-id="1ca90-186">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="1ca90-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="1ca90-187">Domyślnie jest to bezpłatna jednostka SKU z wartościami: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="1ca90-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="1ca90-188">Aby użyć standardowej wersji SKU, użyj wartości: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="1ca90-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca90-189">CommonParameters</span></span>
<span data-ttu-id="1ca90-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca90-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca90-191">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca90-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca90-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ca90-192">INPUTS</span></span>

## <span data-ttu-id="1ca90-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ca90-193">OUTPUTS</span></span>

## <span data-ttu-id="1ca90-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ca90-194">NOTES</span></span>

## <span data-ttu-id="1ca90-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ca90-195">RELATED LINKS</span></span>

[<span data-ttu-id="1ca90-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1ca90-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="1ca90-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ca90-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1ca90-198">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ca90-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="1ca90-199">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1ca90-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


