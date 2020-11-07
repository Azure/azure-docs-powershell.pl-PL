---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710921"
---
# <span data-ttu-id="dee77-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dee77-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="dee77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dee77-102">SYNOPSIS</span></span>
<span data-ttu-id="dee77-103">Tworzy definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dee77-104">SYNTAX</span></span>

### <span data-ttu-id="dee77-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dee77-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dee77-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dee77-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dee77-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dee77-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dee77-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dee77-108">DESCRIPTION</span></span>
<span data-ttu-id="dee77-109">Polecenie cmdlet **New-AzureRmPolicyDefinition** umożliwia utworzenie definicji zasad zawierającej regułę zasad w formacie notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="dee77-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="dee77-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dee77-110">EXAMPLES</span></span>

### <span data-ttu-id="dee77-111">Przykład 1: Tworzenie definicji zasad przy użyciu pliku zasad</span><span class="sxs-lookup"><span data-stu-id="dee77-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="dee77-112">To polecenie tworzy definicję zasad o nazwie LocationDefinition zawierającą regułę określoną w C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="dee77-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="dee77-113">Przykładowa zawartość dla LocationPolicy.jsw pliku podano powyżej.</span><span class="sxs-lookup"><span data-stu-id="dee77-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="dee77-114">Przykład 2: Tworzenie definicji zasad parametrycznych przy użyciu parametrów wbudowanych</span><span class="sxs-lookup"><span data-stu-id="dee77-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="dee77-115">To polecenie tworzy definicję zasad o nazwie LocationDefinition zawierającą regułę określoną w C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="dee77-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="dee77-116">Definicja parametru dla reguły zasad jest podana w tekście.</span><span class="sxs-lookup"><span data-stu-id="dee77-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="dee77-117">Przykład 3: Tworzenie definicji zasad wewnątrz grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dee77-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="dee77-118">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition w grupie zarządzania Dept42.</span><span class="sxs-lookup"><span data-stu-id="dee77-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="dee77-119">To polecenie określa zasadę jako ciąg w prawidłowym formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="dee77-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="dee77-120">Przykład 4: Tworzenie definicji zasad w tekście z metadanymi</span><span class="sxs-lookup"><span data-stu-id="dee77-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="dee77-121">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition z metadanymi wskazującymi jego kategorię "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="dee77-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="dee77-122">To polecenie określa zasadę jako ciąg w prawidłowym formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="dee77-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="dee77-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dee77-123">PARAMETERS</span></span>

### <span data-ttu-id="dee77-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dee77-124">-ApiVersion</span></span>
<span data-ttu-id="dee77-125">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="dee77-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dee77-126">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="dee77-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dee77-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee77-127">-DefaultProfile</span></span>
<span data-ttu-id="dee77-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dee77-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dee77-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="dee77-129">-Description</span></span>
<span data-ttu-id="dee77-130">Określa opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="dee77-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dee77-131">-DisplayName</span></span>
<span data-ttu-id="dee77-132">Określa nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="dee77-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dee77-133">-InformationAction</span></span>
<span data-ttu-id="dee77-134">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="dee77-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="dee77-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dee77-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dee77-136">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="dee77-136">Continue</span></span>
- <span data-ttu-id="dee77-137">Ignorować</span><span class="sxs-lookup"><span data-stu-id="dee77-137">Ignore</span></span>
- <span data-ttu-id="dee77-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="dee77-138">Inquire</span></span>
- <span data-ttu-id="dee77-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dee77-139">SilentlyContinue</span></span>
- <span data-ttu-id="dee77-140">Przestaw</span><span class="sxs-lookup"><span data-stu-id="dee77-140">Stop</span></span>
- <span data-ttu-id="dee77-141">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="dee77-141">Suspend</span></span>

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

### <span data-ttu-id="dee77-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dee77-142">-InformationVariable</span></span>
<span data-ttu-id="dee77-143">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="dee77-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dee77-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="dee77-144">-ManagementGroupName</span></span>
<span data-ttu-id="dee77-145">Nazwa grupy zarządzania nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="dee77-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dee77-146">-Metadata</span></span>
<span data-ttu-id="dee77-147">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-147">The metadata for policy definition.</span></span> <span data-ttu-id="dee77-148">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="dee77-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="dee77-149">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="dee77-149">-Mode</span></span>
<span data-ttu-id="dee77-150">Tryb definicji zasad</span><span class="sxs-lookup"><span data-stu-id="dee77-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee77-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dee77-151">-Name</span></span>
<span data-ttu-id="dee77-152">Określa nazwę definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="dee77-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="dee77-153">-Parameter</span></span>
<span data-ttu-id="dee77-154">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="dee77-155">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="dee77-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="dee77-156">-Policy</span><span class="sxs-lookup"><span data-stu-id="dee77-156">-Policy</span></span>
<span data-ttu-id="dee77-157">Określa regułę zasad dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="dee77-158">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="dee77-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="dee77-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="dee77-159">-Pre</span></span>
<span data-ttu-id="dee77-160">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="dee77-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dee77-161">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dee77-161">-SubscriptionId</span></span>
<span data-ttu-id="dee77-162">Identyfikator subskrypcji nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="dee77-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="dee77-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee77-163">CommonParameters</span></span>
<span data-ttu-id="dee77-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee77-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee77-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee77-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee77-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dee77-166">INPUTS</span></span>

## <span data-ttu-id="dee77-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dee77-167">OUTPUTS</span></span>

## <span data-ttu-id="dee77-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dee77-168">NOTES</span></span>

## <span data-ttu-id="dee77-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dee77-169">RELATED LINKS</span></span>

[<span data-ttu-id="dee77-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dee77-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="dee77-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dee77-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="dee77-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dee77-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


