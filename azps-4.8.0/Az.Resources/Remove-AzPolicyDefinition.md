---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219914"
---
# <span data-ttu-id="0c05c-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c05c-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="0c05c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c05c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c05c-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="0c05c-103">Removes a policy definition.</span></span>

## <span data-ttu-id="0c05c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c05c-104">SYNTAX</span></span>

### <span data-ttu-id="0c05c-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c05c-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c05c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c05c-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c05c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c05c-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c05c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c05c-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c05c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c05c-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c05c-110">Opis</span><span class="sxs-lookup"><span data-stu-id="0c05c-110">DESCRIPTION</span></span>
<span data-ttu-id="0c05c-111">Polecenie cmdlet **Remove-AzPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="0c05c-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="0c05c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c05c-112">EXAMPLES</span></span>

### <span data-ttu-id="0c05c-113">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="0c05c-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="0c05c-114">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="0c05c-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="0c05c-115">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="0c05c-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="0c05c-116">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0c05c-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="0c05c-117">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0c05c-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="0c05c-118">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0c05c-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="0c05c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c05c-119">PARAMETERS</span></span>

### <span data-ttu-id="0c05c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0c05c-120">-ApiVersion</span></span>
<span data-ttu-id="0c05c-121">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0c05c-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0c05c-122">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="0c05c-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0c05c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c05c-123">-DefaultProfile</span></span>
<span data-ttu-id="0c05c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0c05c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c05c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0c05c-125">-Force</span></span>
<span data-ttu-id="0c05c-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0c05c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c05c-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0c05c-127">-Id</span></span>
<span data-ttu-id="0c05c-128">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c05c-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c05c-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c05c-129">-InputObject</span></span>
<span data-ttu-id="0c05c-130">Obiekt definicji zasad, który ma zostać usunięty, był wyprowadzany z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c05c-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="0c05c-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0c05c-131">-ManagementGroupName</span></span>
<span data-ttu-id="0c05c-132">Nazwa grupy zarządzania definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0c05c-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="0c05c-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c05c-133">-Name</span></span>
<span data-ttu-id="0c05c-134">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c05c-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c05c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="0c05c-135">-Pre</span></span>
<span data-ttu-id="0c05c-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="0c05c-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0c05c-137">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0c05c-137">-SubscriptionId</span></span>
<span data-ttu-id="0c05c-138">Identyfikator subskrypcji definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0c05c-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="0c05c-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c05c-139">-Confirm</span></span>
<span data-ttu-id="0c05c-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c05c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c05c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c05c-141">-WhatIf</span></span>
<span data-ttu-id="0c05c-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c05c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c05c-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c05c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c05c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c05c-144">CommonParameters</span></span>
<span data-ttu-id="0c05c-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c05c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c05c-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c05c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c05c-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c05c-147">INPUTS</span></span>

### <span data-ttu-id="0c05c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0c05c-148">System.String</span></span>

### <span data-ttu-id="0c05c-149">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c05c-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0c05c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c05c-150">OUTPUTS</span></span>

### <span data-ttu-id="0c05c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c05c-151">System.Boolean</span></span>

## <span data-ttu-id="0c05c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c05c-152">NOTES</span></span>

## <span data-ttu-id="0c05c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c05c-153">RELATED LINKS</span></span>

[<span data-ttu-id="0c05c-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c05c-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0c05c-155">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c05c-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="0c05c-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c05c-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


