---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503500"
---
# <span data-ttu-id="258d8-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="258d8-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="258d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="258d8-102">SYNOPSIS</span></span>
<span data-ttu-id="258d8-103">Zawiera listę wszystkich lub konkretnego wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="258d8-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="258d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="258d8-104">SYNTAX</span></span>

### <span data-ttu-id="258d8-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="258d8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="258d8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="258d8-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="258d8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="258d8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="258d8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="258d8-108">DESCRIPTION</span></span>
<span data-ttu-id="258d8-109">Zapoznaj się z informacjami na temat wdrożenia programu IoT Edge lub listy wdrożeń krawędzi IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="258d8-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="258d8-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="258d8-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="258d8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="258d8-111">EXAMPLES</span></span>

### <span data-ttu-id="258d8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="258d8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="258d8-113">Zapoznaj się z informacjami o wdrożeniu przeglądarki IoT.</span><span class="sxs-lookup"><span data-stu-id="258d8-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="258d8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="258d8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="258d8-115">Lista wszystkich wdrożeń dotyczących krawędzi IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="258d8-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="258d8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="258d8-116">PARAMETERS</span></span>

### <span data-ttu-id="258d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258d8-117">-DefaultProfile</span></span>
<span data-ttu-id="258d8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="258d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="258d8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="258d8-119">-InputObject</span></span>
<span data-ttu-id="258d8-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="258d8-120">IotHub object</span></span>

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

### <span data-ttu-id="258d8-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="258d8-121">-IotHubName</span></span>
<span data-ttu-id="258d8-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="258d8-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="258d8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="258d8-123">-Name</span></span>
<span data-ttu-id="258d8-124">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="258d8-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="258d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="258d8-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="258d8-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="258d8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="258d8-127">-ResourceId</span></span>
<span data-ttu-id="258d8-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="258d8-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="258d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258d8-129">CommonParameters</span></span>
<span data-ttu-id="258d8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258d8-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258d8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258d8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="258d8-132">INPUTS</span></span>

### <span data-ttu-id="258d8-133">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="258d8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="258d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="258d8-134">System.String</span></span>

## <span data-ttu-id="258d8-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="258d8-135">OUTPUTS</span></span>

### <span data-ttu-id="258d8-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="258d8-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="258d8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="258d8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="258d8-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="258d8-138">NOTES</span></span>

## <span data-ttu-id="258d8-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="258d8-139">RELATED LINKS</span></span>
