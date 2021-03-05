---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: b7b89f239949f6a61e3388b0f5cb794cd4ad0c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004065"
---
# <span data-ttu-id="214ca-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="214ca-101">Update-AzIotHub</span></span>

## <span data-ttu-id="214ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214ca-102">SYNOPSIS</span></span>
<span data-ttu-id="214ca-103">Zaktualizuj centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="214ca-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="214ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="214ca-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="214ca-105">DESCRIPTION</span></span>
<span data-ttu-id="214ca-106">Właściwości tagów aplikacji IotHub można zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="214ca-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="214ca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="214ca-107">EXAMPLES</span></span>

### <span data-ttu-id="214ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="214ca-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="214ca-109">Aktualizowanie tagów Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="214ca-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="214ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="214ca-110">PARAMETERS</span></span>

### <span data-ttu-id="214ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214ca-111">-DefaultProfile</span></span>
<span data-ttu-id="214ca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="214ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214ca-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="214ca-113">-Name</span></span>
<span data-ttu-id="214ca-114">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="214ca-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214ca-115">— Resetowanie</span><span class="sxs-lookup"><span data-stu-id="214ca-115">-Reset</span></span>
<span data-ttu-id="214ca-116">Resetowanie tagów w usłudze IoTHub</span><span class="sxs-lookup"><span data-stu-id="214ca-116">Reset IoTHub Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="214ca-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="214ca-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214ca-119">— Tag</span><span class="sxs-lookup"><span data-stu-id="214ca-119">-Tag</span></span>
<span data-ttu-id="214ca-120">Kolekcja tagów ioTHub</span><span class="sxs-lookup"><span data-stu-id="214ca-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="214ca-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="214ca-121">-Confirm</span></span>
<span data-ttu-id="214ca-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="214ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214ca-123">-WhatIf</span></span>
<span data-ttu-id="214ca-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214ca-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="214ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214ca-126">CommonParameters</span></span>
<span data-ttu-id="214ca-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214ca-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214ca-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214ca-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214ca-129">INPUTS</span></span>

### <span data-ttu-id="214ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="214ca-130">System.String</span></span>

## <span data-ttu-id="214ca-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214ca-131">OUTPUTS</span></span>

### <span data-ttu-id="214ca-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="214ca-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="214ca-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="214ca-133">NOTES</span></span>

## <span data-ttu-id="214ca-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="214ca-134">RELATED LINKS</span></span>
