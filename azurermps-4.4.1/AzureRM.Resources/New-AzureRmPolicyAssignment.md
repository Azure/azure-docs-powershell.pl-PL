---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718101"
---
# <span data-ttu-id="b3c90-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b3c90-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b3c90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3c90-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c90-103">Tworzy przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="b3c90-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3c90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3c90-104">SYNTAX</span></span>

### <span data-ttu-id="b3c90-105">Przypisanie zasad bez parametrów (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b3c90-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-106">Przypisanie zasad z parametrami za pośrednictwem obiektu parametru zasad</span><span class="sxs-lookup"><span data-stu-id="b3c90-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-107">Przypisanie zasad z parametrami za pośrednictwem ciągu parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="b3c90-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-108">Przypisanie zasad z parametrami za pośrednictwem obiektu parametru zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b3c90-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-109">Przypisanie zasad z parametrami za pośrednictwem ciągu parametru zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b3c90-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b3c90-110">Opis</span><span class="sxs-lookup"><span data-stu-id="b3c90-110">DESCRIPTION</span></span>
<span data-ttu-id="b3c90-111">Polecenie cmdlet **New-AzureRmPolicyAssignment** tworzy przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="b3c90-112">Określ zasady i zakres.</span><span class="sxs-lookup"><span data-stu-id="b3c90-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="b3c90-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3c90-113">EXAMPLES</span></span>

### <span data-ttu-id="b3c90-114">Przykład 1: przydział zasad na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3c90-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b3c90-115">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b3c90-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b3c90-116">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b3c90-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="b3c90-117">Drugie polecenie pobiera definicję zasad o nazwie VirtualMachinePolicy przy użyciu polecenia cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b3c90-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b3c90-118">Polecenie zapisuje ten obiekt w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="b3c90-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="b3c90-119">Polecenie ostatnie przypisuje zasady w $Policy na poziomie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3c90-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="b3c90-120">Właściwość **ResourceId** $ResourceGroup identyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3c90-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="b3c90-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3c90-121">PARAMETERS</span></span>

### <span data-ttu-id="b3c90-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3c90-122">-ApiVersion</span></span>
<span data-ttu-id="b3c90-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b3c90-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b3c90-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="b3c90-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b3c90-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3c90-125">-DisplayName</span></span>
<span data-ttu-id="b3c90-126">Określa nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b3c90-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b3c90-127">-InformationAction</span></span>
<span data-ttu-id="b3c90-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b3c90-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b3c90-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b3c90-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3c90-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b3c90-130">Continue</span></span>
- <span data-ttu-id="b3c90-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b3c90-131">Ignore</span></span>
- <span data-ttu-id="b3c90-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="b3c90-132">Inquire</span></span>
- <span data-ttu-id="b3c90-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b3c90-133">SilentlyContinue</span></span>
- <span data-ttu-id="b3c90-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b3c90-134">Stop</span></span>
- <span data-ttu-id="b3c90-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b3c90-135">Suspend</span></span>

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

### <span data-ttu-id="b3c90-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b3c90-136">-InformationVariable</span></span>
<span data-ttu-id="b3c90-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b3c90-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b3c90-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3c90-138">-Name</span></span>
<span data-ttu-id="b3c90-139">Określa nazwę przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b3c90-140">-NotScope</span></span>
<span data-ttu-id="b3c90-141">Nie zakresy przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-141">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3c90-142">-PolicyDefinition</span></span>
<span data-ttu-id="b3c90-143">Określa zasadę, jako obiekt **PSObject** , który zawiera regułę zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b3c90-144">-PolicyParameter</span></span>
<span data-ttu-id="b3c90-145">Ścieżka pliku parametru zasad lub ciąg parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b3c90-146">-PolicyParameterObject</span></span>
<span data-ttu-id="b3c90-147">Obiekt parametru zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b3c90-148">-PolicySetDefinition</span></span>
<span data-ttu-id="b3c90-149">Obiekt definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3c90-150">-Pre</span></span>
<span data-ttu-id="b3c90-151">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b3c90-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b3c90-152">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b3c90-152">-Scope</span></span>
<span data-ttu-id="b3c90-153">Określa zakres, do którego należy przypisać zasady.</span><span class="sxs-lookup"><span data-stu-id="b3c90-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="b3c90-154">Aby na przykład przypisać zasadę do grupy zasobów, określ następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="b3c90-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="b3c90-155">`/subscriptions/``/resourcegroups/`Nazwa grupy zasobów identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b3c90-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c90-156">-DefaultProfile</span></span>
<span data-ttu-id="b3c90-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c90-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3c90-158">— Opis</span><span class="sxs-lookup"><span data-stu-id="b3c90-158">-Description</span></span>
<span data-ttu-id="b3c90-159">Opis przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b3c90-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="b3c90-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="b3c90-160">-Sku</span></span>
<span data-ttu-id="b3c90-161">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="b3c90-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="b3c90-162">Domyślnie jest to bezpłatna wersja jednostki SKU: name = a0, warstwa = Free</span><span class="sxs-lookup"><span data-stu-id="b3c90-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c90-163">CommonParameters</span></span>
<span data-ttu-id="b3c90-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c90-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c90-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c90-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c90-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3c90-166">INPUTS</span></span>

## <span data-ttu-id="b3c90-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3c90-167">OUTPUTS</span></span>

### <span data-ttu-id="b3c90-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b3c90-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b3c90-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3c90-169">NOTES</span></span>

## <span data-ttu-id="b3c90-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3c90-170">RELATED LINKS</span></span>

[<span data-ttu-id="b3c90-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3c90-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b3c90-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b3c90-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b3c90-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b3c90-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b3c90-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b3c90-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


