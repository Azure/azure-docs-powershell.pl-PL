---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 346973683ca7e360c4b4d63a4f2ed4f4856a0797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525218"
---
# <span data-ttu-id="d41d7-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d41d7-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="d41d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d41d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d41d7-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d41d7-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d41d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d41d7-104">SYNTAX</span></span>

### <span data-ttu-id="d41d7-105">GetContainerInstanceLogByNamesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d41d7-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d41d7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d41d7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d41d7-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="d41d7-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d41d7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d41d7-108">DESCRIPTION</span></span>
<span data-ttu-id="d41d7-109">Polecenie cmdlet **Get-AzureRmContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="d41d7-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="d41d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d41d7-110">EXAMPLES</span></span>

### <span data-ttu-id="d41d7-111">Przykład 1. Pobieranie dziennika końcowego wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="d41d7-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d41d7-112">Pobierz dziennik z `container1` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d41d7-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="d41d7-113">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="d41d7-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d41d7-114">Przykład 2: pobieranie dziennika końcowego wystąpienia kontenera o takiej samej nazwie jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="d41d7-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d41d7-115">Pobierz dziennik z `mycontainer` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d41d7-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="d41d7-116">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="d41d7-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d41d7-117">Przykład 3: pobieranie linii ogon 2 dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="d41d7-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="d41d7-118">Pobierz wiersze tail 2 dziennika z `container1` grupy kontenerów `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d41d7-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="d41d7-119">Przykład 4: pobieranie dziennika końcowego wystąpienia kontenera w potoku w grupie kontener</span><span class="sxs-lookup"><span data-stu-id="d41d7-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d41d7-120">Pobieranie dziennika z `mycontainer` potoku w grupie kontener `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d41d7-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="d41d7-121">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="d41d7-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="d41d7-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d41d7-122">PARAMETERS</span></span>

### <span data-ttu-id="d41d7-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="d41d7-123">-ContainerGroupName</span></span>
<span data-ttu-id="d41d7-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d41d7-124">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41d7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41d7-125">-DefaultProfile</span></span>
<span data-ttu-id="d41d7-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d41d7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d41d7-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d41d7-127">-InputContainerGroup</span></span>
<span data-ttu-id="d41d7-128">Wejściowy obiekt grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="d41d7-128">The input container group object.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d41d7-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d41d7-129">-Name</span></span>
<span data-ttu-id="d41d7-130">Nazwa wystąpienia kontenera w grupie kontener.</span><span class="sxs-lookup"><span data-stu-id="d41d7-130">The container instance name in the container group.</span></span>
<span data-ttu-id="d41d7-131">Wartość domyślna: tak samo jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="d41d7-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="d41d7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d41d7-132">-ResourceGroupName</span></span>
<span data-ttu-id="d41d7-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d41d7-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41d7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d41d7-134">-ResourceId</span></span>
<span data-ttu-id="d41d7-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d41d7-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41d7-136">-Koniec</span><span class="sxs-lookup"><span data-stu-id="d41d7-136">-Tail</span></span>
<span data-ttu-id="d41d7-137">Liczba wierszy, w których ma się odogon dziennika.</span><span class="sxs-lookup"><span data-stu-id="d41d7-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="d41d7-138">Jeśli nie określono, polecenie cmdlet zwróci do ponad 4 MB dziennika końcowego.</span><span class="sxs-lookup"><span data-stu-id="d41d7-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41d7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41d7-139">CommonParameters</span></span>
<span data-ttu-id="d41d7-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41d7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41d7-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41d7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41d7-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d41d7-142">INPUTS</span></span>

### <span data-ttu-id="d41d7-143">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d41d7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="d41d7-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d41d7-144">OUTPUTS</span></span>

### <span data-ttu-id="d41d7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d41d7-145">System.String</span></span>

## <span data-ttu-id="d41d7-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d41d7-146">NOTES</span></span>

## <span data-ttu-id="d41d7-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d41d7-147">RELATED LINKS</span></span>
