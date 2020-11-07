---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708281"
---
# <span data-ttu-id="c7634-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7634-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="c7634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7634-102">SYNOPSIS</span></span>
<span data-ttu-id="c7634-103">Modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="c7634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7634-104">SYNTAX</span></span>

### <span data-ttu-id="c7634-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c7634-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7634-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7634-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7634-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7634-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7634-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7634-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7634-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c7634-109">DESCRIPTION</span></span>
<span data-ttu-id="c7634-110">Polecenie cmdlet **Set-AzPolicyDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c7634-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7634-111">EXAMPLES</span></span>

### <span data-ttu-id="c7634-112">Przykład 1: aktualizowanie opisu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="c7634-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="c7634-113">Pierwsze polecenie pobiera definicję zasad o nazwie VMPolicyDefinition przy użyciu polecenia cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c7634-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c7634-114">Polecenie zapisuje ten obiekt w zmiennej $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c7634-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="c7634-115">Drugie polecenie aktualizuje opis definicji zasad określonej przez właściwość **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c7634-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="c7634-116">Przykład 2: aktualizowanie trybu definicji zasad</span><span class="sxs-lookup"><span data-stu-id="c7634-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="c7634-117">To polecenie aktualizuje definicję zasad o nazwie VMPolicyDefinition za pomocą polecenia cmdlet Set-AzPolicyDefinition w celu ustawienia jego właściwości Mode na wartość wszystkie.</span><span class="sxs-lookup"><span data-stu-id="c7634-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="c7634-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7634-118">PARAMETERS</span></span>

### <span data-ttu-id="c7634-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c7634-119">-ApiVersion</span></span>
<span data-ttu-id="c7634-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c7634-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c7634-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c7634-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c7634-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7634-122">-DefaultProfile</span></span>
<span data-ttu-id="c7634-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c7634-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7634-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="c7634-124">-Description</span></span>
<span data-ttu-id="c7634-125">Określa nowy opis definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="c7634-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7634-126">-DisplayName</span></span>
<span data-ttu-id="c7634-127">Określa nową nazwę wyświetlaną dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="c7634-128">-ID</span><span class="sxs-lookup"><span data-stu-id="c7634-128">-Id</span></span>
<span data-ttu-id="c7634-129">Określa w pełni kwalifikowany identyfikator zasobów dla definicji zasad, które zmodyfikowano to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7634-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7634-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c7634-130">-ManagementGroupName</span></span>
<span data-ttu-id="c7634-131">Nazwa grupy zarządzania definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c7634-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="c7634-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c7634-132">-Metadata</span></span>
<span data-ttu-id="c7634-133">Metadane definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-133">The metadata for policy definition.</span></span> <span data-ttu-id="c7634-134">Może to być ścieżka do pliku, który zawiera metadane, lub metadanych jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="c7634-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="c7634-135">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="c7634-135">-Mode</span></span>
<span data-ttu-id="c7634-136">Tryb nowej definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="c7634-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7634-137">-Name</span></span>
<span data-ttu-id="c7634-138">Określa nazwę definicji zasad, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="c7634-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7634-139">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c7634-139">-Parameter</span></span>
<span data-ttu-id="c7634-140">Deklaracja Parameters dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="c7634-141">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako String.</span><span class="sxs-lookup"><span data-stu-id="c7634-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="c7634-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="c7634-142">-Policy</span></span>
<span data-ttu-id="c7634-143">Określa nową regułę dla definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c7634-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="c7634-144">Możesz określić ścieżkę pliku JSON lub ciąg zawierający zasadę w formacie notacji kodu języka JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="c7634-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c7634-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="c7634-145">-Pre</span></span>
<span data-ttu-id="c7634-146">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c7634-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c7634-147">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c7634-147">-SubscriptionId</span></span>
<span data-ttu-id="c7634-148">Identyfikator subskrypcji definicji zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c7634-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="c7634-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7634-149">CommonParameters</span></span>
<span data-ttu-id="c7634-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7634-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7634-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7634-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7634-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7634-152">INPUTS</span></span>

### <span data-ttu-id="c7634-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c7634-153">System.String</span></span>

### <span data-ttu-id="c7634-154">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c7634-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c7634-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7634-155">OUTPUTS</span></span>

### <span data-ttu-id="c7634-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c7634-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c7634-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7634-157">NOTES</span></span>

## <span data-ttu-id="c7634-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7634-158">RELATED LINKS</span></span>

[<span data-ttu-id="c7634-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7634-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c7634-160">Nowe — AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7634-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="c7634-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7634-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


