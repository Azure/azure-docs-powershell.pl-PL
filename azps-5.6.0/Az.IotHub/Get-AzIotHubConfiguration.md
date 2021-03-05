---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988121"
---
# <span data-ttu-id="29fb4-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="29fb4-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="29fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="29fb4-103">Wyświetla listę wszystkich lub określonej konfiguracji automatycznego zarządzania urządzeniami przez usługę IoT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="29fb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29fb4-104">SYNTAX</span></span>

### <span data-ttu-id="29fb4-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29fb4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29fb4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29fb4-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29fb4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29fb4-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29fb4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="29fb4-108">DESCRIPTION</span></span>
<span data-ttu-id="29fb4-109">Uzyskaj szczegółowe informacje na temat konfiguracji automatycznego zarządzania urządzeniami IoT lub listy konfiguracji automatycznego zarządzania urządzeniami IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="29fb4-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="29fb4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="29fb4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29fb4-111">EXAMPLES</span></span>

### <span data-ttu-id="29fb4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29fb4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="29fb4-113">Uzyskaj szczegółowe informacje na temat konfiguracji automatycznego zarządzania urządzeniami przez IoT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="29fb4-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="29fb4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="29fb4-115">Lista konfiguracji automatycznego zarządzania urządzeniami IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="29fb4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29fb4-116">PARAMETERS</span></span>

### <span data-ttu-id="29fb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fb4-117">-DefaultProfile</span></span>
<span data-ttu-id="29fb4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29fb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29fb4-119">-InputObject</span></span>
<span data-ttu-id="29fb4-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="29fb4-120">IotHub object</span></span>

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

### <span data-ttu-id="29fb4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="29fb4-121">-IotHubName</span></span>
<span data-ttu-id="29fb4-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="29fb4-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="29fb4-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29fb4-123">-Name</span></span>
<span data-ttu-id="29fb4-124">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="29fb4-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="29fb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="29fb4-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="29fb4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29fb4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29fb4-127">-ResourceId</span></span>
<span data-ttu-id="29fb4-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="29fb4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="29fb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fb4-129">CommonParameters</span></span>
<span data-ttu-id="29fb4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29fb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fb4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29fb4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fb4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29fb4-132">INPUTS</span></span>

### <span data-ttu-id="29fb4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="29fb4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="29fb4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="29fb4-134">System.String</span></span>

## <span data-ttu-id="29fb4-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29fb4-135">OUTPUTS</span></span>

### <span data-ttu-id="29fb4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="29fb4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="29fb4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="29fb4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="29fb4-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29fb4-138">NOTES</span></span>

## <span data-ttu-id="29fb4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29fb4-139">RELATED LINKS</span></span>
