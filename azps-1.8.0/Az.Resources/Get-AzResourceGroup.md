---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708392"
---
# <span data-ttu-id="99532-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99532-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="99532-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99532-102">SYNOPSIS</span></span>
<span data-ttu-id="99532-103">Pobiera grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99532-103">Gets resource groups.</span></span>

## <span data-ttu-id="99532-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99532-104">SYNTAX</span></span>

### <span data-ttu-id="99532-105">GetByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99532-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99532-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="99532-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99532-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99532-107">DESCRIPTION</span></span>
<span data-ttu-id="99532-108">Polecenie cmdlet **Get-AzResourceGroup** umożliwia pobieranie grup zasobów platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99532-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="99532-109">Możesz uzyskać dostęp do wszystkich grup zasobów lub określić grupę zasobów według nazwy lub według innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="99532-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="99532-110">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich grup zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99532-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="99532-111">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="99532-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="99532-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99532-112">EXAMPLES</span></span>

### <span data-ttu-id="99532-113">Przykład 1: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="99532-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="99532-114">To polecenie pobiera grupę zasobów platformy Azure w ramach abonamentu o nazwie EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="99532-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="99532-115">Przykład 2: pobieranie wszystkich tagów grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="99532-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="99532-116">To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla znaczniki skojarzone z tą grupą.</span><span class="sxs-lookup"><span data-stu-id="99532-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="99532-117">Przykład 3: wyświetlanie grup zasobów według lokalizacji</span><span class="sxs-lookup"><span data-stu-id="99532-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="99532-118">Przykład 4: wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="99532-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="99532-119">Przykład 5: wyświetlanie grup zasobów, których nazwy zaczynają się od serwera WebServer</span><span class="sxs-lookup"><span data-stu-id="99532-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="99532-120">Przykład 6: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="99532-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="99532-121">To polecenie pobiera grupę zasobów platformy Azure w ramach subskrypcji, która rozpoczyna się od "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="99532-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="99532-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99532-122">PARAMETERS</span></span>

### <span data-ttu-id="99532-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99532-123">-ApiVersion</span></span>
<span data-ttu-id="99532-124">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="99532-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="99532-125">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="99532-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="99532-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99532-126">-DefaultProfile</span></span>
<span data-ttu-id="99532-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="99532-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99532-128">-ID</span><span class="sxs-lookup"><span data-stu-id="99532-128">-Id</span></span>
<span data-ttu-id="99532-129">Określa identyfikator grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="99532-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="99532-130">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="99532-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="99532-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99532-131">-Location</span></span>
<span data-ttu-id="99532-132">Określa lokalizację grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="99532-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="99532-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99532-133">-Name</span></span>
<span data-ttu-id="99532-134">Określa nazwę grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="99532-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="99532-135">Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="99532-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="99532-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="99532-136">-Pre</span></span>
<span data-ttu-id="99532-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="99532-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="99532-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="99532-138">-Tag</span></span>
<span data-ttu-id="99532-139">Tag Hashtable w celu filtrowania grup zasobów według.</span><span class="sxs-lookup"><span data-stu-id="99532-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="99532-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99532-140">CommonParameters</span></span>
<span data-ttu-id="99532-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99532-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99532-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99532-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99532-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99532-143">INPUTS</span></span>

### <span data-ttu-id="99532-144">System. String</span><span class="sxs-lookup"><span data-stu-id="99532-144">System.String</span></span>

### <span data-ttu-id="99532-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99532-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="99532-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99532-146">OUTPUTS</span></span>

### <span data-ttu-id="99532-147">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99532-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="99532-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99532-148">NOTES</span></span>

## <span data-ttu-id="99532-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99532-149">RELATED LINKS</span></span>

[<span data-ttu-id="99532-150">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99532-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="99532-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99532-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="99532-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99532-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


