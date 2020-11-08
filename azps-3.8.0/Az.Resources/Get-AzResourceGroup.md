---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052882"
---
# <span data-ttu-id="be8e6-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be8e6-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="be8e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="be8e6-103">Pobiera grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be8e6-103">Gets resource groups.</span></span>

## <span data-ttu-id="be8e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be8e6-104">SYNTAX</span></span>

### <span data-ttu-id="be8e6-105">GetByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be8e6-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be8e6-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="be8e6-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be8e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="be8e6-107">DESCRIPTION</span></span>
<span data-ttu-id="be8e6-108">Polecenie cmdlet **Get-AzResourceGroup** umożliwia pobieranie grup zasobów platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be8e6-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="be8e6-109">Możesz uzyskać dostęp do wszystkich grup zasobów lub określić grupę zasobów według nazwy lub według innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="be8e6-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="be8e6-110">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich grup zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="be8e6-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="be8e6-111">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="be8e6-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="be8e6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be8e6-112">EXAMPLES</span></span>

### <span data-ttu-id="be8e6-113">Przykład 1: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="be8e6-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="be8e6-114">To polecenie pobiera grupę zasobów platformy Azure w ramach abonamentu o nazwie EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="be8e6-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="be8e6-115">Przykład 2: pobieranie wszystkich tagów grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="be8e6-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="be8e6-116">To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla znaczniki skojarzone z tą grupą.</span><span class="sxs-lookup"><span data-stu-id="be8e6-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="be8e6-117">Przykład 3: wyświetlanie grup zasobów według lokalizacji</span><span class="sxs-lookup"><span data-stu-id="be8e6-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="be8e6-118">Przykład 4: wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="be8e6-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="be8e6-119">Przykład 5: wyświetlanie grup zasobów, których nazwy zaczynają się od serwera WebServer</span><span class="sxs-lookup"><span data-stu-id="be8e6-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="be8e6-120">Przykład 6: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="be8e6-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="be8e6-121">To polecenie pobiera grupę zasobów platformy Azure w ramach subskrypcji, która rozpoczyna się od "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="be8e6-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="be8e6-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be8e6-122">PARAMETERS</span></span>

### <span data-ttu-id="be8e6-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be8e6-123">-ApiVersion</span></span>
<span data-ttu-id="be8e6-124">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="be8e6-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="be8e6-125">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="be8e6-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="be8e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8e6-126">-DefaultProfile</span></span>
<span data-ttu-id="be8e6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="be8e6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be8e6-128">-ID</span><span class="sxs-lookup"><span data-stu-id="be8e6-128">-Id</span></span>
<span data-ttu-id="be8e6-129">Określa identyfikator grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="be8e6-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="be8e6-130">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="be8e6-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="be8e6-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="be8e6-131">-Location</span></span>
<span data-ttu-id="be8e6-132">Określa lokalizację grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="be8e6-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="be8e6-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be8e6-133">-Name</span></span>
<span data-ttu-id="be8e6-134">Określa nazwę grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="be8e6-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="be8e6-135">Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="be8e6-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="be8e6-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="be8e6-136">-Pre</span></span>
<span data-ttu-id="be8e6-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="be8e6-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be8e6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="be8e6-138">-Tag</span></span>
<span data-ttu-id="be8e6-139">Tag Hashtable w celu filtrowania grup zasobów według.</span><span class="sxs-lookup"><span data-stu-id="be8e6-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="be8e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8e6-140">CommonParameters</span></span>
<span data-ttu-id="be8e6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be8e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8e6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be8e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8e6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be8e6-143">INPUTS</span></span>

### <span data-ttu-id="be8e6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="be8e6-144">System.String</span></span>

### <span data-ttu-id="be8e6-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be8e6-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="be8e6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be8e6-146">OUTPUTS</span></span>

### <span data-ttu-id="be8e6-147">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be8e6-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="be8e6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be8e6-148">NOTES</span></span>

## <span data-ttu-id="be8e6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be8e6-149">RELATED LINKS</span></span>

[<span data-ttu-id="be8e6-150">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be8e6-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="be8e6-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be8e6-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="be8e6-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be8e6-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


