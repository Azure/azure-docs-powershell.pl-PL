---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: ede228aef26cf7e4729acf3a6acc0faae3902f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898649"
---
# <span data-ttu-id="06ea5-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06ea5-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="06ea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="06ea5-103">Pobiera grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06ea5-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06ea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06ea5-104">SYNTAX</span></span>

### <span data-ttu-id="06ea5-105">GetByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06ea5-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06ea5-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="06ea5-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ea5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06ea5-107">DESCRIPTION</span></span>
<span data-ttu-id="06ea5-108">Polecenie cmdlet **Get-AzureRmResourceGroup** umożliwia pobieranie grup zasobów platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06ea5-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="06ea5-109">Możesz uzyskać dostęp do wszystkich grup zasobów lub określić grupę zasobów według nazwy lub według innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="06ea5-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="06ea5-110">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich grup zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06ea5-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="06ea5-111">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="06ea5-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="06ea5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06ea5-112">EXAMPLES</span></span>

### <span data-ttu-id="06ea5-113">Przykład 1: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="06ea5-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="06ea5-114">To polecenie pobiera grupę zasobów platformy Azure w ramach abonamentu o nazwie EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="06ea5-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="06ea5-115">Przykład 2: pobieranie wszystkich tagów grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06ea5-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="06ea5-116">To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla znaczniki skojarzone z tą grupą.</span><span class="sxs-lookup"><span data-stu-id="06ea5-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="06ea5-117">Przykład 3: wyświetlanie grup zasobów według lokalizacji</span><span class="sxs-lookup"><span data-stu-id="06ea5-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="06ea5-118">Przykład 4: wyświetlanie nazw wszystkich grup zasobów w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="06ea5-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="06ea5-119">Przykład 5: wyświetlanie grup zasobów, których nazwy zaczynają się od serwera WebServer</span><span class="sxs-lookup"><span data-stu-id="06ea5-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="06ea5-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06ea5-120">PARAMETERS</span></span>

### <span data-ttu-id="06ea5-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06ea5-121">-ApiVersion</span></span>
<span data-ttu-id="06ea5-122">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="06ea5-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="06ea5-123">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="06ea5-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="06ea5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ea5-124">-DefaultProfile</span></span>
<span data-ttu-id="06ea5-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="06ea5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06ea5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="06ea5-126">-Id</span></span>
<span data-ttu-id="06ea5-127">Określa identyfikator grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="06ea5-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="06ea5-128">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="06ea5-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="06ea5-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06ea5-129">-Location</span></span>
<span data-ttu-id="06ea5-130">Określa lokalizację grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="06ea5-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="06ea5-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06ea5-131">-Name</span></span>
<span data-ttu-id="06ea5-132">Określa nazwę grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="06ea5-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="06ea5-133">Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="06ea5-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ea5-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="06ea5-134">-Pre</span></span>
<span data-ttu-id="06ea5-135">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="06ea5-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="06ea5-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="06ea5-136">-Tag</span></span>
<span data-ttu-id="06ea5-137">Tag Hashtable w celu filtrowania grup zasobów według.</span><span class="sxs-lookup"><span data-stu-id="06ea5-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="06ea5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ea5-138">CommonParameters</span></span>
<span data-ttu-id="06ea5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ea5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ea5-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ea5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ea5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ea5-141">INPUTS</span></span>

### <span data-ttu-id="06ea5-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="06ea5-142">None</span></span>

## <span data-ttu-id="06ea5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06ea5-143">OUTPUTS</span></span>

### <span data-ttu-id="06ea5-144">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06ea5-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="06ea5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06ea5-145">NOTES</span></span>

## <span data-ttu-id="06ea5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ea5-146">RELATED LINKS</span></span>

[<span data-ttu-id="06ea5-147">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06ea5-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="06ea5-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06ea5-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="06ea5-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06ea5-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


