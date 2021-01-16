---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330013"
---
# <span data-ttu-id="071fa-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="071fa-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="071fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="071fa-102">SYNOPSIS</span></span>
<span data-ttu-id="071fa-103">Lista wszystkich lub określonych automatycznych konfiguracji zarządzania urządzeniami IoT.</span><span class="sxs-lookup"><span data-stu-id="071fa-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="071fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="071fa-104">SYNTAX</span></span>

### <span data-ttu-id="071fa-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="071fa-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="071fa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="071fa-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="071fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="071fa-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="071fa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="071fa-108">DESCRIPTION</span></span>
<span data-ttu-id="071fa-109">Zapoznaj się z informacjami o konfiguracji automatycznego zarządzania urządzeniami IoT lub listą automatycznych konfiguracji zarządzania urządzeniami w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="071fa-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="071fa-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="071fa-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="071fa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="071fa-111">EXAMPLES</span></span>

### <span data-ttu-id="071fa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="071fa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="071fa-113">Zapoznaj się z informacjami dotyczącymi automatycznej konfiguracji zarządzania urządzeniami IoT.</span><span class="sxs-lookup"><span data-stu-id="071fa-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="071fa-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="071fa-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="071fa-115">Lista automatycznych konfiguracji zarządzania urządzeniami IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="071fa-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="071fa-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="071fa-116">PARAMETERS</span></span>

### <span data-ttu-id="071fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071fa-117">-DefaultProfile</span></span>
<span data-ttu-id="071fa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="071fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="071fa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="071fa-119">-InputObject</span></span>
<span data-ttu-id="071fa-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="071fa-120">IotHub object</span></span>

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

### <span data-ttu-id="071fa-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="071fa-121">-IotHubName</span></span>
<span data-ttu-id="071fa-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="071fa-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="071fa-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="071fa-123">-Name</span></span>
<span data-ttu-id="071fa-124">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="071fa-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="071fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="071fa-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="071fa-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="071fa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="071fa-127">-ResourceId</span></span>
<span data-ttu-id="071fa-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="071fa-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="071fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071fa-129">CommonParameters</span></span>
<span data-ttu-id="071fa-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071fa-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="071fa-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071fa-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="071fa-132">INPUTS</span></span>

### <span data-ttu-id="071fa-133">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="071fa-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="071fa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="071fa-134">System.String</span></span>

## <span data-ttu-id="071fa-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="071fa-135">OUTPUTS</span></span>

### <span data-ttu-id="071fa-136">Microsoft. Azure. Commands. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="071fa-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="071fa-137">Microsoft. Azure. Commands. Management. IotHub. models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="071fa-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="071fa-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="071fa-138">NOTES</span></span>

## <span data-ttu-id="071fa-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="071fa-139">RELATED LINKS</span></span>
