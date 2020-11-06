---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550576"
---
# <span data-ttu-id="db92c-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db92c-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="db92c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db92c-102">SYNOPSIS</span></span>
<span data-ttu-id="db92c-103">Pobiera definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="db92c-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db92c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db92c-104">SYNTAX</span></span>

### <span data-ttu-id="db92c-105">GetAllPolicyDefinitions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db92c-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="db92c-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="db92c-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="db92c-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="db92c-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="db92c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="db92c-108">DESCRIPTION</span></span>
<span data-ttu-id="db92c-109">Polecenie cmdlet **Get-AzureRmPolicyDefinition** pobiera wszystkie definicje zasad lub określoną definicję zasady zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="db92c-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="db92c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db92c-110">EXAMPLES</span></span>

### <span data-ttu-id="db92c-111">Przykład 1: pobieranie wszystkich definicji zasad</span><span class="sxs-lookup"><span data-stu-id="db92c-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="db92c-112">To polecenie pobiera wszystkie definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="db92c-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="db92c-113">Przykład 2: uzyskiwanie definicji zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="db92c-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="db92c-114">To polecenie pobiera definicję zasad o nazwie VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="db92c-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="db92c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db92c-115">PARAMETERS</span></span>

### <span data-ttu-id="db92c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="db92c-116">-ApiVersion</span></span>
<span data-ttu-id="db92c-117">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="db92c-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="db92c-118">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="db92c-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="db92c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db92c-119">-DefaultProfile</span></span>
<span data-ttu-id="db92c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="db92c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db92c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="db92c-121">-Id</span></span>
<span data-ttu-id="db92c-122">Określa w pełni kwalifikowany identyfikator zasobu dla definicji zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db92c-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db92c-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="db92c-123">-InformationAction</span></span>
<span data-ttu-id="db92c-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="db92c-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="db92c-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="db92c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db92c-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="db92c-126">Continue</span></span>
- <span data-ttu-id="db92c-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="db92c-127">Ignore</span></span>
- <span data-ttu-id="db92c-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="db92c-128">Inquire</span></span>
- <span data-ttu-id="db92c-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="db92c-129">SilentlyContinue</span></span>
- <span data-ttu-id="db92c-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="db92c-130">Stop</span></span>
- <span data-ttu-id="db92c-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="db92c-131">Suspend</span></span>

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

### <span data-ttu-id="db92c-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="db92c-132">-InformationVariable</span></span>
<span data-ttu-id="db92c-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="db92c-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="db92c-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db92c-134">-Name</span></span>
<span data-ttu-id="db92c-135">Określa nazwę definicji zasad, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db92c-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db92c-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="db92c-136">-Pre</span></span>
<span data-ttu-id="db92c-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="db92c-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db92c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db92c-138">CommonParameters</span></span>
<span data-ttu-id="db92c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db92c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db92c-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db92c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db92c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db92c-141">INPUTS</span></span>

### <span data-ttu-id="db92c-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="db92c-142">None</span></span>
<span data-ttu-id="db92c-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="db92c-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db92c-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db92c-144">OUTPUTS</span></span>

### <span data-ttu-id="db92c-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="db92c-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="db92c-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db92c-146">NOTES</span></span>

## <span data-ttu-id="db92c-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db92c-147">RELATED LINKS</span></span>

[<span data-ttu-id="db92c-148">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db92c-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="db92c-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db92c-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="db92c-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db92c-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


