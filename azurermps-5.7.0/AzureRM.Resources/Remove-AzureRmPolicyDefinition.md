---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716612"
---
# <span data-ttu-id="71e1e-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71e1e-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="71e1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="71e1e-103">Usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="71e1e-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71e1e-104">SYNTAX</span></span>

### <span data-ttu-id="71e1e-105">RemoveByPolicyDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71e1e-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e1e-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="71e1e-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e1e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="71e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="71e1e-108">Polecenie cmdlet **Remove-AzureRmPolicyDefinition** usuwa definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="71e1e-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="71e1e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71e1e-109">EXAMPLES</span></span>

### <span data-ttu-id="71e1e-110">Przykład 1: usuwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="71e1e-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="71e1e-111">To polecenie umożliwia usunięcie określonej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="71e1e-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="71e1e-112">Przykład 2: usuwanie definicji zasad według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="71e1e-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="71e1e-113">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71e1e-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="71e1e-114">Polecenie zapisuje je w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71e1e-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="71e1e-115">Drugie polecenie usuwa definicję zasad zidentyfikowaną przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71e1e-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="71e1e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71e1e-116">PARAMETERS</span></span>

### <span data-ttu-id="71e1e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71e1e-117">-ApiVersion</span></span>
<span data-ttu-id="71e1e-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="71e1e-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="71e1e-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="71e1e-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e1e-120">-DefaultProfile</span></span>
<span data-ttu-id="71e1e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="71e1e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="71e1e-122">-Force</span></span>
<span data-ttu-id="71e1e-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="71e1e-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="71e1e-124">-Id</span></span>
<span data-ttu-id="71e1e-125">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e1e-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71e1e-126">-InformationAction</span></span>
<span data-ttu-id="71e1e-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="71e1e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71e1e-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="71e1e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71e1e-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="71e1e-129">Continue</span></span>
- <span data-ttu-id="71e1e-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="71e1e-130">Ignore</span></span>
- <span data-ttu-id="71e1e-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="71e1e-131">Inquire</span></span>
- <span data-ttu-id="71e1e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71e1e-132">SilentlyContinue</span></span>
- <span data-ttu-id="71e1e-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="71e1e-133">Stop</span></span>
- <span data-ttu-id="71e1e-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="71e1e-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71e1e-135">-InformationVariable</span></span>
<span data-ttu-id="71e1e-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="71e1e-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71e1e-137">-Name</span></span>
<span data-ttu-id="71e1e-138">Określa nazwę definicji zasad, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e1e-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="71e1e-139">-Pre</span></span>
<span data-ttu-id="71e1e-140">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="71e1e-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71e1e-141">-Confirm</span></span>
<span data-ttu-id="71e1e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e1e-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e1e-143">-WhatIf</span></span>
<span data-ttu-id="71e1e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e1e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e1e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71e1e-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e1e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e1e-146">CommonParameters</span></span>
<span data-ttu-id="71e1e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e1e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e1e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e1e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e1e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e1e-149">INPUTS</span></span>

### <span data-ttu-id="71e1e-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71e1e-150">None</span></span>
<span data-ttu-id="71e1e-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="71e1e-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71e1e-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71e1e-152">OUTPUTS</span></span>

### <span data-ttu-id="71e1e-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71e1e-153">System.Boolean</span></span>

## <span data-ttu-id="71e1e-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71e1e-154">NOTES</span></span>

## <span data-ttu-id="71e1e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e1e-155">RELATED LINKS</span></span>

[<span data-ttu-id="71e1e-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71e1e-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71e1e-157">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71e1e-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71e1e-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71e1e-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


