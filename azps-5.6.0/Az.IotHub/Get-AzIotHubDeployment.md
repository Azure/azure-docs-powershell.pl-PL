---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 4c4a9259f80360cfa8947035e84368ca18ed77d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988107"
---
# <span data-ttu-id="05bd4-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="05bd4-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="05bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="05bd4-103">Lista wszystkich lub konkretnego wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="05bd4-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="05bd4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05bd4-104">SYNTAX</span></span>

### <span data-ttu-id="05bd4-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05bd4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05bd4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05bd4-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05bd4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="05bd4-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05bd4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="05bd4-108">DESCRIPTION</span></span>
<span data-ttu-id="05bd4-109">Poznaj szczegóły wdrożenia IoT Edge lub listy wdrożeń IoT Edge w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="05bd4-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="05bd4-110">Aby https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="05bd4-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="05bd4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05bd4-111">EXAMPLES</span></span>

### <span data-ttu-id="05bd4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05bd4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="05bd4-113">Poznaj szczegóły wdrożenia IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="05bd4-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="05bd4-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="05bd4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="05bd4-115">Lista wszystkich wdrożeń programu IoT Edge w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="05bd4-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="05bd4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05bd4-116">PARAMETERS</span></span>

### <span data-ttu-id="05bd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bd4-117">-DefaultProfile</span></span>
<span data-ttu-id="05bd4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="05bd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05bd4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05bd4-119">-InputObject</span></span>
<span data-ttu-id="05bd4-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="05bd4-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05bd4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="05bd4-121">-IotHubName</span></span>
<span data-ttu-id="05bd4-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="05bd4-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05bd4-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="05bd4-123">-Name</span></span>
<span data-ttu-id="05bd4-124">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="05bd4-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="05bd4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05bd4-125">-ResourceGroupName</span></span>
<span data-ttu-id="05bd4-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="05bd4-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05bd4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05bd4-127">-ResourceId</span></span>
<span data-ttu-id="05bd4-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="05bd4-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bd4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bd4-129">CommonParameters</span></span>
<span data-ttu-id="05bd4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bd4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bd4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bd4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bd4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05bd4-132">INPUTS</span></span>

### <span data-ttu-id="05bd4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="05bd4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="05bd4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="05bd4-134">System.String</span></span>

## <span data-ttu-id="05bd4-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05bd4-135">OUTPUTS</span></span>

### <span data-ttu-id="05bd4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="05bd4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="05bd4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDomyłki[]</span><span class="sxs-lookup"><span data-stu-id="05bd4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="05bd4-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05bd4-138">NOTES</span></span>

## <span data-ttu-id="05bd4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05bd4-139">RELATED LINKS</span></span>
