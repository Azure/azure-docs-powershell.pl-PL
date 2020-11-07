---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 160cff39918691c310de6931cd57cb415774d7e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892593"
---
# <span data-ttu-id="a31aa-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a31aa-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="a31aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a31aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a31aa-103">Pobiera przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="a31aa-103">Gets policy assignments.</span></span>

## <span data-ttu-id="a31aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a31aa-104">SYNTAX</span></span>

### <span data-ttu-id="a31aa-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a31aa-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a31aa-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31aa-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a31aa-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31aa-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a31aa-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31aa-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a31aa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a31aa-109">DESCRIPTION</span></span>
<span data-ttu-id="a31aa-110">Polecenie cmdlet **Get-AzPolicyAssignment** pobiera wszystkie przydziały zasad lub określone zadania.</span><span class="sxs-lookup"><span data-stu-id="a31aa-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="a31aa-111">Zidentyfikuj przypisanie zasad, aby uzyskać według nazwy i zakresu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a31aa-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="a31aa-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a31aa-112">EXAMPLES</span></span>

### <span data-ttu-id="a31aa-113">Przykład 1. pobieranie wszystkich przydziałów zasad</span><span class="sxs-lookup"><span data-stu-id="a31aa-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="a31aa-114">To polecenie uzyskuje wszystkie zadania dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="a31aa-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="a31aa-115">Przykład 2: uzyskiwanie określonego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="a31aa-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="a31aa-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdletand zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a31aa-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a31aa-117">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a31aa-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="a31aa-118">Przykład 3: uzyskiwanie wszystkich przypisań zasad przydzielonych do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a31aa-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="a31aa-119">Pierwsze polecenie określa identyfikator grupy zarządzania do zbadania.</span><span class="sxs-lookup"><span data-stu-id="a31aa-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="a31aa-120">Drugie polecenie pobiera wszystkie przydziały zasad, które są przypisane do grupy zarządzania o IDENTYFIKATORze "Moja zarządca".</span><span class="sxs-lookup"><span data-stu-id="a31aa-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="a31aa-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a31aa-121">PARAMETERS</span></span>

### <span data-ttu-id="a31aa-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a31aa-122">-ApiVersion</span></span>
<span data-ttu-id="a31aa-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="a31aa-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a31aa-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="a31aa-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a31aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31aa-125">-DefaultProfile</span></span>
<span data-ttu-id="a31aa-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a31aa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a31aa-127">-ID</span><span class="sxs-lookup"><span data-stu-id="a31aa-127">-Id</span></span>
<span data-ttu-id="a31aa-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31aa-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a31aa-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="a31aa-129">-IncludeDescendent</span></span>
<span data-ttu-id="a31aa-130">Powoduje, że lista zwracanych przypisań zasad obejmuje wszystkie zadania powiązane z danym zakresem, w tym te z zakresów nadrzędnych i te pochodzące od zakresów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="a31aa-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31aa-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a31aa-131">-InformationAction</span></span>
<span data-ttu-id="a31aa-132">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a31aa-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a31aa-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a31aa-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a31aa-134">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a31aa-134">Continue</span></span>
- <span data-ttu-id="a31aa-135">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a31aa-135">Ignore</span></span>
- <span data-ttu-id="a31aa-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="a31aa-136">Inquire</span></span>
- <span data-ttu-id="a31aa-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a31aa-137">SilentlyContinue</span></span>
- <span data-ttu-id="a31aa-138">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a31aa-138">Stop</span></span>
- <span data-ttu-id="a31aa-139">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a31aa-139">Suspend</span></span>

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

### <span data-ttu-id="a31aa-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a31aa-140">-InformationVariable</span></span>
<span data-ttu-id="a31aa-141">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a31aa-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a31aa-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a31aa-142">-Name</span></span>
<span data-ttu-id="a31aa-143">Określa nazwę przypisania zasad, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31aa-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31aa-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a31aa-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="a31aa-145">Określa identyfikator definicji zasad dla przypisań zasad, które jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31aa-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31aa-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="a31aa-146">-Pre</span></span>
<span data-ttu-id="a31aa-147">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="a31aa-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a31aa-148">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a31aa-148">-Scope</span></span>
<span data-ttu-id="a31aa-149">Określa zakres, w którym zasady są stosowane do przydziału, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31aa-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31aa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31aa-150">CommonParameters</span></span>
<span data-ttu-id="a31aa-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31aa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31aa-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31aa-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31aa-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a31aa-153">INPUTS</span></span>

## <span data-ttu-id="a31aa-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a31aa-154">OUTPUTS</span></span>

## <span data-ttu-id="a31aa-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a31aa-155">NOTES</span></span>

## <span data-ttu-id="a31aa-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a31aa-156">RELATED LINKS</span></span>

[<span data-ttu-id="a31aa-157">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a31aa-157">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="a31aa-158">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a31aa-158">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="a31aa-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a31aa-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


