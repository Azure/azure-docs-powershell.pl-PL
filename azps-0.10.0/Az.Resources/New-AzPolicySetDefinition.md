---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: c5de339929e44433efdee64de0257c62845c5b26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892490"
---
# <span data-ttu-id="ec61f-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ec61f-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ec61f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec61f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec61f-103">Tworzy definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="ec61f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec61f-104">SYNTAX</span></span>

### <span data-ttu-id="ec61f-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec61f-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec61f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec61f-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec61f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec61f-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec61f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ec61f-108">DESCRIPTION</span></span>
<span data-ttu-id="ec61f-109">Polecenie cmdlet **New-AzPolicySetDefinition** umożliwia utworzenie definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="ec61f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec61f-110">EXAMPLES</span></span>

### <span data-ttu-id="ec61f-111">Przykład 1: Tworzenie definicji zestawu zasad przy użyciu pliku zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="ec61f-111">Example 1: Create a policy set definition by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="ec61f-112">To polecenie tworzy definicję zestawu zasad o nazwie VMPolicyDefinition zawierającą definicje zasad określone w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="ec61f-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="ec61f-113">Przykładowa zawartość VMPolicy.jsjest podana powyżej.</span><span class="sxs-lookup"><span data-stu-id="ec61f-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="ec61f-114">Przykład 2: Tworzenie definicji zestawu zasad sparametryzowanych</span><span class="sxs-lookup"><span data-stu-id="ec61f-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="ec61f-115">To polecenie tworzy definicję zestawu zasad sparametryzowanego o nazwie VMPolicyDefinition zawierającą definicje zasad określone w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="ec61f-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="ec61f-116">Przykładowa zawartość VMPolicy.jsjest podana powyżej.</span><span class="sxs-lookup"><span data-stu-id="ec61f-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="ec61f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec61f-117">PARAMETERS</span></span>

### <span data-ttu-id="ec61f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec61f-118">-ApiVersion</span></span>
<span data-ttu-id="ec61f-119">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ec61f-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec61f-120">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ec61f-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ec61f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec61f-121">-DefaultProfile</span></span>
<span data-ttu-id="ec61f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ec61f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec61f-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="ec61f-123">-Description</span></span>
<span data-ttu-id="ec61f-124">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="ec61f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec61f-125">-DisplayName</span></span>
<span data-ttu-id="ec61f-126">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="ec61f-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ec61f-127">-ManagementGroupName</span></span>
<span data-ttu-id="ec61f-128">Nazwa grupy zarządzania nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="ec61f-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ec61f-129">-Metadata</span></span>
<span data-ttu-id="ec61f-130">Metadane dotyczące definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-130">The metadata for policy set definition.</span></span> <span data-ttu-id="ec61f-131">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="ec61f-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="ec61f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec61f-132">-Name</span></span>
<span data-ttu-id="ec61f-133">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="ec61f-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ec61f-134">-Parameter</span></span>
<span data-ttu-id="ec61f-135">Deklaracja Parameters dla definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="ec61f-136">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="ec61f-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="ec61f-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ec61f-137">-PolicyDefinition</span></span>
<span data-ttu-id="ec61f-138">Definicja zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-138">The policy set definition.</span></span> <span data-ttu-id="ec61f-139">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicji zestawu zasad jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="ec61f-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="ec61f-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec61f-140">-Pre</span></span>
<span data-ttu-id="ec61f-141">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ec61f-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec61f-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ec61f-142">-SubscriptionId</span></span>
<span data-ttu-id="ec61f-143">Identyfikator subskrypcji nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec61f-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="ec61f-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec61f-144">-Confirm</span></span>
<span data-ttu-id="ec61f-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec61f-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec61f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec61f-146">-WhatIf</span></span>
<span data-ttu-id="ec61f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec61f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec61f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec61f-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec61f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec61f-149">CommonParameters</span></span>
<span data-ttu-id="ec61f-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec61f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec61f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec61f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec61f-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec61f-152">INPUTS</span></span>

### <span data-ttu-id="ec61f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ec61f-153">System.String</span></span>

### <span data-ttu-id="ec61f-154">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ec61f-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ec61f-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec61f-155">OUTPUTS</span></span>

### <span data-ttu-id="ec61f-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ec61f-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ec61f-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec61f-157">NOTES</span></span>

## <span data-ttu-id="ec61f-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec61f-158">RELATED LINKS</span></span>
