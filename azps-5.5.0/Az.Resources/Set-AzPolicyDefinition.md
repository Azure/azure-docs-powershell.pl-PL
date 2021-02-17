---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192715"
---
# <span data-ttu-id="083b6-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="083b6-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="083b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083b6-102">SYNOPSIS</span></span>
<span data-ttu-id="083b6-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="083b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="083b6-104">SYNTAX</span></span>

### <span data-ttu-id="083b6-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="083b6-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083b6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="083b6-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083b6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="083b6-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083b6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="083b6-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083b6-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="083b6-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="083b6-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="083b6-110">DESCRIPTION</span></span>
<span data-ttu-id="083b6-111">Polecenie **cmdlet Set-AzPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="083b6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="083b6-112">EXAMPLES</span></span>

### <span data-ttu-id="083b6-113">Przykład 1. Aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="083b6-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="083b6-114">Pierwsze polecenie otrzymuje definicję zasad o nazwie VMPolicyDefinition przy użyciu Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083b6-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="083b6-115">Polecenie przechowuje ten obiekt w $PolicyDefinition zmienną.</span><span class="sxs-lookup"><span data-stu-id="083b6-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="083b6-116">Drugie polecenie aktualizuje opis definicji zasad zidentyfikowanych przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="083b6-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="083b6-117">Przykład 2. Aktualizowanie trybu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="083b6-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="083b6-118">To polecenie aktualizuje definicję zasad o nazwie VMPolicyDefinition, używając Set-AzPolicyDefinition cmdlet w celu ustawienia właściwości trybu na wartość "All".</span><span class="sxs-lookup"><span data-stu-id="083b6-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="083b6-119">Przykład 3. Aktualizowanie metadanych definicji zasad</span><span class="sxs-lookup"><span data-stu-id="083b6-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="083b6-120">To polecenie aktualizuje metadane definicji zasad o nazwie VMPolicyDefinition, aby wskazać, że jej kategoria to "Maszyny wirtualne".</span><span class="sxs-lookup"><span data-stu-id="083b6-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="083b6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="083b6-121">PARAMETERS</span></span>

### <span data-ttu-id="083b6-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="083b6-122">-ApiVersion</span></span>
<span data-ttu-id="083b6-123">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="083b6-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="083b6-124">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="083b6-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="083b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083b6-125">-DefaultProfile</span></span>
<span data-ttu-id="083b6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="083b6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="083b6-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="083b6-127">-Description</span></span>
<span data-ttu-id="083b6-128">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="083b6-129">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="083b6-129">-DisplayName</span></span>
<span data-ttu-id="083b6-130">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="083b6-131">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="083b6-131">-Id</span></span>
<span data-ttu-id="083b6-132">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083b6-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083b6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="083b6-133">-InputObject</span></span>
<span data-ttu-id="083b6-134">Obiekt definicji zasad do aktualizacji, który był wyprowadzony z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083b6-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="083b6-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="083b6-135">-ManagementGroupName</span></span>
<span data-ttu-id="083b6-136">Nazwa grupy zarządzania definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="083b6-136">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083b6-137">— Metadane</span><span class="sxs-lookup"><span data-stu-id="083b6-137">-Metadata</span></span>
<span data-ttu-id="083b6-138">Metadane dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-138">The metadata for policy definition.</span></span> <span data-ttu-id="083b6-139">Może to być ścieżka do nazwy pliku zawierającej metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="083b6-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="083b6-140">— tryb</span><span class="sxs-lookup"><span data-stu-id="083b6-140">-Mode</span></span>
<span data-ttu-id="083b6-141">Tryb definicji nowych zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="083b6-142">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="083b6-142">-Name</span></span>
<span data-ttu-id="083b6-143">Określa nazwę definicji zasad, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083b6-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083b6-144">- Parametr</span><span class="sxs-lookup"><span data-stu-id="083b6-144">-Parameter</span></span>
<span data-ttu-id="083b6-145">Deklaracja parametrów dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="083b6-146">Może to być ścieżka do nazwy pliku lub uri zawierającej deklarację parametrów lub deklaracja parametrów jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="083b6-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="083b6-147">— Zasady</span><span class="sxs-lookup"><span data-stu-id="083b6-147">-Policy</span></span>
<span data-ttu-id="083b6-148">Określa nową regułę zasad dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="083b6-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="083b6-149">Ścieżkę pliku json lub ciągu zawierającego zasady można określić w formacie JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="083b6-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="083b6-150">— Przed</span><span class="sxs-lookup"><span data-stu-id="083b6-150">-Pre</span></span>
<span data-ttu-id="083b6-151">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="083b6-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="083b6-152">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="083b6-152">-SubscriptionId</span></span>
<span data-ttu-id="083b6-153">Identyfikator subskrypcji definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="083b6-153">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083b6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083b6-154">CommonParameters</span></span>
<span data-ttu-id="083b6-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083b6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083b6-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="083b6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083b6-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="083b6-157">INPUTS</span></span>

### <span data-ttu-id="083b6-158">System.String</span><span class="sxs-lookup"><span data-stu-id="083b6-158">System.String</span></span>

### <span data-ttu-id="083b6-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="083b6-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="083b6-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="083b6-160">OUTPUTS</span></span>

### <span data-ttu-id="083b6-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="083b6-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="083b6-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="083b6-162">NOTES</span></span>

## <span data-ttu-id="083b6-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="083b6-163">RELATED LINKS</span></span>

[<span data-ttu-id="083b6-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="083b6-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="083b6-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="083b6-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="083b6-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="083b6-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


