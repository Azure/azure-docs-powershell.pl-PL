---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 78dc06f53a94f6fe1524189a0cea32f214439f66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708396"
---
# <span data-ttu-id="919e6-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="919e6-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="919e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="919e6-102">SYNOPSIS</span></span>
<span data-ttu-id="919e6-103">Pobiera definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="919e6-103">Gets policy definitions.</span></span>

## <span data-ttu-id="919e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="919e6-104">SYNTAX</span></span>

### <span data-ttu-id="919e6-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="919e6-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919e6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="919e6-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919e6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="919e6-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919e6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="919e6-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="919e6-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="919e6-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919e6-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="919e6-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="919e6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="919e6-111">DESCRIPTION</span></span>
<span data-ttu-id="919e6-112">Polecenie cmdlet **Get-AzPolicyDefinition** Pobiera kolekcję definicji zasad lub określoną definicję zasady zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="919e6-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="919e6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="919e6-113">EXAMPLES</span></span>

### <span data-ttu-id="919e6-114">Przykład 1: pobieranie wszystkich definicji zasad</span><span class="sxs-lookup"><span data-stu-id="919e6-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="919e6-115">To polecenie pobiera wszystkie definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="919e6-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="919e6-116">Przykład 2: pobieranie definicji zasad z bieżącego abonamentu według nazwy</span><span class="sxs-lookup"><span data-stu-id="919e6-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="919e6-117">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="919e6-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="919e6-118">Przykład 3: pobieranie definicji zasad z grupy zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="919e6-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="919e6-119">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z grupy zarządzania o nazwie Dept42.</span><span class="sxs-lookup"><span data-stu-id="919e6-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="919e6-120">Przykład 4: pobieranie wszystkich wbudowanych definicji zasad z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="919e6-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="919e6-121">To polecenie pobiera wszystkie wbudowane definicje zasad z subskrypcji o IDENTYFIKATORze 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="919e6-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="919e6-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="919e6-122">PARAMETERS</span></span>

### <span data-ttu-id="919e6-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="919e6-123">-ApiVersion</span></span>
<span data-ttu-id="919e6-124">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="919e6-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="919e6-125">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="919e6-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="919e6-126">-Wbudowane</span><span class="sxs-lookup"><span data-stu-id="919e6-126">-Builtin</span></span>
<span data-ttu-id="919e6-127">Ograniczanie listy wyników tylko do wbudowanych definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="919e6-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="919e6-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="919e6-128">-Custom</span></span>
<span data-ttu-id="919e6-129">Ogranicza listę wyników tylko do definicji zasad niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="919e6-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="919e6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919e6-130">-DefaultProfile</span></span>
<span data-ttu-id="919e6-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="919e6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="919e6-132">-ID</span><span class="sxs-lookup"><span data-stu-id="919e6-132">-Id</span></span>
<span data-ttu-id="919e6-133">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919e6-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="919e6-134">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="919e6-134">-ManagementGroupName</span></span>
<span data-ttu-id="919e6-135">Nazwa grupy zarządzania definicji zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="919e6-135">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="919e6-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="919e6-136">-Name</span></span>
<span data-ttu-id="919e6-137">Określa nazwę definicji zasad, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919e6-137">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="919e6-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="919e6-138">-Pre</span></span>
<span data-ttu-id="919e6-139">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="919e6-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="919e6-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="919e6-140">-SubscriptionId</span></span>
<span data-ttu-id="919e6-141">Identyfikator subskrypcji definicji zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="919e6-141">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="919e6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919e6-142">CommonParameters</span></span>
<span data-ttu-id="919e6-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919e6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919e6-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919e6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919e6-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="919e6-145">INPUTS</span></span>

### <span data-ttu-id="919e6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="919e6-146">System.String</span></span>

### <span data-ttu-id="919e6-147">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="919e6-147">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="919e6-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="919e6-148">OUTPUTS</span></span>

### <span data-ttu-id="919e6-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="919e6-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="919e6-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="919e6-150">NOTES</span></span>

## <span data-ttu-id="919e6-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="919e6-151">RELATED LINKS</span></span>

[<span data-ttu-id="919e6-152">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="919e6-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="919e6-153">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="919e6-153">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="919e6-154">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="919e6-154">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


