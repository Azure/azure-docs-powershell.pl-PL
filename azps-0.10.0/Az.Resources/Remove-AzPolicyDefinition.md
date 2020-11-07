---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892398"
---
# <span data-ttu-id="04806-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04806-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="04806-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04806-102">SYNOPSIS</span></span>
<span data-ttu-id="04806-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="04806-103">Removes a policy definition.</span></span>

## <span data-ttu-id="04806-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04806-104">SYNTAX</span></span>

### <span data-ttu-id="04806-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04806-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04806-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04806-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04806-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04806-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04806-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04806-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04806-109">Opis</span><span class="sxs-lookup"><span data-stu-id="04806-109">DESCRIPTION</span></span>
<span data-ttu-id="04806-110">Polecenie cmdlet **Remove-AzPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="04806-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="04806-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04806-111">EXAMPLES</span></span>

### <span data-ttu-id="04806-112">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="04806-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="04806-113">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="04806-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="04806-114">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="04806-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="04806-115">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04806-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="04806-116">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04806-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="04806-117">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04806-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="04806-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04806-118">PARAMETERS</span></span>

### <span data-ttu-id="04806-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="04806-119">-ApiVersion</span></span>
<span data-ttu-id="04806-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="04806-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="04806-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="04806-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="04806-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04806-122">-DefaultProfile</span></span>
<span data-ttu-id="04806-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="04806-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04806-124">-Force</span><span class="sxs-lookup"><span data-stu-id="04806-124">-Force</span></span>
<span data-ttu-id="04806-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="04806-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04806-126">-ID</span><span class="sxs-lookup"><span data-stu-id="04806-126">-Id</span></span>
<span data-ttu-id="04806-127">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04806-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="04806-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04806-128">-InformationAction</span></span>
<span data-ttu-id="04806-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="04806-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="04806-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04806-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04806-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="04806-131">Continue</span></span>
- <span data-ttu-id="04806-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="04806-132">Ignore</span></span>
- <span data-ttu-id="04806-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="04806-133">Inquire</span></span>
- <span data-ttu-id="04806-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04806-134">SilentlyContinue</span></span>
- <span data-ttu-id="04806-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="04806-135">Stop</span></span>
- <span data-ttu-id="04806-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="04806-136">Suspend</span></span>

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

### <span data-ttu-id="04806-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04806-137">-InformationVariable</span></span>
<span data-ttu-id="04806-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="04806-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="04806-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="04806-139">-ManagementGroupName</span></span>
<span data-ttu-id="04806-140">Nazwa grupy zarządzania definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="04806-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="04806-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04806-141">-Name</span></span>
<span data-ttu-id="04806-142">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04806-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="04806-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="04806-143">-Pre</span></span>
<span data-ttu-id="04806-144">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="04806-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="04806-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="04806-145">-SubscriptionId</span></span>
<span data-ttu-id="04806-146">Identyfikator subskrypcji definicji zasad do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="04806-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="04806-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04806-147">-Confirm</span></span>
<span data-ttu-id="04806-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04806-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04806-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04806-149">-WhatIf</span></span>
<span data-ttu-id="04806-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04806-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04806-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04806-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04806-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04806-152">CommonParameters</span></span>
<span data-ttu-id="04806-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04806-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04806-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04806-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04806-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04806-155">INPUTS</span></span>

## <span data-ttu-id="04806-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04806-156">OUTPUTS</span></span>

## <span data-ttu-id="04806-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04806-157">NOTES</span></span>

## <span data-ttu-id="04806-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04806-158">RELATED LINKS</span></span>

[<span data-ttu-id="04806-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04806-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="04806-160">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04806-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="04806-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04806-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


