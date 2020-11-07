---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718706"
---
# <span data-ttu-id="89397-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89397-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="89397-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89397-102">SYNOPSIS</span></span>
<span data-ttu-id="89397-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89397-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89397-104">SYNTAX</span></span>

### <span data-ttu-id="89397-105">Zestaw parametrów Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-105">The policy definition name parameter set.</span></span> <span data-ttu-id="89397-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="89397-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89397-107">Zestaw parametrów identyfikatora definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89397-108">Opis</span><span class="sxs-lookup"><span data-stu-id="89397-108">DESCRIPTION</span></span>
<span data-ttu-id="89397-109">Polecenie cmdlet **Set-AzureRmPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="89397-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89397-110">EXAMPLES</span></span>

### <span data-ttu-id="89397-111">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="89397-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="89397-112">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="89397-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="89397-113">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="89397-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="89397-114">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="89397-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="89397-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89397-115">PARAMETERS</span></span>

### <span data-ttu-id="89397-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89397-116">-ApiVersion</span></span>
<span data-ttu-id="89397-117">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="89397-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="89397-118">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="89397-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="89397-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="89397-119">-Description</span></span>
<span data-ttu-id="89397-120">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-120">Specifies a new description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89397-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89397-121">-DisplayName</span></span>
<span data-ttu-id="89397-122">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-122">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89397-123">-ID</span><span class="sxs-lookup"><span data-stu-id="89397-123">-Id</span></span>
<span data-ttu-id="89397-124">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89397-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89397-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89397-125">-InformationAction</span></span>
<span data-ttu-id="89397-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="89397-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89397-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89397-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89397-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="89397-128">Continue</span></span>
- <span data-ttu-id="89397-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="89397-129">Ignore</span></span>
- <span data-ttu-id="89397-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="89397-130">Inquire</span></span>
- <span data-ttu-id="89397-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89397-131">SilentlyContinue</span></span>
- <span data-ttu-id="89397-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="89397-132">Stop</span></span>
- <span data-ttu-id="89397-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="89397-133">Suspend</span></span>

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

### <span data-ttu-id="89397-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89397-134">-InformationVariable</span></span>
<span data-ttu-id="89397-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="89397-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89397-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89397-136">-Name</span></span>
<span data-ttu-id="89397-137">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="89397-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89397-138">-Policy</span><span class="sxs-lookup"><span data-stu-id="89397-138">-Policy</span></span>
<span data-ttu-id="89397-139">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="89397-140">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="89397-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89397-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="89397-141">-Pre</span></span>
<span data-ttu-id="89397-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="89397-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="89397-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89397-143">-DefaultProfile</span></span>
<span data-ttu-id="89397-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89397-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89397-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="89397-145">-Metadata</span></span>
<span data-ttu-id="89397-146">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-146">The metadata for policy definition.</span></span> <span data-ttu-id="89397-147">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="89397-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89397-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="89397-148">-Parameter</span></span>
<span data-ttu-id="89397-149">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="89397-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="89397-150">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="89397-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89397-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89397-151">CommonParameters</span></span>
<span data-ttu-id="89397-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89397-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89397-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89397-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89397-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89397-154">INPUTS</span></span>

## <span data-ttu-id="89397-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89397-155">OUTPUTS</span></span>

### <span data-ttu-id="89397-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="89397-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="89397-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89397-157">NOTES</span></span>

## <span data-ttu-id="89397-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89397-158">RELATED LINKS</span></span>

[<span data-ttu-id="89397-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89397-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="89397-160">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89397-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="89397-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89397-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


