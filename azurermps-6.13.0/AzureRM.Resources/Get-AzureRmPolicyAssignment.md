---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 71f3c6ab80fd0ba44d715cb25b4bf690e44359c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541516"
---
# <span data-ttu-id="6d2f8-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6d2f8-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6d2f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2f8-103">Pobiera przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d2f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d2f8-104">SYNTAX</span></span>

### <span data-ttu-id="6d2f8-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d2f8-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d2f8-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d2f8-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d2f8-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d2f8-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d2f8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d2f8-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d2f8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6d2f8-109">DESCRIPTION</span></span>
<span data-ttu-id="6d2f8-110">Polecenie cmdlet **Get-AzureRmPolicyAssignment** pobiera wszystkie przydziały zasad lub określone zadania.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="6d2f8-111">Zidentyfikuj przypisanie zasad, aby uzyskać według nazwy i zakresu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="6d2f8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d2f8-112">EXAMPLES</span></span>

### <span data-ttu-id="6d2f8-113">Przykład 1. pobieranie wszystkich przydziałów zasad</span><span class="sxs-lookup"><span data-stu-id="6d2f8-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="6d2f8-114">To polecenie uzyskuje wszystkie zadania dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="6d2f8-115">Przykład 2: uzyskiwanie określonego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="6d2f8-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="6d2f8-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzureRMResourceGroup cmdletand zapisuje ją w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6d2f8-117">Drugie polecenie pobiera przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="6d2f8-118">Przykład 3: uzyskiwanie wszystkich przypisań zasad przydzielonych do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6d2f8-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="6d2f8-119">Pierwsze polecenie określa identyfikator grupy zarządzania do zbadania.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="6d2f8-120">Drugie polecenie pobiera wszystkie przydziały zasad, które są przypisane do grupy zarządzania o IDENTYFIKATORze "Moja zarządca".</span><span class="sxs-lookup"><span data-stu-id="6d2f8-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="6d2f8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d2f8-121">PARAMETERS</span></span>

### <span data-ttu-id="6d2f8-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d2f8-122">-ApiVersion</span></span>
<span data-ttu-id="6d2f8-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d2f8-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6d2f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2f8-125">-DefaultProfile</span></span>
<span data-ttu-id="6d2f8-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d2f8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d2f8-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6d2f8-127">-Id</span></span>
<span data-ttu-id="6d2f8-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d2f8-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="6d2f8-129">-IncludeDescendent</span></span>
<span data-ttu-id="6d2f8-130">Powoduje, że lista zwracanych przypisań zasad obejmuje wszystkie zadania powiązane z danym zakresem, w tym te z zakresów nadrzędnych i te pochodzące od zakresów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="6d2f8-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6d2f8-131">-InformationAction</span></span>
<span data-ttu-id="6d2f8-132">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="6d2f8-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6d2f8-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6d2f8-134">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6d2f8-134">Continue</span></span>
- <span data-ttu-id="6d2f8-135">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6d2f8-135">Ignore</span></span>
- <span data-ttu-id="6d2f8-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="6d2f8-136">Inquire</span></span>
- <span data-ttu-id="6d2f8-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d2f8-137">SilentlyContinue</span></span>
- <span data-ttu-id="6d2f8-138">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6d2f8-138">Stop</span></span>
- <span data-ttu-id="6d2f8-139">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6d2f8-139">Suspend</span></span>

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

### <span data-ttu-id="6d2f8-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d2f8-140">-InformationVariable</span></span>
<span data-ttu-id="6d2f8-141">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6d2f8-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d2f8-142">-Name</span></span>
<span data-ttu-id="6d2f8-143">Określa nazwę przypisania zasad, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d2f8-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6d2f8-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="6d2f8-145">Określa identyfikator definicji zasad dla przypisań zasad, które jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d2f8-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="6d2f8-146">-Pre</span></span>
<span data-ttu-id="6d2f8-147">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6d2f8-148">-Zakres</span><span class="sxs-lookup"><span data-stu-id="6d2f8-148">-Scope</span></span>
<span data-ttu-id="6d2f8-149">Określa zakres, w którym zasady są stosowane do przydziału, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d2f8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2f8-150">CommonParameters</span></span>
<span data-ttu-id="6d2f8-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2f8-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2f8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2f8-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d2f8-153">INPUTS</span></span>

## <span data-ttu-id="6d2f8-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d2f8-154">OUTPUTS</span></span>

## <span data-ttu-id="6d2f8-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d2f8-155">NOTES</span></span>

## <span data-ttu-id="6d2f8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d2f8-156">RELATED LINKS</span></span>

[<span data-ttu-id="6d2f8-157">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6d2f8-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6d2f8-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6d2f8-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6d2f8-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6d2f8-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


