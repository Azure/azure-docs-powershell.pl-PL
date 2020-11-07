---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718275"
---
# <span data-ttu-id="98c4b-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="98c4b-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="98c4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="98c4b-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="98c4b-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98c4b-104">SYNTAX</span></span>

### <span data-ttu-id="98c4b-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98c4b-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c4b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c4b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c4b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c4b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c4b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c4b-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c4b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="98c4b-109">DESCRIPTION</span></span>
<span data-ttu-id="98c4b-110">Polecenie cmdlet **Remove-AzureRmPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="98c4b-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="98c4b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98c4b-111">EXAMPLES</span></span>

### <span data-ttu-id="98c4b-112">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="98c4b-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="98c4b-113">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="98c4b-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="98c4b-114">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="98c4b-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="98c4b-115">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="98c4b-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="98c4b-116">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="98c4b-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="98c4b-117">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="98c4b-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="98c4b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98c4b-118">PARAMETERS</span></span>

### <span data-ttu-id="98c4b-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="98c4b-119">-ApiVersion</span></span>
<span data-ttu-id="98c4b-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="98c4b-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="98c4b-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="98c4b-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="98c4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c4b-122">-DefaultProfile</span></span>
<span data-ttu-id="98c4b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98c4b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c4b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="98c4b-124">-Force</span></span>
<span data-ttu-id="98c4b-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="98c4b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98c4b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="98c4b-126">-Id</span></span>
<span data-ttu-id="98c4b-127">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c4b-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="98c4b-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="98c4b-128">-InformationAction</span></span>
<span data-ttu-id="98c4b-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="98c4b-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="98c4b-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="98c4b-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98c4b-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="98c4b-131">Continue</span></span>
- <span data-ttu-id="98c4b-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="98c4b-132">Ignore</span></span>
- <span data-ttu-id="98c4b-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="98c4b-133">Inquire</span></span>
- <span data-ttu-id="98c4b-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98c4b-134">SilentlyContinue</span></span>
- <span data-ttu-id="98c4b-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="98c4b-135">Stop</span></span>
- <span data-ttu-id="98c4b-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="98c4b-136">Suspend</span></span>

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

### <span data-ttu-id="98c4b-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98c4b-137">-InformationVariable</span></span>
<span data-ttu-id="98c4b-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="98c4b-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98c4b-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="98c4b-139">-ManagementGroupName</span></span>
<span data-ttu-id="98c4b-140">Nazwa grupy zarządzania definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="98c4b-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="98c4b-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98c4b-141">-Name</span></span>
<span data-ttu-id="98c4b-142">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c4b-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c4b-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="98c4b-143">-Pre</span></span>
<span data-ttu-id="98c4b-144">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="98c4b-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="98c4b-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98c4b-145">-SubscriptionId</span></span>
<span data-ttu-id="98c4b-146">Identyfikator subskrypcji definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="98c4b-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="98c4b-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98c4b-147">-Confirm</span></span>
<span data-ttu-id="98c4b-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c4b-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c4b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c4b-149">-WhatIf</span></span>
<span data-ttu-id="98c4b-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c4b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c4b-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98c4b-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c4b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c4b-152">CommonParameters</span></span>
<span data-ttu-id="98c4b-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c4b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c4b-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c4b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c4b-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98c4b-155">INPUTS</span></span>

## <span data-ttu-id="98c4b-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98c4b-156">OUTPUTS</span></span>

## <span data-ttu-id="98c4b-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98c4b-157">NOTES</span></span>

## <span data-ttu-id="98c4b-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98c4b-158">RELATED LINKS</span></span>

[<span data-ttu-id="98c4b-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="98c4b-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="98c4b-160">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="98c4b-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="98c4b-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="98c4b-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


