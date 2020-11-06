---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551612"
---
# <span data-ttu-id="7e41b-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7e41b-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="7e41b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e41b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e41b-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="7e41b-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e41b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e41b-104">SYNTAX</span></span>

### <span data-ttu-id="7e41b-105">SetByPolicyAssignmentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e41b-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e41b-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="7e41b-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7e41b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e41b-107">DESCRIPTION</span></span>
<span data-ttu-id="7e41b-108">Polecenie cmdlet **Set-AzureRmPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="7e41b-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="7e41b-109">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="7e41b-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="7e41b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e41b-110">EXAMPLES</span></span>

### <span data-ttu-id="7e41b-111">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="7e41b-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="7e41b-112">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e41b-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="7e41b-113">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e41b-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="7e41b-114">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="7e41b-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="7e41b-115">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="7e41b-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="7e41b-116">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad określonym przez właściwość **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="7e41b-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="7e41b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e41b-117">PARAMETERS</span></span>

### <span data-ttu-id="7e41b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e41b-118">-ApiVersion</span></span>
<span data-ttu-id="7e41b-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7e41b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7e41b-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="7e41b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7e41b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e41b-121">-DefaultProfile</span></span>
<span data-ttu-id="7e41b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e41b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e41b-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="7e41b-123">-Description</span></span>
<span data-ttu-id="7e41b-124">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="7e41b-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e41b-125">-DisplayName</span></span>
<span data-ttu-id="7e41b-126">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="7e41b-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-127">-ID</span><span class="sxs-lookup"><span data-stu-id="7e41b-127">-Id</span></span>
<span data-ttu-id="7e41b-128">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="7e41b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7e41b-129">-InformationAction</span></span>
<span data-ttu-id="7e41b-130">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7e41b-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e41b-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7e41b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e41b-132">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7e41b-132">Continue</span></span>
- <span data-ttu-id="7e41b-133">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7e41b-133">Ignore</span></span>
- <span data-ttu-id="7e41b-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="7e41b-134">Inquire</span></span>
- <span data-ttu-id="7e41b-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7e41b-135">SilentlyContinue</span></span>
- <span data-ttu-id="7e41b-136">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7e41b-136">Stop</span></span>
- <span data-ttu-id="7e41b-137">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7e41b-137">Suspend</span></span>

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

### <span data-ttu-id="7e41b-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7e41b-138">-InformationVariable</span></span>
<span data-ttu-id="7e41b-139">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7e41b-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e41b-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e41b-140">-Name</span></span>
<span data-ttu-id="7e41b-141">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e41b-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="7e41b-142">-NotScope</span></span>
<span data-ttu-id="7e41b-143">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="7e41b-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="7e41b-144">-Pre</span></span>
<span data-ttu-id="7e41b-145">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="7e41b-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7e41b-146">-Zakres</span><span class="sxs-lookup"><span data-stu-id="7e41b-146">-Scope</span></span>
<span data-ttu-id="7e41b-147">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="7e41b-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="7e41b-148">-Sku</span></span>
<span data-ttu-id="7e41b-149">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="7e41b-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e41b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e41b-150">CommonParameters</span></span>
<span data-ttu-id="7e41b-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e41b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e41b-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e41b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e41b-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e41b-153">INPUTS</span></span>

### <span data-ttu-id="7e41b-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e41b-154">None</span></span>
<span data-ttu-id="7e41b-155">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7e41b-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e41b-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e41b-156">OUTPUTS</span></span>

### <span data-ttu-id="7e41b-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7e41b-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7e41b-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e41b-158">NOTES</span></span>

## <span data-ttu-id="7e41b-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e41b-159">RELATED LINKS</span></span>

[<span data-ttu-id="7e41b-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7e41b-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="7e41b-161">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7e41b-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="7e41b-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7e41b-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


