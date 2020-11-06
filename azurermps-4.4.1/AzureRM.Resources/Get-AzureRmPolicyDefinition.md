---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552368"
---
# <span data-ttu-id="780b1-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="780b1-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="780b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="780b1-102">SYNOPSIS</span></span>
<span data-ttu-id="780b1-103">Pobiera definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="780b1-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="780b1-104">SYNTAX</span></span>

### <span data-ttu-id="780b1-105">Zestaw parametrów lista wszystkich definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="780b1-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="780b1-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="780b1-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="780b1-107">Zestaw parametrów Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="780b1-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="780b1-108">Zestaw parametrów identyfikatora definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="780b1-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="780b1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="780b1-109">DESCRIPTION</span></span>
<span data-ttu-id="780b1-110">Polecenie cmdlet **Get-AzureRmPolicyDefinition** pobiera wszystkie definicje zasad lub określoną definicję zasady zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="780b1-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="780b1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="780b1-111">EXAMPLES</span></span>

### <span data-ttu-id="780b1-112">Przykład 1: pobieranie wszystkich definicji zasad</span><span class="sxs-lookup"><span data-stu-id="780b1-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="780b1-113">To polecenie pobiera wszystkie definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="780b1-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="780b1-114">Przykład 2: uzyskiwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="780b1-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="780b1-115">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="780b1-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="780b1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="780b1-116">PARAMETERS</span></span>

### <span data-ttu-id="780b1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="780b1-117">-ApiVersion</span></span>
<span data-ttu-id="780b1-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="780b1-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="780b1-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="780b1-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="780b1-120">-ID</span><span class="sxs-lookup"><span data-stu-id="780b1-120">-Id</span></span>
<span data-ttu-id="780b1-121">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="780b1-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="780b1-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="780b1-122">-InformationAction</span></span>
<span data-ttu-id="780b1-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="780b1-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="780b1-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="780b1-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="780b1-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="780b1-125">Continue</span></span>
- <span data-ttu-id="780b1-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="780b1-126">Ignore</span></span>
- <span data-ttu-id="780b1-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="780b1-127">Inquire</span></span>
- <span data-ttu-id="780b1-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="780b1-128">SilentlyContinue</span></span>
- <span data-ttu-id="780b1-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="780b1-129">Stop</span></span>
- <span data-ttu-id="780b1-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="780b1-130">Suspend</span></span>

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

### <span data-ttu-id="780b1-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="780b1-131">-InformationVariable</span></span>
<span data-ttu-id="780b1-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="780b1-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="780b1-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="780b1-133">-Name</span></span>
<span data-ttu-id="780b1-134">Określa nazwę definicji zasad, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="780b1-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="780b1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="780b1-135">-Pre</span></span>
<span data-ttu-id="780b1-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="780b1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="780b1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780b1-137">-DefaultProfile</span></span>
<span data-ttu-id="780b1-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="780b1-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="780b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780b1-139">CommonParameters</span></span>
<span data-ttu-id="780b1-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780b1-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780b1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780b1-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="780b1-142">INPUTS</span></span>

## <span data-ttu-id="780b1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="780b1-143">OUTPUTS</span></span>

### <span data-ttu-id="780b1-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="780b1-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="780b1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="780b1-145">NOTES</span></span>

## <span data-ttu-id="780b1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="780b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="780b1-147">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="780b1-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="780b1-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="780b1-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="780b1-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="780b1-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


