---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386528"
---
# <span data-ttu-id="da622-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="da622-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="da622-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da622-102">SYNOPSIS</span></span>
<span data-ttu-id="da622-103">Ustawianie modułów brzegowych na urządzeniu z jedną krawędzią.</span><span class="sxs-lookup"><span data-stu-id="da622-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="da622-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da622-104">SYNTAX</span></span>

### <span data-ttu-id="da622-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da622-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da622-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="da622-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da622-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="da622-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da622-108">Opis</span><span class="sxs-lookup"><span data-stu-id="da622-108">DESCRIPTION</span></span>
<span data-ttu-id="da622-109">Umożliwia zastosowanie zawartości konfiguracji dostarczonych modułów do określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="da622-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="da622-110">Uwaga: po wykonaniu polecenia polecenie przeprowadzi zbieranie modułów zastosowanych do urządzenia.</span><span class="sxs-lookup"><span data-stu-id="da622-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="da622-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da622-111">EXAMPLES</span></span>

### <span data-ttu-id="da622-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da622-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="da622-113">Testowanie modułów brzegowych podczas opracowywania przez ustawienie modułów na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="da622-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="da622-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da622-114">PARAMETERS</span></span>

### <span data-ttu-id="da622-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da622-115">-DefaultProfile</span></span>
<span data-ttu-id="da622-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da622-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da622-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="da622-117">-DeviceId</span></span>
<span data-ttu-id="da622-118">Identyfikator urządzenia w celu krawędzi docelowej.</span><span class="sxs-lookup"><span data-stu-id="da622-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da622-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da622-119">-InputObject</span></span>
<span data-ttu-id="da622-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="da622-120">IotHub object</span></span>

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

### <span data-ttu-id="da622-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="da622-121">-IotHubName</span></span>
<span data-ttu-id="da622-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="da622-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="da622-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="da622-123">-ModulesContent</span></span>
<span data-ttu-id="da622-124">Zawartość konfiguracji modułów na urządzeniach IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="da622-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da622-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da622-125">-ResourceGroupName</span></span>
<span data-ttu-id="da622-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="da622-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="da622-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da622-127">-ResourceId</span></span>
<span data-ttu-id="da622-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="da622-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="da622-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da622-129">-Confirm</span></span>
<span data-ttu-id="da622-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da622-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da622-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da622-131">-WhatIf</span></span>
<span data-ttu-id="da622-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da622-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da622-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da622-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da622-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da622-134">CommonParameters</span></span>
<span data-ttu-id="da622-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da622-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da622-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da622-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da622-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da622-137">INPUTS</span></span>

### <span data-ttu-id="da622-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="da622-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="da622-139">System. String</span><span class="sxs-lookup"><span data-stu-id="da622-139">System.String</span></span>

## <span data-ttu-id="da622-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da622-140">OUTPUTS</span></span>

### <span data-ttu-id="da622-141">Microsoft. Azure. Commands. Management. IotHub. models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="da622-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="da622-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da622-142">NOTES</span></span>

## <span data-ttu-id="da622-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da622-143">RELATED LINKS</span></span>
