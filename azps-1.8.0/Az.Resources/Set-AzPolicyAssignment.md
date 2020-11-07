---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708282"
---
# <span data-ttu-id="2285c-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2285c-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="2285c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2285c-102">SYNOPSIS</span></span>
<span data-ttu-id="2285c-103">Modyfikuje przypisanie zasady.</span><span class="sxs-lookup"><span data-stu-id="2285c-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="2285c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2285c-104">SYNTAX</span></span>

### <span data-ttu-id="2285c-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2285c-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2285c-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2285c-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2285c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2285c-107">DESCRIPTION</span></span>
<span data-ttu-id="2285c-108">Polecenie cmdlet **Set-AzPolicyAssignment** modyfikuje przypisanie zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2285c-109">Określ przydział według identyfikatora lub według jego nazwy i zakresu.</span><span class="sxs-lookup"><span data-stu-id="2285c-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2285c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2285c-110">EXAMPLES</span></span>

### <span data-ttu-id="2285c-111">Przykład 1: aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="2285c-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="2285c-112">Pierwsze polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2285c-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2285c-113">Polecenie zapisuje ten obiekt w zmiennej $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2285c-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2285c-114">Drugie polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2285c-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2285c-115">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2285c-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2285c-116">Ostatnie polecenie aktualizuje nazwę wyświetlaną w przypisaniu zasad w grupie zasobów identyfikowanej przez właściwość **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2285c-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="2285c-117">Przykład 2: Dodawanie zarządzanej tożsamości do przypisania zasad</span><span class="sxs-lookup"><span data-stu-id="2285c-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="2285c-118">Pierwsze polecenie uzyskuje przypisanie zasad o nazwie PolicyAssignment z bieżącej subskrypcji przy użyciu polecenia cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2285c-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2285c-119">Polecenie zapisuje ten obiekt w zmiennej $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2285c-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2285c-120">Polecenie ostatnie przypisuje zarządzaną tożsamość do przypisania zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="2285c-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2285c-121">PARAMETERS</span></span>

### <span data-ttu-id="2285c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2285c-122">-ApiVersion</span></span>
<span data-ttu-id="2285c-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="2285c-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2285c-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="2285c-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2285c-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2285c-125">-AssignIdentity</span></span>
<span data-ttu-id="2285c-126">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zadania zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="2285c-127">Tożsamość będzie używana podczas wykonywania wdrożeń zasad "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="2285c-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="2285c-128">Lokalizacja jest wymagana podczas przypisywania tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2285c-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="2285c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2285c-129">-DefaultProfile</span></span>
<span data-ttu-id="2285c-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2285c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2285c-131">— Opis</span><span class="sxs-lookup"><span data-stu-id="2285c-131">-Description</span></span>
<span data-ttu-id="2285c-132">Opis przydziału zasad</span><span class="sxs-lookup"><span data-stu-id="2285c-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="2285c-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2285c-133">-DisplayName</span></span>
<span data-ttu-id="2285c-134">Określa nową nazwę wyświetlaną dla przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="2285c-135">-ID</span><span class="sxs-lookup"><span data-stu-id="2285c-135">-Id</span></span>
<span data-ttu-id="2285c-136">Określa w pełni kwalifikowany identyfikator zasobu dla przydziału zasad, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="2285c-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2285c-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2285c-137">-Location</span></span>
<span data-ttu-id="2285c-138">Lokalizacja tożsamości zasobu przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="2285c-139">Jest to wymagane, gdy jest stosowany przełącznik-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="2285c-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="2285c-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2285c-140">-Metadata</span></span>
<span data-ttu-id="2285c-141">Zaktualizowane metadane przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="2285c-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="2285c-142">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="2285c-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="2285c-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2285c-143">-Name</span></span>
<span data-ttu-id="2285c-144">Określa nazwę przypisania zasad, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2285c-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2285c-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2285c-145">-NotScope</span></span>
<span data-ttu-id="2285c-146">Przypisanie zasad nie zawiera zakresów.</span><span class="sxs-lookup"><span data-stu-id="2285c-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="2285c-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="2285c-147">-Pre</span></span>
<span data-ttu-id="2285c-148">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="2285c-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2285c-149">-Zakres</span><span class="sxs-lookup"><span data-stu-id="2285c-149">-Scope</span></span>
<span data-ttu-id="2285c-150">Określa zakres, w którym zasady są stosowane.</span><span class="sxs-lookup"><span data-stu-id="2285c-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="2285c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2285c-151">CommonParameters</span></span>
<span data-ttu-id="2285c-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2285c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2285c-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2285c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2285c-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2285c-154">INPUTS</span></span>

### <span data-ttu-id="2285c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2285c-155">System.String</span></span>

### <span data-ttu-id="2285c-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="2285c-156">System.String[]</span></span>

## <span data-ttu-id="2285c-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2285c-157">OUTPUTS</span></span>

### <span data-ttu-id="2285c-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2285c-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2285c-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2285c-159">NOTES</span></span>

## <span data-ttu-id="2285c-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2285c-160">RELATED LINKS</span></span>

[<span data-ttu-id="2285c-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2285c-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2285c-162">Nowe — AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2285c-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2285c-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2285c-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


