---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503900"
---
# <span data-ttu-id="f30be-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="f30be-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="f30be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f30be-102">SYNOPSIS</span></span>
<span data-ttu-id="f30be-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="f30be-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="f30be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f30be-104">SYNTAX</span></span>

### <span data-ttu-id="f30be-105">GetContainerInstanceLogByNamesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f30be-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f30be-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f30be-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f30be-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="f30be-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f30be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f30be-108">DESCRIPTION</span></span>
<span data-ttu-id="f30be-109">Polecenie cmdlet **Get-AzContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="f30be-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="f30be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f30be-110">EXAMPLES</span></span>

### <span data-ttu-id="f30be-111">Przykład 1. Pobieranie dziennika końcowego wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="f30be-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="f30be-112">Pobierz dziennik z `container1` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="f30be-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="f30be-113">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="f30be-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="f30be-114">Przykład 2: pobieranie dziennika końcowego wystąpienia kontenera o takiej samej nazwie jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="f30be-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="f30be-115">Pobierz dziennik z `mycontainer` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="f30be-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="f30be-116">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="f30be-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="f30be-117">Przykład 3: pobieranie linii ogon 2 dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="f30be-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="f30be-118">Pobierz wiersze tail 2 dziennika z `container1` grupy kontenerów `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="f30be-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="f30be-119">Przykład 4: pobieranie dziennika końcowego wystąpienia kontenera w potoku w grupie kontener</span><span class="sxs-lookup"><span data-stu-id="f30be-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="f30be-120">Pobieranie dziennika z `mycontainer` potoku w grupie kontener `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="f30be-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="f30be-121">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="f30be-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="f30be-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f30be-122">PARAMETERS</span></span>

### <span data-ttu-id="f30be-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="f30be-123">-ContainerGroupName</span></span>
<span data-ttu-id="f30be-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="f30be-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30be-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30be-125">-DefaultProfile</span></span>
<span data-ttu-id="f30be-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f30be-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30be-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f30be-127">-InputContainerGroup</span></span>
<span data-ttu-id="f30be-128">Wejściowy obiekt grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="f30be-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30be-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f30be-129">-Name</span></span>
<span data-ttu-id="f30be-130">Nazwa wystąpienia kontenera w grupie kontener.</span><span class="sxs-lookup"><span data-stu-id="f30be-130">The container instance name in the container group.</span></span>
<span data-ttu-id="f30be-131">Wartość domyślna: tak samo jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="f30be-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="f30be-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30be-132">-ResourceGroupName</span></span>
<span data-ttu-id="f30be-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f30be-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30be-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f30be-134">-ResourceId</span></span>
<span data-ttu-id="f30be-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f30be-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30be-136">-Koniec</span><span class="sxs-lookup"><span data-stu-id="f30be-136">-Tail</span></span>
<span data-ttu-id="f30be-137">Liczba wierszy, w których ma się odogon dziennika.</span><span class="sxs-lookup"><span data-stu-id="f30be-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="f30be-138">Jeśli nie określono, polecenie cmdlet zwróci do ponad 4 MB dziennika końcowego.</span><span class="sxs-lookup"><span data-stu-id="f30be-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30be-139">CommonParameters</span></span>
<span data-ttu-id="f30be-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30be-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30be-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30be-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f30be-142">INPUTS</span></span>

### <span data-ttu-id="f30be-143">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f30be-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="f30be-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f30be-144">System.String</span></span>

## <span data-ttu-id="f30be-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f30be-145">OUTPUTS</span></span>

### <span data-ttu-id="f30be-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f30be-146">System.String</span></span>

## <span data-ttu-id="f30be-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f30be-147">NOTES</span></span>

## <span data-ttu-id="f30be-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f30be-148">RELATED LINKS</span></span>
