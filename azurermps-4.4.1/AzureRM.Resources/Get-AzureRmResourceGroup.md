---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717803"
---
# <span data-ttu-id="26f28-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f28-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="26f28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26f28-102">SYNOPSIS</span></span>
<span data-ttu-id="26f28-103">Pobiera grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26f28-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26f28-104">SYNTAX</span></span>

### <span data-ttu-id="26f28-105">Umożliwia wyświetlenie listy grup zasobów na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="26f28-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="26f28-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="26f28-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f28-107">Umożliwia wyświetlenie listy grup zasobów na podstawie identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="26f28-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f28-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26f28-108">DESCRIPTION</span></span>
<span data-ttu-id="26f28-109">Polecenie cmdlet **Get-AzureRmResourceGroup** umożliwia pobieranie grup zasobów platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="26f28-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="26f28-110">Możesz uzyskać dostęp do wszystkich grup zasobów lub określić grupę zasobów według nazwy lub według innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="26f28-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="26f28-111">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich grup zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="26f28-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="26f28-112">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26f28-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="26f28-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26f28-113">EXAMPLES</span></span>

### <span data-ttu-id="26f28-114">Przykład 1: pobieranie grupy zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="26f28-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="26f28-115">To polecenie pobiera grupę zasobów platformy Azure w ramach abonamentu o nazwie EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="26f28-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="26f28-116">Przykład 2: pobieranie wszystkich tagów grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26f28-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="26f28-117">To polecenie pobiera grupę zasobów o nazwie ContosoRG i wyświetla znaczniki skojarzone z tą grupą.</span><span class="sxs-lookup"><span data-stu-id="26f28-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="26f28-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26f28-118">PARAMETERS</span></span>

### <span data-ttu-id="26f28-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26f28-119">-ApiVersion</span></span>
<span data-ttu-id="26f28-120">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="26f28-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26f28-121">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="26f28-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="26f28-122">-ID</span><span class="sxs-lookup"><span data-stu-id="26f28-122">-Id</span></span>
<span data-ttu-id="26f28-123">Określa identyfikator grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="26f28-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="26f28-124">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="26f28-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f28-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26f28-125">-Location</span></span>
<span data-ttu-id="26f28-126">Określa lokalizację grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="26f28-126">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="26f28-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26f28-127">-Name</span></span>
<span data-ttu-id="26f28-128">Określa nazwę grupy zasobów, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="26f28-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="26f28-129">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="26f28-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f28-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="26f28-130">-Pre</span></span>
<span data-ttu-id="26f28-131">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="26f28-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26f28-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f28-132">-DefaultProfile</span></span>
<span data-ttu-id="26f28-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26f28-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26f28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f28-134">CommonParameters</span></span>
<span data-ttu-id="26f28-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f28-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f28-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f28-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26f28-137">INPUTS</span></span>

### <span data-ttu-id="26f28-138">Ciąg</span><span class="sxs-lookup"><span data-stu-id="26f28-138">String</span></span>
<span data-ttu-id="26f28-139">Możesz popotokować dane wejściowe za pomocą nazwy właściwości polecenia cmdlet, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="26f28-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="26f28-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26f28-140">OUTPUTS</span></span>

### <span data-ttu-id="26f28-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f28-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="26f28-142">To polecenie cmdlet zwraca grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26f28-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="26f28-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26f28-143">NOTES</span></span>

## <span data-ttu-id="26f28-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26f28-144">RELATED LINKS</span></span>

[<span data-ttu-id="26f28-145">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f28-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="26f28-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f28-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="26f28-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f28-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


