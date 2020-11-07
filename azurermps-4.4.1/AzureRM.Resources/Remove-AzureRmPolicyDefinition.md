---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718709"
---
# <span data-ttu-id="4cbee-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cbee-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4cbee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cbee-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbee-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4cbee-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cbee-104">SYNTAX</span></span>

### <span data-ttu-id="4cbee-105">Zestaw parametrów Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4cbee-105">The policy definition name parameter set.</span></span> <span data-ttu-id="4cbee-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="4cbee-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbee-107">Zestaw parametrów identyfikatora definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4cbee-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cbee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4cbee-108">DESCRIPTION</span></span>
<span data-ttu-id="4cbee-109">Polecenie cmdlet **Remove-AzureRmPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4cbee-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="4cbee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cbee-110">EXAMPLES</span></span>

### <span data-ttu-id="4cbee-111">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="4cbee-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="4cbee-112">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4cbee-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="4cbee-113">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="4cbee-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="4cbee-114">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cbee-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4cbee-115">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cbee-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="4cbee-116">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cbee-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4cbee-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cbee-117">PARAMETERS</span></span>

### <span data-ttu-id="4cbee-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cbee-118">-ApiVersion</span></span>
<span data-ttu-id="4cbee-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4cbee-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4cbee-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="4cbee-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4cbee-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4cbee-121">-Force</span></span>
<span data-ttu-id="4cbee-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4cbee-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cbee-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4cbee-123">-Id</span></span>
<span data-ttu-id="4cbee-124">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbee-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbee-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4cbee-125">-InformationAction</span></span>
<span data-ttu-id="4cbee-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4cbee-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4cbee-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4cbee-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4cbee-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4cbee-128">Continue</span></span>
- <span data-ttu-id="4cbee-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4cbee-129">Ignore</span></span>
- <span data-ttu-id="4cbee-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="4cbee-130">Inquire</span></span>
- <span data-ttu-id="4cbee-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4cbee-131">SilentlyContinue</span></span>
- <span data-ttu-id="4cbee-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4cbee-132">Stop</span></span>
- <span data-ttu-id="4cbee-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4cbee-133">Suspend</span></span>

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

### <span data-ttu-id="4cbee-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4cbee-134">-InformationVariable</span></span>
<span data-ttu-id="4cbee-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4cbee-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4cbee-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4cbee-136">-Name</span></span>
<span data-ttu-id="4cbee-137">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbee-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbee-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="4cbee-138">-Pre</span></span>
<span data-ttu-id="4cbee-139">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="4cbee-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4cbee-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cbee-140">-Confirm</span></span>
<span data-ttu-id="4cbee-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbee-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbee-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbee-142">-WhatIf</span></span>
<span data-ttu-id="4cbee-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbee-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cbee-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cbee-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbee-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbee-145">-DefaultProfile</span></span>
<span data-ttu-id="4cbee-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbee-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbee-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbee-147">CommonParameters</span></span>
<span data-ttu-id="4cbee-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbee-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbee-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbee-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbee-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cbee-150">INPUTS</span></span>

## <span data-ttu-id="4cbee-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cbee-151">OUTPUTS</span></span>

### <span data-ttu-id="4cbee-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cbee-152">System.Boolean</span></span>

## <span data-ttu-id="4cbee-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cbee-153">NOTES</span></span>

## <span data-ttu-id="4cbee-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cbee-154">RELATED LINKS</span></span>

[<span data-ttu-id="4cbee-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cbee-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4cbee-156">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cbee-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4cbee-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cbee-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


