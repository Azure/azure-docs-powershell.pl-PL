---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: ce9dafe30d9f26a0d28ab206d16a50076247eaf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708303"
---
# <span data-ttu-id="63621-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63621-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="63621-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63621-102">SYNOPSIS</span></span>
<span data-ttu-id="63621-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="63621-103">Removes a policy definition.</span></span>

## <span data-ttu-id="63621-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63621-104">SYNTAX</span></span>

### <span data-ttu-id="63621-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63621-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63621-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63621-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63621-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63621-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63621-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63621-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63621-109">Opis</span><span class="sxs-lookup"><span data-stu-id="63621-109">DESCRIPTION</span></span>
<span data-ttu-id="63621-110">Polecenie cmdlet **Remove-AzPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="63621-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="63621-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63621-111">EXAMPLES</span></span>

### <span data-ttu-id="63621-112">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="63621-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="63621-113">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="63621-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="63621-114">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="63621-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="63621-115">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="63621-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="63621-116">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="63621-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="63621-117">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="63621-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="63621-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63621-118">PARAMETERS</span></span>

### <span data-ttu-id="63621-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="63621-119">-ApiVersion</span></span>
<span data-ttu-id="63621-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="63621-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="63621-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="63621-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="63621-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63621-122">-DefaultProfile</span></span>
<span data-ttu-id="63621-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="63621-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63621-124">-Force</span><span class="sxs-lookup"><span data-stu-id="63621-124">-Force</span></span>
<span data-ttu-id="63621-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="63621-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63621-126">-ID</span><span class="sxs-lookup"><span data-stu-id="63621-126">-Id</span></span>
<span data-ttu-id="63621-127">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63621-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63621-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="63621-128">-ManagementGroupName</span></span>
<span data-ttu-id="63621-129">Nazwa grupy zarządzania definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="63621-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="63621-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63621-130">-Name</span></span>
<span data-ttu-id="63621-131">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63621-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63621-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="63621-132">-Pre</span></span>
<span data-ttu-id="63621-133">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="63621-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="63621-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="63621-134">-SubscriptionId</span></span>
<span data-ttu-id="63621-135">Identyfikator subskrypcji definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="63621-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="63621-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63621-136">-Confirm</span></span>
<span data-ttu-id="63621-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63621-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63621-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63621-138">-WhatIf</span></span>
<span data-ttu-id="63621-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63621-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63621-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63621-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63621-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63621-141">CommonParameters</span></span>
<span data-ttu-id="63621-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63621-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63621-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63621-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63621-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63621-144">INPUTS</span></span>

### <span data-ttu-id="63621-145">System. String</span><span class="sxs-lookup"><span data-stu-id="63621-145">System.String</span></span>

### <span data-ttu-id="63621-146">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="63621-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="63621-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63621-147">OUTPUTS</span></span>

### <span data-ttu-id="63621-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63621-148">System.Boolean</span></span>

## <span data-ttu-id="63621-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63621-149">NOTES</span></span>

## <span data-ttu-id="63621-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63621-150">RELATED LINKS</span></span>

[<span data-ttu-id="63621-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63621-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="63621-152">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63621-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="63621-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63621-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


