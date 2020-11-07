---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718022"
---
# <span data-ttu-id="ada0d-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ada0d-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="ada0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ada0d-102">SYNOPSIS</span></span>
<span data-ttu-id="ada0d-103">Pobiera przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="ada0d-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ada0d-104">SYNTAX</span></span>

### <span data-ttu-id="ada0d-105">GetAllPolicyAssignments (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ada0d-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ada0d-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ada0d-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ada0d-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="ada0d-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ada0d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ada0d-108">DESCRIPTION</span></span>
<span data-ttu-id="ada0d-109">Polecenie cmdlet **Get-AzureRmPolicyAssignment** pobiera wszystkie przydziały zasad lub określone zadania.</span><span class="sxs-lookup"><span data-stu-id="ada0d-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="ada0d-110">Zidentyfikuj przypisanie zasad, aby uzyskać według nazwy i zakresu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="ada0d-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="ada0d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ada0d-111">EXAMPLES</span></span>

### <span data-ttu-id="ada0d-112">Przykład 1. pobieranie wszystkich przydziałów zasad</span><span class="sxs-lookup"><span data-stu-id="ada0d-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="ada0d-113">To polecenie uzyskuje wszystkie zadania dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="ada0d-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="ada0d-114">Przykład 2: uzyskiwanie określonego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="ada0d-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="ada0d-115">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ada0d-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ada0d-116">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ada0d-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ada0d-117">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ada0d-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="ada0d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ada0d-118">PARAMETERS</span></span>

### <span data-ttu-id="ada0d-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ada0d-119">-ApiVersion</span></span>
<span data-ttu-id="ada0d-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ada0d-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ada0d-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="ada0d-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada0d-122">-DefaultProfile</span></span>
<span data-ttu-id="ada0d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ada0d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ada0d-124">-Id</span></span>
<span data-ttu-id="ada0d-125">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada0d-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ada0d-126">-InformationAction</span></span>
<span data-ttu-id="ada0d-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ada0d-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ada0d-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ada0d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ada0d-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ada0d-129">Continue</span></span>
- <span data-ttu-id="ada0d-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ada0d-130">Ignore</span></span>
- <span data-ttu-id="ada0d-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="ada0d-131">Inquire</span></span>
- <span data-ttu-id="ada0d-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ada0d-132">SilentlyContinue</span></span>
- <span data-ttu-id="ada0d-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ada0d-133">Stop</span></span>
- <span data-ttu-id="ada0d-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ada0d-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ada0d-135">-InformationVariable</span></span>
<span data-ttu-id="ada0d-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ada0d-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ada0d-137">-Name</span></span>
<span data-ttu-id="ada0d-138">Określa nazwę przypisania zasad, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada0d-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ada0d-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="ada0d-140">Określa identyfikator definicji zasad dla przypisań zasad, które jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada0d-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="ada0d-141">-Pre</span></span>
<span data-ttu-id="ada0d-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ada0d-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ada0d-143">-Scope</span></span>
<span data-ttu-id="ada0d-144">Określa zakres, w którym zasady są stosowane do przydziału, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada0d-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada0d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada0d-145">CommonParameters</span></span>
<span data-ttu-id="ada0d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada0d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada0d-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada0d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada0d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada0d-148">INPUTS</span></span>

### <span data-ttu-id="ada0d-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ada0d-149">None</span></span>
<span data-ttu-id="ada0d-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ada0d-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ada0d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ada0d-151">OUTPUTS</span></span>

### <span data-ttu-id="ada0d-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ada0d-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ada0d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ada0d-153">NOTES</span></span>

## <span data-ttu-id="ada0d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada0d-154">RELATED LINKS</span></span>

[<span data-ttu-id="ada0d-155">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ada0d-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ada0d-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ada0d-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ada0d-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ada0d-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


