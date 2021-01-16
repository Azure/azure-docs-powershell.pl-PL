---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351730"
---
# <span data-ttu-id="4fcba-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcba-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="4fcba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fcba-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcba-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="4fcba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fcba-104">SYNTAX</span></span>

### <span data-ttu-id="4fcba-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4fcba-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcba-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcba-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcba-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcba-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcba-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcba-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcba-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcba-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fcba-110">Opis</span><span class="sxs-lookup"><span data-stu-id="4fcba-110">DESCRIPTION</span></span>
<span data-ttu-id="4fcba-111">Polecenie cmdlet **Set-AzPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4fcba-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fcba-112">EXAMPLES</span></span>

### <span data-ttu-id="4fcba-113">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="4fcba-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="4fcba-114">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fcba-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4fcba-115">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fcba-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4fcba-116">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fcba-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="4fcba-117">Przykład 2: aktualizowanie trybu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="4fcba-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="4fcba-118">To polecenie aktualizuje definicję zasad o nazwie VMPolicyDefinition za pomocą polecenia cmdlet Set-AzPolicyDefinition w celu ustawienia jego właściwości Mode na wartość wszystkie.</span><span class="sxs-lookup"><span data-stu-id="4fcba-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="4fcba-119">Przykład 3: aktualizowanie metadanych definicji zasad</span><span class="sxs-lookup"><span data-stu-id="4fcba-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="4fcba-120">To polecenie powoduje zaktualizowanie metadanych definicji zasad o nazwie VMPolicyDefinition w celu wskazania jej kategorii "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="4fcba-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="4fcba-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fcba-121">PARAMETERS</span></span>

### <span data-ttu-id="4fcba-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4fcba-122">-ApiVersion</span></span>
<span data-ttu-id="4fcba-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4fcba-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4fcba-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="4fcba-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4fcba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcba-125">-DefaultProfile</span></span>
<span data-ttu-id="4fcba-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4fcba-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fcba-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="4fcba-127">-Description</span></span>
<span data-ttu-id="4fcba-128">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="4fcba-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4fcba-129">-DisplayName</span></span>
<span data-ttu-id="4fcba-130">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="4fcba-131">-ID</span><span class="sxs-lookup"><span data-stu-id="4fcba-131">-Id</span></span>
<span data-ttu-id="4fcba-132">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fcba-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4fcba-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4fcba-133">-InputObject</span></span>
<span data-ttu-id="4fcba-134">Obiekt definicji zasad w celu zaktualizowania danych wyjściowych z innego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fcba-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcba-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcba-135">-ManagementGroupName</span></span>
<span data-ttu-id="4fcba-136">Nazwa grupy zarządzania definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4fcba-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="4fcba-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4fcba-137">-Metadata</span></span>
<span data-ttu-id="4fcba-138">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-138">The metadata for policy definition.</span></span> <span data-ttu-id="4fcba-139">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="4fcba-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="4fcba-140">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="4fcba-140">-Mode</span></span>
<span data-ttu-id="4fcba-141">Tryb nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="4fcba-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fcba-142">-Name</span></span>
<span data-ttu-id="4fcba-143">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="4fcba-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4fcba-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4fcba-144">-Parameter</span></span>
<span data-ttu-id="4fcba-145">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="4fcba-146">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="4fcba-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="4fcba-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="4fcba-147">-Policy</span></span>
<span data-ttu-id="4fcba-148">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="4fcba-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="4fcba-149">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="4fcba-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="4fcba-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="4fcba-150">-Pre</span></span>
<span data-ttu-id="4fcba-151">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="4fcba-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4fcba-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4fcba-152">-SubscriptionId</span></span>
<span data-ttu-id="4fcba-153">Identyfikator subskrypcji definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4fcba-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="4fcba-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcba-154">CommonParameters</span></span>
<span data-ttu-id="4fcba-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fcba-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcba-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fcba-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcba-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fcba-157">INPUTS</span></span>

### <span data-ttu-id="4fcba-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4fcba-158">System.String</span></span>

### <span data-ttu-id="4fcba-159">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4fcba-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4fcba-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fcba-160">OUTPUTS</span></span>

### <span data-ttu-id="4fcba-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4fcba-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4fcba-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fcba-162">NOTES</span></span>

## <span data-ttu-id="4fcba-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fcba-163">RELATED LINKS</span></span>

[<span data-ttu-id="4fcba-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcba-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="4fcba-165">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcba-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="4fcba-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcba-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


