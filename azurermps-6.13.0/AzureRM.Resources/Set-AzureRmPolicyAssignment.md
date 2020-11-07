---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0fd276b8af8c16fdeb4d412029ac884ae3e5e183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718773"
---
# <span data-ttu-id="b958d-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b958d-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b958d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b958d-102">SYNOPSIS</span></span>
<span data-ttu-id="b958d-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="b958d-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b958d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b958d-104">SYNTAX</span></span>

### <span data-ttu-id="b958d-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b958d-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b958d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b958d-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b958d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b958d-107">DESCRIPTION</span></span>
<span data-ttu-id="b958d-108">Polecenie cmdlet **Set-AzureRmPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="b958d-109">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="b958d-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="b958d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b958d-110">EXAMPLES</span></span>

### <span data-ttu-id="b958d-111">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="b958d-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="b958d-112">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b958d-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b958d-113">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b958d-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b958d-114">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b958d-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b958d-115">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b958d-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b958d-116">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b958d-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b958d-117">Przykład 2: Dodawanie zarządzanej tożsamości do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="b958d-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="b958d-118">Pierwsze polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji przy użyciu polecenia cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b958d-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b958d-119">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b958d-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b958d-120">Polecenie ostatnie przypisuje zarządzaną tożsamość do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="b958d-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b958d-121">PARAMETERS</span></span>

### <span data-ttu-id="b958d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b958d-122">-ApiVersion</span></span>
<span data-ttu-id="b958d-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b958d-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b958d-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="b958d-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b958d-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b958d-125">-AssignIdentity</span></span>
<span data-ttu-id="b958d-126">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b958d-127">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="b958d-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b958d-128">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b958d-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b958d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b958d-129">-DefaultProfile</span></span>
<span data-ttu-id="b958d-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b958d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b958d-131">— Opis</span><span class="sxs-lookup"><span data-stu-id="b958d-131">-Description</span></span>
<span data-ttu-id="b958d-132">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="b958d-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="b958d-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b958d-133">-DisplayName</span></span>
<span data-ttu-id="b958d-134">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b958d-135">-ID</span><span class="sxs-lookup"><span data-stu-id="b958d-135">-Id</span></span>
<span data-ttu-id="b958d-136">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="b958d-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b958d-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b958d-137">-InformationAction</span></span>
<span data-ttu-id="b958d-138">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b958d-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b958d-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b958d-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b958d-140">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b958d-140">Continue</span></span>
- <span data-ttu-id="b958d-141">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b958d-141">Ignore</span></span>
- <span data-ttu-id="b958d-142">Inquire</span><span class="sxs-lookup"><span data-stu-id="b958d-142">Inquire</span></span>
- <span data-ttu-id="b958d-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b958d-143">SilentlyContinue</span></span>
- <span data-ttu-id="b958d-144">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b958d-144">Stop</span></span>
- <span data-ttu-id="b958d-145">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b958d-145">Suspend</span></span>

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

### <span data-ttu-id="b958d-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b958d-146">-InformationVariable</span></span>
<span data-ttu-id="b958d-147">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b958d-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b958d-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b958d-148">-Location</span></span>
<span data-ttu-id="b958d-149">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b958d-150">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="b958d-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="b958d-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b958d-151">-Metadata</span></span>
<span data-ttu-id="b958d-152">Zaktualizowane metadane przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b958d-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="b958d-153">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="b958d-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="b958d-154">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b958d-154">-Name</span></span>
<span data-ttu-id="b958d-155">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b958d-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b958d-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b958d-156">-NotScope</span></span>
<span data-ttu-id="b958d-157">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="b958d-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="b958d-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="b958d-158">-Pre</span></span>
<span data-ttu-id="b958d-159">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b958d-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b958d-160">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b958d-160">-Scope</span></span>
<span data-ttu-id="b958d-161">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="b958d-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b958d-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="b958d-162">-Sku</span></span>
<span data-ttu-id="b958d-163">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="b958d-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="b958d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b958d-164">CommonParameters</span></span>
<span data-ttu-id="b958d-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b958d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b958d-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b958d-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b958d-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b958d-167">INPUTS</span></span>

## <span data-ttu-id="b958d-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b958d-168">OUTPUTS</span></span>

## <span data-ttu-id="b958d-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b958d-169">NOTES</span></span>

## <span data-ttu-id="b958d-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b958d-170">RELATED LINKS</span></span>

[<span data-ttu-id="b958d-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b958d-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b958d-172">Nowe — AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b958d-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b958d-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b958d-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


