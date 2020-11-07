---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: feddd9645b22c554d5e78813194ecc8837fdf3fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892349"
---
# <span data-ttu-id="4bbfc-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bbfc-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="4bbfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbfc-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="4bbfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bbfc-104">SYNTAX</span></span>

### <span data-ttu-id="4bbfc-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bbfc-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4bbfc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bbfc-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4bbfc-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bbfc-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4bbfc-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bbfc-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4bbfc-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4bbfc-109">DESCRIPTION</span></span>
<span data-ttu-id="4bbfc-110">Polecenie cmdlet **Set-AzPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4bbfc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bbfc-111">EXAMPLES</span></span>

### <span data-ttu-id="4bbfc-112">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="4bbfc-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="4bbfc-113">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4bbfc-114">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4bbfc-115">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="4bbfc-116">Przykład 2: aktualizowanie trybu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="4bbfc-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="4bbfc-117">To polecenie aktualizuje definicję zasad o nazwie VMPolicyDefinition za pomocą polecenia cmdlet Set-AzPolicyDefinition w celu ustawienia jego właściwości Mode na wartość wszystkie.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="4bbfc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bbfc-118">PARAMETERS</span></span>

### <span data-ttu-id="4bbfc-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4bbfc-119">-ApiVersion</span></span>
<span data-ttu-id="4bbfc-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4bbfc-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4bbfc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbfc-122">-DefaultProfile</span></span>
<span data-ttu-id="4bbfc-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4bbfc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bbfc-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="4bbfc-124">-Description</span></span>
<span data-ttu-id="4bbfc-125">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="4bbfc-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4bbfc-126">-DisplayName</span></span>
<span data-ttu-id="4bbfc-127">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="4bbfc-128">-ID</span><span class="sxs-lookup"><span data-stu-id="4bbfc-128">-Id</span></span>
<span data-ttu-id="4bbfc-129">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4bbfc-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4bbfc-130">-InformationAction</span></span>
<span data-ttu-id="4bbfc-131">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="4bbfc-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4bbfc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4bbfc-133">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4bbfc-133">Continue</span></span>
- <span data-ttu-id="4bbfc-134">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4bbfc-134">Ignore</span></span>
- <span data-ttu-id="4bbfc-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="4bbfc-135">Inquire</span></span>
- <span data-ttu-id="4bbfc-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4bbfc-136">SilentlyContinue</span></span>
- <span data-ttu-id="4bbfc-137">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4bbfc-137">Stop</span></span>
- <span data-ttu-id="4bbfc-138">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4bbfc-138">Suspend</span></span>

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

### <span data-ttu-id="4bbfc-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4bbfc-139">-InformationVariable</span></span>
<span data-ttu-id="4bbfc-140">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4bbfc-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbfc-141">-ManagementGroupName</span></span>
<span data-ttu-id="4bbfc-142">Nazwa grupy zarządzania definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="4bbfc-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4bbfc-143">-Metadata</span></span>
<span data-ttu-id="4bbfc-144">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-144">The metadata for policy definition.</span></span> <span data-ttu-id="4bbfc-145">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="4bbfc-146">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="4bbfc-146">-Mode</span></span>
<span data-ttu-id="4bbfc-147">Tryb nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="4bbfc-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4bbfc-148">-Name</span></span>
<span data-ttu-id="4bbfc-149">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4bbfc-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4bbfc-150">-Parameter</span></span>
<span data-ttu-id="4bbfc-151">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="4bbfc-152">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="4bbfc-153">-Policy</span><span class="sxs-lookup"><span data-stu-id="4bbfc-153">-Policy</span></span>
<span data-ttu-id="4bbfc-154">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="4bbfc-155">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="4bbfc-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="4bbfc-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="4bbfc-156">-Pre</span></span>
<span data-ttu-id="4bbfc-157">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4bbfc-158">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4bbfc-158">-SubscriptionId</span></span>
<span data-ttu-id="4bbfc-159">Identyfikator subskrypcji definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="4bbfc-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbfc-160">CommonParameters</span></span>
<span data-ttu-id="4bbfc-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbfc-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbfc-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbfc-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbfc-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bbfc-163">INPUTS</span></span>

## <span data-ttu-id="4bbfc-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bbfc-164">OUTPUTS</span></span>

## <span data-ttu-id="4bbfc-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bbfc-165">NOTES</span></span>

## <span data-ttu-id="4bbfc-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bbfc-166">RELATED LINKS</span></span>

[<span data-ttu-id="4bbfc-167">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bbfc-167">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="4bbfc-168">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bbfc-168">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="4bbfc-169">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bbfc-169">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


