---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 4f71814790d5c543a867ad4de0aaac37c98079a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552556"
---
# <span data-ttu-id="02fc4-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="02fc4-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="02fc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="02fc4-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02fc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02fc4-104">SYNTAX</span></span>

### <span data-ttu-id="02fc4-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02fc4-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02fc4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02fc4-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02fc4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02fc4-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02fc4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02fc4-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="02fc4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="02fc4-109">DESCRIPTION</span></span>
<span data-ttu-id="02fc4-110">Polecenie cmdlet **Set-AzureRmPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="02fc4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02fc4-111">EXAMPLES</span></span>

### <span data-ttu-id="02fc4-112">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="02fc4-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="02fc4-113">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="02fc4-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="02fc4-114">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="02fc4-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="02fc4-115">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="02fc4-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="02fc4-116">Przykład 2: aktualizowanie trybu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="02fc4-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="02fc4-117">To polecenie aktualizuje definicję zasad o nazwie VMPolicyDefinition za pomocą polecenia cmdlet Set-AzureRmPolicyDefinition w celu ustawienia jego właściwości Mode na wartość wszystkie.</span><span class="sxs-lookup"><span data-stu-id="02fc4-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="02fc4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02fc4-118">PARAMETERS</span></span>

### <span data-ttu-id="02fc4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="02fc4-119">-ApiVersion</span></span>
<span data-ttu-id="02fc4-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="02fc4-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="02fc4-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="02fc4-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="02fc4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fc4-122">-DefaultProfile</span></span>
<span data-ttu-id="02fc4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02fc4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02fc4-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="02fc4-124">-Description</span></span>
<span data-ttu-id="02fc4-125">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="02fc4-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02fc4-126">-DisplayName</span></span>
<span data-ttu-id="02fc4-127">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="02fc4-128">-ID</span><span class="sxs-lookup"><span data-stu-id="02fc4-128">-Id</span></span>
<span data-ttu-id="02fc4-129">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02fc4-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="02fc4-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="02fc4-130">-InformationAction</span></span>
<span data-ttu-id="02fc4-131">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="02fc4-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="02fc4-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="02fc4-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02fc4-133">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="02fc4-133">Continue</span></span>
- <span data-ttu-id="02fc4-134">Ignorować</span><span class="sxs-lookup"><span data-stu-id="02fc4-134">Ignore</span></span>
- <span data-ttu-id="02fc4-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="02fc4-135">Inquire</span></span>
- <span data-ttu-id="02fc4-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="02fc4-136">SilentlyContinue</span></span>
- <span data-ttu-id="02fc4-137">Przestaw</span><span class="sxs-lookup"><span data-stu-id="02fc4-137">Stop</span></span>
- <span data-ttu-id="02fc4-138">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="02fc4-138">Suspend</span></span>

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

### <span data-ttu-id="02fc4-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="02fc4-139">-InformationVariable</span></span>
<span data-ttu-id="02fc4-140">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="02fc4-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="02fc4-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="02fc4-141">-ManagementGroupName</span></span>
<span data-ttu-id="02fc4-142">Nazwa grupy zarządzania definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="02fc4-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="02fc4-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="02fc4-143">-Metadata</span></span>
<span data-ttu-id="02fc4-144">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-144">The metadata for policy definition.</span></span> <span data-ttu-id="02fc4-145">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="02fc4-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="02fc4-146">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="02fc4-146">-Mode</span></span>
<span data-ttu-id="02fc4-147">Tryb nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02fc4-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02fc4-148">-Name</span></span>
<span data-ttu-id="02fc4-149">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="02fc4-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02fc4-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="02fc4-150">-Parameter</span></span>
<span data-ttu-id="02fc4-151">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="02fc4-152">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="02fc4-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="02fc4-153">-Policy</span><span class="sxs-lookup"><span data-stu-id="02fc4-153">-Policy</span></span>
<span data-ttu-id="02fc4-154">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="02fc4-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="02fc4-155">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="02fc4-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="02fc4-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="02fc4-156">-Pre</span></span>
<span data-ttu-id="02fc4-157">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="02fc4-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="02fc4-158">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="02fc4-158">-SubscriptionId</span></span>
<span data-ttu-id="02fc4-159">Identyfikator subskrypcji definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="02fc4-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="02fc4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fc4-160">CommonParameters</span></span>
<span data-ttu-id="02fc4-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02fc4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fc4-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02fc4-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fc4-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02fc4-163">INPUTS</span></span>

## <span data-ttu-id="02fc4-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02fc4-164">OUTPUTS</span></span>

## <span data-ttu-id="02fc4-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02fc4-165">NOTES</span></span>

## <span data-ttu-id="02fc4-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02fc4-166">RELATED LINKS</span></span>

[<span data-ttu-id="02fc4-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="02fc4-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="02fc4-168">Nowe — AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="02fc4-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="02fc4-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="02fc4-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


