---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542992"
---
# <span data-ttu-id="9404a-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9404a-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="9404a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9404a-102">SYNOPSIS</span></span>
<span data-ttu-id="9404a-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="9404a-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9404a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9404a-104">SYNTAX</span></span>

### <span data-ttu-id="9404a-105">Zestaw parametrów nazwa przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="9404a-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="9404a-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="9404a-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9404a-107">Ustawiony parametr identyfikatora przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="9404a-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9404a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9404a-108">DESCRIPTION</span></span>
<span data-ttu-id="9404a-109">Polecenie cmdlet **Set-AzureRmPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="9404a-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="9404a-110">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="9404a-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="9404a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9404a-111">EXAMPLES</span></span>

### <span data-ttu-id="9404a-112">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="9404a-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="9404a-113">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9404a-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="9404a-114">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9404a-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="9404a-115">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9404a-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="9404a-116">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9404a-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="9404a-117">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad określonym przez właściwość **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9404a-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="9404a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9404a-118">PARAMETERS</span></span>

### <span data-ttu-id="9404a-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9404a-119">-ApiVersion</span></span>
<span data-ttu-id="9404a-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="9404a-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9404a-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="9404a-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9404a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9404a-122">-DisplayName</span></span>
<span data-ttu-id="9404a-123">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="9404a-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="9404a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9404a-124">-Id</span></span>
<span data-ttu-id="9404a-125">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="9404a-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9404a-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9404a-126">-InformationAction</span></span>
<span data-ttu-id="9404a-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9404a-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9404a-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9404a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9404a-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9404a-129">Continue</span></span>
- <span data-ttu-id="9404a-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9404a-130">Ignore</span></span>
- <span data-ttu-id="9404a-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="9404a-131">Inquire</span></span>
- <span data-ttu-id="9404a-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9404a-132">SilentlyContinue</span></span>
- <span data-ttu-id="9404a-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9404a-133">Stop</span></span>
- <span data-ttu-id="9404a-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9404a-134">Suspend</span></span>

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

### <span data-ttu-id="9404a-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9404a-135">-InformationVariable</span></span>
<span data-ttu-id="9404a-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9404a-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9404a-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9404a-137">-Name</span></span>
<span data-ttu-id="9404a-138">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9404a-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9404a-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="9404a-139">-NotScope</span></span>
<span data-ttu-id="9404a-140">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="9404a-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9404a-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="9404a-141">-Pre</span></span>
<span data-ttu-id="9404a-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="9404a-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9404a-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="9404a-143">-Scope</span></span>
<span data-ttu-id="9404a-144">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="9404a-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="9404a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9404a-145">-DefaultProfile</span></span>
<span data-ttu-id="9404a-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9404a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9404a-147">— Opis</span><span class="sxs-lookup"><span data-stu-id="9404a-147">-Description</span></span>
<span data-ttu-id="9404a-148">Opis przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="9404a-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="9404a-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="9404a-149">-Sku</span></span>
<span data-ttu-id="9404a-150">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="9404a-150">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="9404a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9404a-151">CommonParameters</span></span>
<span data-ttu-id="9404a-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9404a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9404a-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9404a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9404a-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9404a-154">INPUTS</span></span>

## <span data-ttu-id="9404a-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9404a-155">OUTPUTS</span></span>

### <span data-ttu-id="9404a-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9404a-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9404a-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9404a-157">NOTES</span></span>

## <span data-ttu-id="9404a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9404a-158">RELATED LINKS</span></span>

[<span data-ttu-id="9404a-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9404a-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="9404a-160">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9404a-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="9404a-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9404a-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


