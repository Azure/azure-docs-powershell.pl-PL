---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 79f71c31f1a04b350733465338e9edcbd281af5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710158"
---
# <span data-ttu-id="67510-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="67510-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="67510-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67510-102">SYNOPSIS</span></span>
<span data-ttu-id="67510-103">Pobiera grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="67510-103">Gets container groups.</span></span>

## <span data-ttu-id="67510-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67510-104">SYNTAX</span></span>

### <span data-ttu-id="67510-105">ListContainerGroupParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67510-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67510-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="67510-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67510-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="67510-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67510-108">Opis</span><span class="sxs-lookup"><span data-stu-id="67510-108">DESCRIPTION</span></span>
<span data-ttu-id="67510-109">Polecenie cmdlet **Get-AzContainerGroup** pobiera określoną grupę kontenerów lub wszystkie grupy kontenerów w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="67510-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="67510-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67510-110">EXAMPLES</span></span>

### <span data-ttu-id="67510-111">Przykład 1: Pobiera określoną grupę kontenerów</span><span class="sxs-lookup"><span data-stu-id="67510-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

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
State                    : Running
Events                   : {}
```

<span data-ttu-id="67510-112">Polecenie pobiera określoną grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="67510-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="67510-113">Przykład 2: Pobiera grupy kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="67510-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="67510-114">Polecenie pobiera grupy kontenerów w grupie zasobów `demo` .</span><span class="sxs-lookup"><span data-stu-id="67510-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="67510-115">Przykład 3: Pobiera grupy kontenerów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="67510-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="67510-116">Polecenie pobiera grupy kontenerów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="67510-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="67510-117">Przykład 4: Pobiera grupy kontenerów przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="67510-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

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
State                    : Running
Events                   : {}
```

<span data-ttu-id="67510-118">Polecenie pobiera grupę kontenerów z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="67510-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="67510-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67510-119">PARAMETERS</span></span>

### <span data-ttu-id="67510-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67510-120">-DefaultProfile</span></span>
<span data-ttu-id="67510-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67510-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67510-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67510-122">-Name</span></span>
<span data-ttu-id="67510-123">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="67510-123">The container group Name.</span></span>

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

### <span data-ttu-id="67510-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67510-124">-ResourceGroupName</span></span>
<span data-ttu-id="67510-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67510-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="67510-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67510-126">-ResourceId</span></span>
<span data-ttu-id="67510-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="67510-127">The resource id.</span></span>

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

### <span data-ttu-id="67510-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67510-128">CommonParameters</span></span>
<span data-ttu-id="67510-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67510-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67510-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67510-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67510-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67510-131">INPUTS</span></span>

### <span data-ttu-id="67510-132">System. String</span><span class="sxs-lookup"><span data-stu-id="67510-132">System.String</span></span>

## <span data-ttu-id="67510-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67510-133">OUTPUTS</span></span>

### <span data-ttu-id="67510-134">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="67510-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="67510-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67510-135">NOTES</span></span>

## <span data-ttu-id="67510-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67510-136">RELATED LINKS</span></span>
