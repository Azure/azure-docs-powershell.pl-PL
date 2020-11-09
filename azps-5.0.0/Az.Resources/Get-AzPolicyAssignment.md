---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308910"
---
# <span data-ttu-id="0c62f-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c62f-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="0c62f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c62f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c62f-103">Pobiera przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="0c62f-103">Gets policy assignments.</span></span>

## <span data-ttu-id="0c62f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c62f-104">SYNTAX</span></span>

### <span data-ttu-id="0c62f-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c62f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c62f-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c62f-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c62f-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c62f-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c62f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c62f-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c62f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0c62f-109">DESCRIPTION</span></span>
<span data-ttu-id="0c62f-110">Polecenie cmdlet **Get-AzPolicyAssignment** pobiera wszystkie przydziały zasad lub określone zadania.</span><span class="sxs-lookup"><span data-stu-id="0c62f-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="0c62f-111">Zidentyfikuj przypisanie zasad, aby uzyskać według nazwy i zakresu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="0c62f-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="0c62f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c62f-112">EXAMPLES</span></span>

### <span data-ttu-id="0c62f-113">Przykład 1. pobieranie wszystkich przydziałów zasad</span><span class="sxs-lookup"><span data-stu-id="0c62f-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="0c62f-114">To polecenie uzyskuje wszystkie zadania dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="0c62f-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="0c62f-115">Przykład 2: uzyskiwanie określonego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="0c62f-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="0c62f-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup i zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0c62f-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0c62f-117">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0c62f-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="0c62f-118">Przykład 3: uzyskiwanie wszystkich przypisań zasad przydzielonych do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="0c62f-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="0c62f-119">Pierwsze polecenie określa identyfikator grupy zarządzania do zbadania.</span><span class="sxs-lookup"><span data-stu-id="0c62f-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="0c62f-120">Drugie polecenie pobiera wszystkie przydziały zasad, które są przypisane do grupy zarządzania o IDENTYFIKATORze "Moja zarządca".</span><span class="sxs-lookup"><span data-stu-id="0c62f-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="0c62f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c62f-121">PARAMETERS</span></span>

### <span data-ttu-id="0c62f-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0c62f-122">-ApiVersion</span></span>
<span data-ttu-id="0c62f-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0c62f-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0c62f-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="0c62f-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0c62f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c62f-125">-DefaultProfile</span></span>
<span data-ttu-id="0c62f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0c62f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c62f-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0c62f-127">-Id</span></span>
<span data-ttu-id="0c62f-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c62f-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c62f-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="0c62f-129">-IncludeDescendent</span></span>
<span data-ttu-id="0c62f-130">Powoduje, że lista zwracanych przypisań zasad obejmuje wszystkie zadania powiązane z danym zakresem, w tym te z zakresów nadrzędnych i te pochodzące od zakresów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="0c62f-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="0c62f-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c62f-131">-Name</span></span>
<span data-ttu-id="0c62f-132">Określa nazwę przypisania zasad, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c62f-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c62f-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0c62f-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="0c62f-134">Określa identyfikator definicji zasad dla przypisań zasad, które jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c62f-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c62f-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="0c62f-135">-Pre</span></span>
<span data-ttu-id="0c62f-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="0c62f-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0c62f-137">-Zakres</span><span class="sxs-lookup"><span data-stu-id="0c62f-137">-Scope</span></span>
<span data-ttu-id="0c62f-138">Określa zakres, w którym zasady są stosowane do przydziału, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c62f-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c62f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c62f-139">CommonParameters</span></span>
<span data-ttu-id="0c62f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c62f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c62f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c62f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c62f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c62f-142">INPUTS</span></span>

### <span data-ttu-id="0c62f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0c62f-143">System.String</span></span>

### <span data-ttu-id="0c62f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c62f-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c62f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c62f-145">OUTPUTS</span></span>

### <span data-ttu-id="0c62f-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0c62f-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0c62f-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c62f-147">NOTES</span></span>

## <span data-ttu-id="0c62f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c62f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0c62f-149">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c62f-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="0c62f-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c62f-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="0c62f-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c62f-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


