---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542996"
---
# <span data-ttu-id="c8ed8-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8ed8-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="c8ed8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ed8-103">Pobiera przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8ed8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8ed8-104">SYNTAX</span></span>

### <span data-ttu-id="c8ed8-105">Zestaw parametrów lista wszystkich przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="c8ed8-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="c8ed8-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8ed8-107">Zestaw parametrów nazwa przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8ed8-108">Ustawiony parametr identyfikatora przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8ed8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c8ed8-109">DESCRIPTION</span></span>
<span data-ttu-id="c8ed8-110">Polecenie cmdlet **Get-AzureRmPolicyAssignment** pobiera wszystkie przydziały zasad lub określone zadania.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="c8ed8-111">Zidentyfikuj przypisanie zasad, aby uzyskać według nazwy i zakresu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="c8ed8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8ed8-112">EXAMPLES</span></span>

### <span data-ttu-id="c8ed8-113">Przykład 1. pobieranie wszystkich przydziałów zasad</span><span class="sxs-lookup"><span data-stu-id="c8ed8-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="c8ed8-114">To polecenie uzyskuje wszystkie zadania dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="c8ed8-115">Przykład 2: uzyskiwanie określonego przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="c8ed8-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c8ed8-116">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c8ed8-117">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c8ed8-118">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment07 dla zakresu, który identyfikuje właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="c8ed8-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8ed8-119">PARAMETERS</span></span>

### <span data-ttu-id="c8ed8-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8ed8-120">-ApiVersion</span></span>
<span data-ttu-id="c8ed8-121">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8ed8-122">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c8ed8-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c8ed8-123">-Id</span></span>
<span data-ttu-id="c8ed8-124">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8ed8-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8ed8-125">-InformationAction</span></span>
<span data-ttu-id="c8ed8-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8ed8-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c8ed8-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8ed8-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c8ed8-128">Continue</span></span>
- <span data-ttu-id="c8ed8-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c8ed8-129">Ignore</span></span>
- <span data-ttu-id="c8ed8-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="c8ed8-130">Inquire</span></span>
- <span data-ttu-id="c8ed8-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8ed8-131">SilentlyContinue</span></span>
- <span data-ttu-id="c8ed8-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c8ed8-132">Stop</span></span>
- <span data-ttu-id="c8ed8-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c8ed8-133">Suspend</span></span>

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

### <span data-ttu-id="c8ed8-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8ed8-134">-InformationVariable</span></span>
<span data-ttu-id="c8ed8-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8ed8-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8ed8-136">-Name</span></span>
<span data-ttu-id="c8ed8-137">Określa nazwę przypisania zasad, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8ed8-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c8ed8-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="c8ed8-139">Określa identyfikator definicji zasad dla przypisań zasad, które jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8ed8-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8ed8-140">-Pre</span></span>
<span data-ttu-id="c8ed8-141">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8ed8-142">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c8ed8-142">-Scope</span></span>
<span data-ttu-id="c8ed8-143">Określa zakres, w którym zasady są stosowane do przydziału, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8ed8-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ed8-144">-DefaultProfile</span></span>
<span data-ttu-id="c8ed8-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8ed8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ed8-146">CommonParameters</span></span>
<span data-ttu-id="c8ed8-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ed8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ed8-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8ed8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ed8-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8ed8-149">INPUTS</span></span>

## <span data-ttu-id="c8ed8-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8ed8-150">OUTPUTS</span></span>

### <span data-ttu-id="c8ed8-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c8ed8-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c8ed8-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8ed8-152">NOTES</span></span>

## <span data-ttu-id="c8ed8-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8ed8-153">RELATED LINKS</span></span>

[<span data-ttu-id="c8ed8-154">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8ed8-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c8ed8-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8ed8-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c8ed8-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8ed8-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


