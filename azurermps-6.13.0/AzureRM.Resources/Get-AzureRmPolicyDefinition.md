---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 30e113ca85c24b46d4594658f1d91abb6b14bd3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544855"
---
# <span data-ttu-id="bea17-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bea17-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="bea17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bea17-102">SYNOPSIS</span></span>
<span data-ttu-id="bea17-103">Pobiera definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="bea17-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bea17-104">SYNTAX</span></span>

### <span data-ttu-id="bea17-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bea17-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea17-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea17-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea17-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea17-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea17-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea17-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea17-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea17-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea17-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea17-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bea17-111">Opis</span><span class="sxs-lookup"><span data-stu-id="bea17-111">DESCRIPTION</span></span>
<span data-ttu-id="bea17-112">Polecenie cmdlet **Get-AzureRmPolicyDefinition** Pobiera kolekcję definicji zasad lub określoną definicję zasady zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="bea17-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="bea17-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bea17-113">EXAMPLES</span></span>

### <span data-ttu-id="bea17-114">Przykład 1: pobieranie wszystkich definicji zasad</span><span class="sxs-lookup"><span data-stu-id="bea17-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="bea17-115">To polecenie pobiera wszystkie definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="bea17-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="bea17-116">Przykład 2: pobieranie definicji zasad z bieżącego abonamentu według nazwy</span><span class="sxs-lookup"><span data-stu-id="bea17-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="bea17-117">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="bea17-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="bea17-118">Przykład 3: pobieranie definicji zasad z grupy zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="bea17-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="bea17-119">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition z grupy zarządzania o nazwie Dept42.</span><span class="sxs-lookup"><span data-stu-id="bea17-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="bea17-120">Przykład 4: pobieranie wszystkich wbudowanych definicji zasad z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bea17-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="bea17-121">To polecenie pobiera wszystkie wbudowane definicje zasad z subskrypcji o IDENTYFIKATORze 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="bea17-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="bea17-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bea17-122">PARAMETERS</span></span>

### <span data-ttu-id="bea17-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bea17-123">-ApiVersion</span></span>
<span data-ttu-id="bea17-124">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="bea17-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bea17-125">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="bea17-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bea17-126">-Wbudowane</span><span class="sxs-lookup"><span data-stu-id="bea17-126">-Builtin</span></span>
<span data-ttu-id="bea17-127">Ograniczanie listy wyników tylko do wbudowanych definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="bea17-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="bea17-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="bea17-128">-Custom</span></span>
<span data-ttu-id="bea17-129">Ogranicza listę wyników tylko do definicji zasad niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="bea17-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="bea17-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea17-130">-DefaultProfile</span></span>
<span data-ttu-id="bea17-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bea17-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea17-132">-ID</span><span class="sxs-lookup"><span data-stu-id="bea17-132">-Id</span></span>
<span data-ttu-id="bea17-133">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea17-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bea17-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bea17-134">-InformationAction</span></span>
<span data-ttu-id="bea17-135">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="bea17-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bea17-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bea17-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bea17-137">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="bea17-137">Continue</span></span>
- <span data-ttu-id="bea17-138">Ignorować</span><span class="sxs-lookup"><span data-stu-id="bea17-138">Ignore</span></span>
- <span data-ttu-id="bea17-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="bea17-139">Inquire</span></span>
- <span data-ttu-id="bea17-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bea17-140">SilentlyContinue</span></span>
- <span data-ttu-id="bea17-141">Przestaw</span><span class="sxs-lookup"><span data-stu-id="bea17-141">Stop</span></span>
- <span data-ttu-id="bea17-142">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="bea17-142">Suspend</span></span>

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

### <span data-ttu-id="bea17-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bea17-143">-InformationVariable</span></span>
<span data-ttu-id="bea17-144">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="bea17-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bea17-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bea17-145">-ManagementGroupName</span></span>
<span data-ttu-id="bea17-146">Nazwa grupy zarządzania definicji zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bea17-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="bea17-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bea17-147">-Name</span></span>
<span data-ttu-id="bea17-148">Określa nazwę definicji zasad, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea17-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bea17-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="bea17-149">-Pre</span></span>
<span data-ttu-id="bea17-150">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="bea17-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bea17-151">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bea17-151">-SubscriptionId</span></span>
<span data-ttu-id="bea17-152">Identyfikator subskrypcji definicji zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bea17-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="bea17-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea17-153">CommonParameters</span></span>
<span data-ttu-id="bea17-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea17-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea17-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea17-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea17-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bea17-156">INPUTS</span></span>

## <span data-ttu-id="bea17-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bea17-157">OUTPUTS</span></span>

## <span data-ttu-id="bea17-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bea17-158">NOTES</span></span>

## <span data-ttu-id="bea17-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bea17-159">RELATED LINKS</span></span>

[<span data-ttu-id="bea17-160">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bea17-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bea17-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bea17-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bea17-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bea17-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


