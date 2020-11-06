---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542352"
---
# <span data-ttu-id="aec11-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aec11-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="aec11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aec11-102">SYNOPSIS</span></span>
<span data-ttu-id="aec11-103">Tworzy definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aec11-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aec11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aec11-105">DESCRIPTION</span></span>
<span data-ttu-id="aec11-106">Polecenie cmdlet **New-AzureRmPolicyDefinition** umożliwia utworzenie definicji zasad zawierającej regułę zasad w formacie notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="aec11-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="aec11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aec11-107">EXAMPLES</span></span>

### <span data-ttu-id="aec11-108">Przykład 1: Tworzenie definicji zasad przy użyciu pliku zasad</span><span class="sxs-lookup"><span data-stu-id="aec11-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="aec11-109">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition zawierającą regułę określoną w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="aec11-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="aec11-110">Przykład 2: Tworzenie definicji zasad w tekście</span><span class="sxs-lookup"><span data-stu-id="aec11-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="aec11-111">To polecenie tworzy definicję zasad o nazwie VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="aec11-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="aec11-112">To polecenie określa zasadę jako ciąg w prawidłowym formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="aec11-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="aec11-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aec11-113">PARAMETERS</span></span>

### <span data-ttu-id="aec11-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aec11-114">-ApiVersion</span></span>
<span data-ttu-id="aec11-115">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="aec11-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aec11-116">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="aec11-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aec11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec11-117">-DefaultProfile</span></span>
<span data-ttu-id="aec11-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aec11-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aec11-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="aec11-119">-Description</span></span>
<span data-ttu-id="aec11-120">Określa opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-120">Specifies a description for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aec11-121">-DisplayName</span></span>
<span data-ttu-id="aec11-122">Określa nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-122">Specifies a display name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aec11-123">-InformationAction</span></span>
<span data-ttu-id="aec11-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="aec11-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aec11-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="aec11-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aec11-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="aec11-126">Continue</span></span>
- <span data-ttu-id="aec11-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="aec11-127">Ignore</span></span>
- <span data-ttu-id="aec11-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="aec11-128">Inquire</span></span>
- <span data-ttu-id="aec11-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aec11-129">SilentlyContinue</span></span>
- <span data-ttu-id="aec11-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="aec11-130">Stop</span></span>
- <span data-ttu-id="aec11-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="aec11-131">Suspend</span></span>

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

### <span data-ttu-id="aec11-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aec11-132">-InformationVariable</span></span>
<span data-ttu-id="aec11-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="aec11-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aec11-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="aec11-134">-Metadata</span></span>
<span data-ttu-id="aec11-135">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-135">The metadata for policy definition.</span></span> <span data-ttu-id="aec11-136">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="aec11-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-137">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="aec11-137">-Mode</span></span>
<span data-ttu-id="aec11-138">Tryb definicji zasad</span><span class="sxs-lookup"><span data-stu-id="aec11-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aec11-139">-Name</span></span>
<span data-ttu-id="aec11-140">Określa nazwę definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-140">Specifies a name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="aec11-141">-Parameter</span></span>
<span data-ttu-id="aec11-142">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="aec11-143">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="aec11-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="aec11-144">-Policy</span></span>
<span data-ttu-id="aec11-145">Określa regułę zasad dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="aec11-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="aec11-146">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="aec11-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec11-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="aec11-147">-Pre</span></span>
<span data-ttu-id="aec11-148">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="aec11-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aec11-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec11-149">CommonParameters</span></span>
<span data-ttu-id="aec11-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec11-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec11-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec11-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec11-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec11-152">INPUTS</span></span>

### <span data-ttu-id="aec11-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aec11-153">None</span></span>
<span data-ttu-id="aec11-154">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="aec11-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aec11-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aec11-155">OUTPUTS</span></span>

### <span data-ttu-id="aec11-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="aec11-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aec11-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aec11-157">NOTES</span></span>

## <span data-ttu-id="aec11-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec11-158">RELATED LINKS</span></span>

[<span data-ttu-id="aec11-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aec11-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="aec11-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aec11-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="aec11-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aec11-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


