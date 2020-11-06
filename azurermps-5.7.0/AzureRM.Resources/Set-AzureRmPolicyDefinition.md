---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550559"
---
# <span data-ttu-id="7e9fe-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7e9fe-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="7e9fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9fe-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e9fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e9fe-104">SYNTAX</span></span>

### <span data-ttu-id="7e9fe-105">SetByPolicyDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e9fe-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e9fe-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="7e9fe-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e9fe-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7e9fe-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7e9fe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e9fe-108">DESCRIPTION</span></span>
<span data-ttu-id="7e9fe-109">Polecenie cmdlet **Set-AzureRmPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="7e9fe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e9fe-110">EXAMPLES</span></span>

### <span data-ttu-id="7e9fe-111">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="7e9fe-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="7e9fe-112">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7e9fe-113">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="7e9fe-114">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="7e9fe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e9fe-115">PARAMETERS</span></span>

### <span data-ttu-id="7e9fe-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e9fe-116">-ApiVersion</span></span>
<span data-ttu-id="7e9fe-117">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7e9fe-118">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7e9fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9fe-119">-DefaultProfile</span></span>
<span data-ttu-id="7e9fe-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e9fe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e9fe-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="7e9fe-121">-Description</span></span>
<span data-ttu-id="7e9fe-122">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-122">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="7e9fe-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e9fe-123">-DisplayName</span></span>
<span data-ttu-id="7e9fe-124">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-124">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="7e9fe-125">-ID</span><span class="sxs-lookup"><span data-stu-id="7e9fe-125">-Id</span></span>
<span data-ttu-id="7e9fe-126">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7e9fe-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7e9fe-127">-InformationAction</span></span>
<span data-ttu-id="7e9fe-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e9fe-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7e9fe-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e9fe-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7e9fe-130">Continue</span></span>
- <span data-ttu-id="7e9fe-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7e9fe-131">Ignore</span></span>
- <span data-ttu-id="7e9fe-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="7e9fe-132">Inquire</span></span>
- <span data-ttu-id="7e9fe-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7e9fe-133">SilentlyContinue</span></span>
- <span data-ttu-id="7e9fe-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7e9fe-134">Stop</span></span>
- <span data-ttu-id="7e9fe-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7e9fe-135">Suspend</span></span>

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

### <span data-ttu-id="7e9fe-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7e9fe-136">-InformationVariable</span></span>
<span data-ttu-id="7e9fe-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e9fe-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7e9fe-138">-Metadata</span></span>
<span data-ttu-id="7e9fe-139">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-139">The metadata for policy definition.</span></span> <span data-ttu-id="7e9fe-140">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="7e9fe-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e9fe-141">-Name</span></span>
<span data-ttu-id="7e9fe-142">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7e9fe-143">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7e9fe-143">-Parameter</span></span>
<span data-ttu-id="7e9fe-144">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="7e9fe-145">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="7e9fe-146">-Policy</span><span class="sxs-lookup"><span data-stu-id="7e9fe-146">-Policy</span></span>
<span data-ttu-id="7e9fe-147">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="7e9fe-148">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="7e9fe-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="7e9fe-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="7e9fe-149">-Pre</span></span>
<span data-ttu-id="7e9fe-150">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7e9fe-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9fe-151">CommonParameters</span></span>
<span data-ttu-id="7e9fe-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9fe-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9fe-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9fe-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e9fe-154">INPUTS</span></span>

### <span data-ttu-id="7e9fe-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e9fe-155">None</span></span>
<span data-ttu-id="7e9fe-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7e9fe-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e9fe-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e9fe-157">OUTPUTS</span></span>

### <span data-ttu-id="7e9fe-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7e9fe-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7e9fe-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e9fe-159">NOTES</span></span>

## <span data-ttu-id="7e9fe-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e9fe-160">RELATED LINKS</span></span>

[<span data-ttu-id="7e9fe-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7e9fe-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7e9fe-162">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7e9fe-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7e9fe-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7e9fe-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


