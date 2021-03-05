---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012257"
---
# <span data-ttu-id="d0c8d-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d0c8d-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="d0c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c8d-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="d0c8d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0c8d-104">SYNTAX</span></span>

### <span data-ttu-id="d0c8d-105">GetContainerInstanceLogByNamesParamSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d0c8d-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c8d-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d0c8d-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c8d-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="d0c8d-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0c8d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0c8d-108">DESCRIPTION</span></span>
<span data-ttu-id="d0c8d-109">Polecenie **cmdlet Get-AzContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenera.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="d0c8d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0c8d-110">EXAMPLES</span></span>

### <span data-ttu-id="d0c8d-111">Przykład 1. Uzyskiwanie dziennika tail of a container instance</span><span class="sxs-lookup"><span data-stu-id="d0c8d-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d0c8d-112">Pobierz dziennik z `container1` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="d0c8d-113">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d0c8d-114">Przykład 2. Uzyskiwanie dziennika tail of a container instance, które ma taką samą nazwę jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="d0c8d-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d0c8d-115">Pobierz dziennik z `mycontainer` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="d0c8d-116">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d0c8d-117">Przykład 3. Uzyskiwanie dwóch wierszy dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="d0c8d-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="d0c8d-118">Pobierz 2 wiersze dziennika z `container1` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="d0c8d-119">Przykład 4. Pobierz dziennik tail wystąpienia kontenera w potoku w grupie kontenerów</span><span class="sxs-lookup"><span data-stu-id="d0c8d-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d0c8d-120">Pobierz dziennik z `mycontainer` potoku w grupie kontenerów. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="d0c8d-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="d0c8d-121">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="d0c8d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0c8d-122">PARAMETERS</span></span>

### <span data-ttu-id="d0c8d-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c8d-123">-ContainerGroupName</span></span>
<span data-ttu-id="d0c8d-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-124">The container group name.</span></span>

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

### <span data-ttu-id="d0c8d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c8d-125">-DefaultProfile</span></span>
<span data-ttu-id="d0c8d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0c8d-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d0c8d-127">-InputContainerGroup</span></span>
<span data-ttu-id="d0c8d-128">Obiekt grupy kontenera wprowadzania.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-128">The input container group object.</span></span>

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

### <span data-ttu-id="d0c8d-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0c8d-129">-Name</span></span>
<span data-ttu-id="d0c8d-130">Nazwa wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-130">The container instance name in the container group.</span></span>
<span data-ttu-id="d0c8d-131">Domyślne: taka sama jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="d0c8d-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="d0c8d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c8d-132">-ResourceGroupName</span></span>
<span data-ttu-id="d0c8d-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-133">The resource group name.</span></span>

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

### <span data-ttu-id="d0c8d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0c8d-134">-ResourceId</span></span>
<span data-ttu-id="d0c8d-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-135">The resource id.</span></span>

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

### <span data-ttu-id="d0c8d-136">- Tail</span><span class="sxs-lookup"><span data-stu-id="d0c8d-136">-Tail</span></span>
<span data-ttu-id="d0c8d-137">Liczba wierszy do odsuń dziennika.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="d0c8d-138">Jeśli nie zostanie określone, polecenie cmdlet zwróci maksymalnie 4 MB dziennika</span><span class="sxs-lookup"><span data-stu-id="d0c8d-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="d0c8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c8d-139">CommonParameters</span></span>
<span data-ttu-id="d0c8d-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c8d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c8d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c8d-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0c8d-142">INPUTS</span></span>

### <span data-ttu-id="d0c8d-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d0c8d-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="d0c8d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d0c8d-144">System.String</span></span>

## <span data-ttu-id="d0c8d-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0c8d-145">OUTPUTS</span></span>

### <span data-ttu-id="d0c8d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d0c8d-146">System.String</span></span>

## <span data-ttu-id="d0c8d-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0c8d-147">NOTES</span></span>

## <span data-ttu-id="d0c8d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0c8d-148">RELATED LINKS</span></span>
