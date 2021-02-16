---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186499"
---
# <span data-ttu-id="aadfe-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="aadfe-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="aadfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aadfe-102">SYNOPSIS</span></span>
<span data-ttu-id="aadfe-103">Otrzymuje przydziały zasad.</span><span class="sxs-lookup"><span data-stu-id="aadfe-103">Gets policy assignments.</span></span>

## <span data-ttu-id="aadfe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aadfe-104">SYNTAX</span></span>

### <span data-ttu-id="aadfe-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="aadfe-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aadfe-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadfe-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aadfe-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadfe-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aadfe-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadfe-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aadfe-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="aadfe-109">DESCRIPTION</span></span>
<span data-ttu-id="aadfe-110">Polecenie **cmdlet Get-AzPolicyAssignment** pobiera wszystkie lub konkretne przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="aadfe-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="aadfe-111">Zidentyfikuj przypisanie zasad do uzyskania według nazwy i zakresu lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="aadfe-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="aadfe-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aadfe-112">EXAMPLES</span></span>

### <span data-ttu-id="aadfe-113">Przykład 1. Uzyskiwanie wszystkich przypisań zasad</span><span class="sxs-lookup"><span data-stu-id="aadfe-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="aadfe-114">To polecenie pobiera wszystkie przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="aadfe-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="aadfe-115">Przykład 2. Uzyskiwanie konkretnego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="aadfe-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="aadfe-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje je w zmiennej $ResourceGroup zasobów.</span><span class="sxs-lookup"><span data-stu-id="aadfe-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="aadfe-117">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **IdentyfikatorZasób** $ResourceGroup zasad.</span><span class="sxs-lookup"><span data-stu-id="aadfe-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="aadfe-118">Przykład 3. Uzyskiwanie wszystkich przypisań zasad do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="aadfe-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="aadfe-119">Pierwsze polecenie określa identyfikator grupy zarządzania, do których ma być zwracane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="aadfe-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="aadfe-120">Drugie polecenie pobiera wszystkie przypisania zasad przypisane do grupy zarządzania z identyfikatorem "myManagementGroup".</span><span class="sxs-lookup"><span data-stu-id="aadfe-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="aadfe-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aadfe-121">PARAMETERS</span></span>

### <span data-ttu-id="aadfe-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aadfe-122">-ApiVersion</span></span>
<span data-ttu-id="aadfe-123">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="aadfe-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aadfe-124">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="aadfe-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aadfe-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadfe-125">-DefaultProfile</span></span>
<span data-ttu-id="aadfe-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="aadfe-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aadfe-127">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="aadfe-127">-Id</span></span>
<span data-ttu-id="aadfe-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadfe-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aadfe-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="aadfe-129">-IncludeDescendent</span></span>
<span data-ttu-id="aadfe-130">Powoduje, że lista zwróconych przypisań zasad zawiera wszystkie przydziały związane z danym zakresem, w tym te z zakresów nadrzędnych i te z zakresów malejąco.</span><span class="sxs-lookup"><span data-stu-id="aadfe-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="aadfe-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aadfe-131">-Name</span></span>
<span data-ttu-id="aadfe-132">Określa nazwę przydziału zasad, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadfe-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aadfe-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="aadfe-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="aadfe-134">Określa identyfikator definicji zasad przypisań zasad, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadfe-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aadfe-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="aadfe-135">-Pre</span></span>
<span data-ttu-id="aadfe-136">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="aadfe-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aadfe-137">— Zakres</span><span class="sxs-lookup"><span data-stu-id="aadfe-137">-Scope</span></span>
<span data-ttu-id="aadfe-138">Określa zakres, w jakim zasady są stosowane do przydziału, do którego otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadfe-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aadfe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadfe-139">CommonParameters</span></span>
<span data-ttu-id="aadfe-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadfe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadfe-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aadfe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadfe-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aadfe-142">INPUTS</span></span>

### <span data-ttu-id="aadfe-143">System.String</span><span class="sxs-lookup"><span data-stu-id="aadfe-143">System.String</span></span>

### <span data-ttu-id="aadfe-144">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="aadfe-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aadfe-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aadfe-145">OUTPUTS</span></span>

### <span data-ttu-id="aadfe-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="aadfe-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aadfe-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aadfe-147">NOTES</span></span>

## <span data-ttu-id="aadfe-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aadfe-148">RELATED LINKS</span></span>

[<span data-ttu-id="aadfe-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="aadfe-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="aadfe-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="aadfe-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="aadfe-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="aadfe-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


