---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: f97f7ca82ae17c61994a84fbc4b1405b41fdb566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554199"
---
# <span data-ttu-id="b31f2-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b31f2-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="b31f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b31f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b31f2-103">Pobiera grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b31f2-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b31f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b31f2-104">SYNTAX</span></span>

### <span data-ttu-id="b31f2-105">ListContainerGroupParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b31f2-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31f2-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b31f2-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31f2-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b31f2-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31f2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b31f2-108">DESCRIPTION</span></span>
<span data-ttu-id="b31f2-109">Polecenie cmdlet **Get-AzureRmContainerGroup** pobiera określoną grupę kontenerów lub wszystkie grupy kontenerów w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b31f2-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="b31f2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b31f2-110">EXAMPLES</span></span>

### <span data-ttu-id="b31f2-111">Przykład 1: Pobiera określoną grupę kontenerów</span><span class="sxs-lookup"><span data-stu-id="b31f2-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
```

<span data-ttu-id="b31f2-112">Polecenie pobiera określoną grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b31f2-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="b31f2-113">Przykład 2: Pobiera grupy kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b31f2-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="b31f2-114">Polecenie pobiera grupy kontenerów w grupie zasobów `demo` .</span><span class="sxs-lookup"><span data-stu-id="b31f2-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="b31f2-115">Przykład 3: Pobiera grupy kontenerów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b31f2-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="b31f2-116">Polecenie pobiera grupy kontenerów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b31f2-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="b31f2-117">Przykład 4: Pobiera grupy kontenerów przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="b31f2-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
```

<span data-ttu-id="b31f2-118">Polecenie pobiera grupę kontenerów z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="b31f2-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="b31f2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b31f2-119">PARAMETERS</span></span>

### <span data-ttu-id="b31f2-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b31f2-120">-Name</span></span>
<span data-ttu-id="b31f2-121">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b31f2-121">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b31f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="b31f2-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b31f2-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31f2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b31f2-124">-ResourceId</span></span>
<span data-ttu-id="b31f2-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b31f2-125">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31f2-126">-DefaultProfile</span></span>
<span data-ttu-id="b31f2-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b31f2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b31f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31f2-128">CommonParameters</span></span>
<span data-ttu-id="b31f2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31f2-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b31f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31f2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b31f2-131">INPUTS</span></span>

### <span data-ttu-id="b31f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b31f2-132">System.String</span></span>

## <span data-ttu-id="b31f2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b31f2-133">OUTPUTS</span></span>

### <span data-ttu-id="b31f2-134">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b31f2-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b31f2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b31f2-135">NOTES</span></span>

## <span data-ttu-id="b31f2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b31f2-136">RELATED LINKS</span></span>

