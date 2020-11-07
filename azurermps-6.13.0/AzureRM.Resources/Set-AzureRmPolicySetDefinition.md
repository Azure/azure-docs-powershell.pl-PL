---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d558e7104027e4c3fcef3b6e8d8427d5fd3802fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718768"
---
# <span data-ttu-id="89a4d-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="89a4d-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="89a4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="89a4d-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="89a4d-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89a4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89a4d-104">SYNTAX</span></span>

### <span data-ttu-id="89a4d-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89a4d-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89a4d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89a4d-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89a4d-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89a4d-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89a4d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89a4d-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a4d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="89a4d-109">DESCRIPTION</span></span>
<span data-ttu-id="89a4d-110">Polecenie cmdlet **Set-AzureRmPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="89a4d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89a4d-111">EXAMPLES</span></span>

### <span data-ttu-id="89a4d-112">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="89a4d-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="89a4d-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="89a4d-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="89a4d-114">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="89a4d-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="89a4d-115">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="89a4d-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="89a4d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89a4d-116">PARAMETERS</span></span>

### <span data-ttu-id="89a4d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89a4d-117">-ApiVersion</span></span>
<span data-ttu-id="89a4d-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="89a4d-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="89a4d-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="89a4d-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="89a4d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a4d-120">-DefaultProfile</span></span>
<span data-ttu-id="89a4d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="89a4d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89a4d-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="89a4d-122">-Description</span></span>
<span data-ttu-id="89a4d-123">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="89a4d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89a4d-124">-DisplayName</span></span>
<span data-ttu-id="89a4d-125">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="89a4d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="89a4d-126">-Id</span></span>
<span data-ttu-id="89a4d-127">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="89a4d-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="89a4d-128">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="89a4d-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="89a4d-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="89a4d-129">-ManagementGroupName</span></span>
<span data-ttu-id="89a4d-130">Nazwa grupy zarządzania definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="89a4d-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="89a4d-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="89a4d-131">-Metadata</span></span>
<span data-ttu-id="89a4d-132">Metadane zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="89a4d-133">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="89a4d-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="89a4d-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89a4d-134">-Name</span></span>
<span data-ttu-id="89a4d-135">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-135">The policy set definition name.</span></span>

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

### <span data-ttu-id="89a4d-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="89a4d-136">-Parameter</span></span>
<span data-ttu-id="89a4d-137">Deklaracja parametrów zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="89a4d-138">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="89a4d-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="89a4d-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89a4d-139">-PolicyDefinition</span></span>
<span data-ttu-id="89a4d-140">Definicja zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="89a4d-140">The policy set definition.</span></span> <span data-ttu-id="89a4d-141">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicji zestawu zasad jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="89a4d-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="89a4d-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="89a4d-142">-Pre</span></span>
<span data-ttu-id="89a4d-143">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="89a4d-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="89a4d-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="89a4d-144">-SubscriptionId</span></span>
<span data-ttu-id="89a4d-145">Identyfikator subskrypcji definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="89a4d-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="89a4d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89a4d-146">-Confirm</span></span>
<span data-ttu-id="89a4d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a4d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a4d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a4d-148">-WhatIf</span></span>
<span data-ttu-id="89a4d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a4d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89a4d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89a4d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a4d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a4d-151">CommonParameters</span></span>
<span data-ttu-id="89a4d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a4d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a4d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a4d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a4d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89a4d-154">INPUTS</span></span>

### <span data-ttu-id="89a4d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="89a4d-155">System.String</span></span>

### <span data-ttu-id="89a4d-156">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="89a4d-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="89a4d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89a4d-157">OUTPUTS</span></span>

### <span data-ttu-id="89a4d-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="89a4d-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="89a4d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89a4d-159">NOTES</span></span>

## <span data-ttu-id="89a4d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89a4d-160">RELATED LINKS</span></span>
