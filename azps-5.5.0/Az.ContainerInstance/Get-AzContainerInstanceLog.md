---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177379"
---
# <span data-ttu-id="54351-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="54351-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="54351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54351-102">SYNOPSIS</span></span>
<span data-ttu-id="54351-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="54351-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54351-104">SYNTAX</span></span>

### <span data-ttu-id="54351-105">GetContainerInstanceLogByNamesParamSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="54351-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54351-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="54351-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54351-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="54351-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54351-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="54351-108">DESCRIPTION</span></span>
<span data-ttu-id="54351-109">Polecenie **cmdlet Get-AzContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenera.</span><span class="sxs-lookup"><span data-stu-id="54351-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="54351-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54351-110">EXAMPLES</span></span>

### <span data-ttu-id="54351-111">Przykład 1. Uzyskiwanie dziennika tail of a container instance</span><span class="sxs-lookup"><span data-stu-id="54351-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="54351-112">Pobierz dziennik z `container1` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="54351-113">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="54351-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="54351-114">Przykład 2. Uzyskiwanie dziennika tail of a container instance, które ma taką samą nazwę jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="54351-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="54351-115">Pobierz dziennik z `mycontainer` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="54351-116">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="54351-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="54351-117">Przykład 3. Uzyskiwanie dwóch wierszy dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="54351-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="54351-118">Pobierz 2 wiersze dziennika z `container1` grupy `mycontainer` kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="54351-119">Przykład 4. Pobierz dziennik tail wystąpienia kontenera w potoku w grupie kontenerów</span><span class="sxs-lookup"><span data-stu-id="54351-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="54351-120">Pobierz dziennik z `mycontainer` potoku w grupie kontenerów. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="54351-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="54351-121">Domyślnie zostanie zwrócona zawartość dziennika o rozmiarze do 4 MB.</span><span class="sxs-lookup"><span data-stu-id="54351-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="54351-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54351-122">PARAMETERS</span></span>

### <span data-ttu-id="54351-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="54351-123">-ContainerGroupName</span></span>
<span data-ttu-id="54351-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-124">The container group name.</span></span>

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

### <span data-ttu-id="54351-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54351-125">-DefaultProfile</span></span>
<span data-ttu-id="54351-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54351-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54351-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="54351-127">-InputContainerGroup</span></span>
<span data-ttu-id="54351-128">Obiekt grupy kontenera wprowadzania.</span><span class="sxs-lookup"><span data-stu-id="54351-128">The input container group object.</span></span>

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

### <span data-ttu-id="54351-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="54351-129">-Name</span></span>
<span data-ttu-id="54351-130">Nazwa wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="54351-130">The container instance name in the container group.</span></span>
<span data-ttu-id="54351-131">Domyślne: taka sama jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="54351-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="54351-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54351-132">-ResourceGroupName</span></span>
<span data-ttu-id="54351-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54351-133">The resource group name.</span></span>

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

### <span data-ttu-id="54351-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54351-134">-ResourceId</span></span>
<span data-ttu-id="54351-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="54351-135">The resource id.</span></span>

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

### <span data-ttu-id="54351-136">- Tail</span><span class="sxs-lookup"><span data-stu-id="54351-136">-Tail</span></span>
<span data-ttu-id="54351-137">Liczba wierszy do odsuń dziennika.</span><span class="sxs-lookup"><span data-stu-id="54351-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="54351-138">Jeśli nie zostanie określone, polecenie cmdlet zwróci maksymalnie 4 MB dziennika</span><span class="sxs-lookup"><span data-stu-id="54351-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="54351-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54351-139">CommonParameters</span></span>
<span data-ttu-id="54351-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54351-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54351-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54351-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54351-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54351-142">INPUTS</span></span>

### <span data-ttu-id="54351-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="54351-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="54351-144">System.String</span><span class="sxs-lookup"><span data-stu-id="54351-144">System.String</span></span>

## <span data-ttu-id="54351-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54351-145">OUTPUTS</span></span>

### <span data-ttu-id="54351-146">System.String</span><span class="sxs-lookup"><span data-stu-id="54351-146">System.String</span></span>

## <span data-ttu-id="54351-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54351-147">NOTES</span></span>

## <span data-ttu-id="54351-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54351-148">RELATED LINKS</span></span>
