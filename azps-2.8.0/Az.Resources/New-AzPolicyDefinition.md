---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 1c3b18d5e098e19a8259f3b8faf06adcc25f7333
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871803"
---
# <span data-ttu-id="7246f-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7246f-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="7246f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7246f-102">SYNOPSIS</span></span>
<span data-ttu-id="7246f-103">Tworzy definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-103">Creates a policy definition.</span></span>

## <span data-ttu-id="7246f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7246f-104">SYNTAX</span></span>

### <span data-ttu-id="7246f-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7246f-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7246f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7246f-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7246f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7246f-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7246f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7246f-108">DESCRIPTION</span></span>
<span data-ttu-id="7246f-109">Polecenie cmdlet **New-AzPolicyDefinition** umożliwia utworzenie definicji zasad zawierającej regułę zasad w formacie notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="7246f-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="7246f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7246f-110">EXAMPLES</span></span>

### <span data-ttu-id="7246f-111">Przykład 1: Tworzenie definicji zasad przy użyciu pliku zasad</span><span class="sxs-lookup"><span data-stu-id="7246f-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="7246f-112">To polecenie tworzy definicję zasad o nazwie LocationDefinition zawierającą regułę określoną w C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="7246f-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="7246f-113">Przykładowa zawartość dla LocationPolicy.jsw pliku podano powyżej.</span><span class="sxs-lookup"><span data-stu-id="7246f-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="7246f-114">Przykład 2: Tworzenie definicji zasad parametrycznych przy użyciu parametrów wbudowanych</span><span class="sxs-lookup"><span data-stu-id="7246f-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="7246f-115">To polecenie tworzy definicję zasad o nazwie LocationDefinition zawierającą regułę określoną w C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="7246f-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="7246f-116">Definicja parametru dla reguły zasad jest podana w tekście.</span><span class="sxs-lookup"><span data-stu-id="7246f-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="7246f-117">Przykład 3: Tworzenie definicji zasad wewnątrz grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="7246f-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="7246f-118">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition w grupie zarządzania Dept42.</span><span class="sxs-lookup"><span data-stu-id="7246f-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="7246f-119">To polecenie określa zasadę jako ciąg w prawidłowym formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="7246f-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="7246f-120">Przykład 4: Tworzenie definicji zasad w tekście z metadanymi</span><span class="sxs-lookup"><span data-stu-id="7246f-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="7246f-121">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition z metadanymi wskazującymi jego kategorię "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="7246f-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="7246f-122">To polecenie określa zasadę jako ciąg w prawidłowym formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="7246f-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="7246f-123">Przykład 5: Tworzenie definicji zasad w tekście z trybem</span><span class="sxs-lookup"><span data-stu-id="7246f-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="7246f-124">To polecenie tworzy definicję zasad o nazwie TagsPolicyDefinition w trybie "indeksowane", wskazującą, że zasady powinny być oceniane tylko dla typów zasobów obsługujących znaczniki i lokalizację.</span><span class="sxs-lookup"><span data-stu-id="7246f-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="7246f-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7246f-125">PARAMETERS</span></span>

### <span data-ttu-id="7246f-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7246f-126">-ApiVersion</span></span>
<span data-ttu-id="7246f-127">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7246f-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7246f-128">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="7246f-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7246f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7246f-129">-DefaultProfile</span></span>
<span data-ttu-id="7246f-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7246f-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7246f-131">— Opis</span><span class="sxs-lookup"><span data-stu-id="7246f-131">-Description</span></span>
<span data-ttu-id="7246f-132">Określa opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="7246f-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7246f-133">-DisplayName</span></span>
<span data-ttu-id="7246f-134">Określa nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="7246f-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7246f-135">-ManagementGroupName</span></span>
<span data-ttu-id="7246f-136">Nazwa grupy zarządzania nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="7246f-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7246f-137">-Metadata</span></span>
<span data-ttu-id="7246f-138">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-138">The metadata for policy definition.</span></span> <span data-ttu-id="7246f-139">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="7246f-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="7246f-140">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="7246f-140">-Mode</span></span>
<span data-ttu-id="7246f-141">Tryb definicji zasad</span><span class="sxs-lookup"><span data-stu-id="7246f-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7246f-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7246f-142">-Name</span></span>
<span data-ttu-id="7246f-143">Określa nazwę definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="7246f-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7246f-144">-Parameter</span></span>
<span data-ttu-id="7246f-145">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="7246f-146">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="7246f-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="7246f-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="7246f-147">-Policy</span></span>
<span data-ttu-id="7246f-148">Określa regułę zasad dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="7246f-149">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="7246f-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="7246f-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="7246f-150">-Pre</span></span>
<span data-ttu-id="7246f-151">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="7246f-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7246f-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7246f-152">-SubscriptionId</span></span>
<span data-ttu-id="7246f-153">Identyfikator subskrypcji nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7246f-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="7246f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7246f-154">CommonParameters</span></span>
<span data-ttu-id="7246f-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7246f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7246f-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7246f-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7246f-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7246f-157">INPUTS</span></span>

### <span data-ttu-id="7246f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7246f-158">System.String</span></span>

### <span data-ttu-id="7246f-159">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7246f-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7246f-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7246f-160">OUTPUTS</span></span>

### <span data-ttu-id="7246f-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7246f-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7246f-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7246f-162">NOTES</span></span>

## <span data-ttu-id="7246f-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7246f-163">RELATED LINKS</span></span>

[<span data-ttu-id="7246f-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7246f-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7246f-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7246f-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="7246f-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7246f-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


