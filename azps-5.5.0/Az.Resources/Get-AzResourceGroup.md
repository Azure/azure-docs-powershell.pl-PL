---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186467"
---
# <span data-ttu-id="5acca-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5acca-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="5acca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5acca-102">SYNOPSIS</span></span>
<span data-ttu-id="5acca-103">Pobiera grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5acca-103">Gets resource groups.</span></span>

## <span data-ttu-id="5acca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5acca-104">SYNTAX</span></span>

### <span data-ttu-id="5acca-105">GetByResourceGroupName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="5acca-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5acca-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5acca-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5acca-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5acca-107">DESCRIPTION</span></span>
<span data-ttu-id="5acca-108">Polecenie **cmdlet Get-AzResourceGroup** pobiera grupy zasobów platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5acca-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="5acca-109">Możesz pobrać wszystkie grupy zasobów lub określić grupę zasobów według nazwy lub innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="5acca-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="5acca-110">Domyślnie to polecenie cmdlet pobiera wszystkie grupy zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5acca-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="5acca-111">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5acca-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5acca-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5acca-112">EXAMPLES</span></span>

### <span data-ttu-id="5acca-113">Przykład 1. Uzyskiwanie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="5acca-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="5acca-114">To polecenie pobiera grupę zasobów platformy Azure w ramach subskrypcji o nazwie EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="5acca-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="5acca-115">Przykład 2. Uzyskiwanie wszystkich tagów grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5acca-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5acca-116">To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla skojarzone z nią tagi.</span><span class="sxs-lookup"><span data-stu-id="5acca-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="5acca-117">Przykład 3. Uzyskiwanie grup zasobów na podstawie tagu</span><span class="sxs-lookup"><span data-stu-id="5acca-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="5acca-118">Przykład 4. Wyświetlanie grup zasobów według lokalizacji</span><span class="sxs-lookup"><span data-stu-id="5acca-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="5acca-119">Przykład 5. Wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="5acca-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="5acca-120">Przykład 6. Wyświetlanie grup zasobów, których nazwy zaczynają się od serwera sieci Web</span><span class="sxs-lookup"><span data-stu-id="5acca-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="5acca-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5acca-121">PARAMETERS</span></span>

### <span data-ttu-id="5acca-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5acca-122">-ApiVersion</span></span>
<span data-ttu-id="5acca-123">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="5acca-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5acca-124">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="5acca-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5acca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5acca-125">-DefaultProfile</span></span>
<span data-ttu-id="5acca-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5acca-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5acca-127">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="5acca-127">-Id</span></span>
<span data-ttu-id="5acca-128">Określa identyfikator grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="5acca-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="5acca-129">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="5acca-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acca-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5acca-130">-Location</span></span>
<span data-ttu-id="5acca-131">Określa lokalizację grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="5acca-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acca-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5acca-132">-Name</span></span>
<span data-ttu-id="5acca-133">Określa nazwę grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="5acca-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="5acca-134">Ten parametr obsługuje symbole wieloznaczne na początku i/lub na końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="5acca-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5acca-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="5acca-135">-Pre</span></span>
<span data-ttu-id="5acca-136">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="5acca-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5acca-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="5acca-137">-Tag</span></span>
<span data-ttu-id="5acca-138">Tabela skrótów tagów, według których można filtrować grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5acca-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5acca-139">CommonParameters</span></span>
<span data-ttu-id="5acca-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5acca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5acca-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5acca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5acca-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5acca-142">INPUTS</span></span>

### <span data-ttu-id="5acca-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5acca-143">System.String</span></span>

### <span data-ttu-id="5acca-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5acca-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5acca-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5acca-145">OUTPUTS</span></span>

### <span data-ttu-id="5acca-146">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5acca-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="5acca-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5acca-147">NOTES</span></span>

## <span data-ttu-id="5acca-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5acca-148">RELATED LINKS</span></span>

[<span data-ttu-id="5acca-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5acca-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="5acca-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5acca-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="5acca-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5acca-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

