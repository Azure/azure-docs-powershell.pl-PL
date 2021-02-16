---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186483"
---
# <span data-ttu-id="a6994-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6994-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="a6994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6994-102">SYNOPSIS</span></span>
<span data-ttu-id="a6994-103">Pobiera definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="a6994-103">Gets policy definitions.</span></span>

## <span data-ttu-id="a6994-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6994-104">SYNTAX</span></span>

### <span data-ttu-id="a6994-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6994-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6994-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6994-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6994-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6994-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6994-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6994-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6994-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6994-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6994-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6994-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6994-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6994-111">DESCRIPTION</span></span>
<span data-ttu-id="a6994-112">Polecenie **cmdlet Get-AzPolicyDefinition** pobiera kolekcję definicji zasad lub określoną definicję zasad identyfikowaną za pomocą nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a6994-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="a6994-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6994-113">EXAMPLES</span></span>

### <span data-ttu-id="a6994-114">Przykład 1. Pobierz wszystkie definicje zasad</span><span class="sxs-lookup"><span data-stu-id="a6994-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="a6994-115">To polecenie pobiera wszystkie definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="a6994-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="a6994-116">Przykład 2. Uzyskiwanie definicji zasad z bieżącej subskrypcji według nazwy</span><span class="sxs-lookup"><span data-stu-id="a6994-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="a6994-117">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="a6994-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="a6994-118">Przykład 3. Uzyskiwanie definicji zasad z grupy zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="a6994-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="a6994-119">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z grupy zarządzania o nazwie Sprz42.</span><span class="sxs-lookup"><span data-stu-id="a6994-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="a6994-120">Przykład 4. Uzyskiwanie wszystkich wbudowanych definicji zasad z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a6994-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="a6994-121">To polecenie pobiera wszystkie wbudowane definicje zasad z subskrypcji o identyfikatorze 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="a6994-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="a6994-122">Przykład 5. Pobierz definicje zasad z danej kategorii</span><span class="sxs-lookup"><span data-stu-id="a6994-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="a6994-123">To polecenie pobiera wszystkie definicje zasad w kategorii "Maszyny wirtualnej".</span><span class="sxs-lookup"><span data-stu-id="a6994-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="a6994-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6994-124">PARAMETERS</span></span>

### <span data-ttu-id="a6994-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a6994-125">-ApiVersion</span></span>
<span data-ttu-id="a6994-126">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="a6994-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a6994-127">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="a6994-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a6994-128">— wbudowane</span><span class="sxs-lookup"><span data-stu-id="a6994-128">-Builtin</span></span>
<span data-ttu-id="a6994-129">Ogranicza listę wyników tylko do wbudowanych definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="a6994-129">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6994-130">— Niestandardowe</span><span class="sxs-lookup"><span data-stu-id="a6994-130">-Custom</span></span>
<span data-ttu-id="a6994-131">Ogranicza listę wyników tylko do definicji zasad niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="a6994-131">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6994-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6994-132">-DefaultProfile</span></span>
<span data-ttu-id="a6994-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a6994-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6994-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a6994-134">-Id</span></span>
<span data-ttu-id="a6994-135">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6994-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a6994-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a6994-136">-ManagementGroupName</span></span>
<span data-ttu-id="a6994-137">Nazwa grupy zarządzania, które mają otrzymać definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="a6994-137">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6994-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6994-138">-Name</span></span>
<span data-ttu-id="a6994-139">Określa nazwę definicji zasad pobieraną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6994-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6994-140">— Przed</span><span class="sxs-lookup"><span data-stu-id="a6994-140">-Pre</span></span>
<span data-ttu-id="a6994-141">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="a6994-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a6994-142">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6994-142">-SubscriptionId</span></span>
<span data-ttu-id="a6994-143">Identyfikator subskrypcji definicji zasad do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a6994-143">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6994-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6994-144">CommonParameters</span></span>
<span data-ttu-id="a6994-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6994-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6994-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6994-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6994-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6994-147">INPUTS</span></span>

### <span data-ttu-id="a6994-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a6994-148">System.String</span></span>

### <span data-ttu-id="a6994-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6994-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a6994-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6994-150">OUTPUTS</span></span>

### <span data-ttu-id="a6994-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a6994-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a6994-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6994-152">NOTES</span></span>

## <span data-ttu-id="a6994-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6994-153">RELATED LINKS</span></span>

[<span data-ttu-id="a6994-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6994-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a6994-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6994-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="a6994-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6994-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


