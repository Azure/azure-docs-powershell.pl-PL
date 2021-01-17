---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386421"
---
# <span data-ttu-id="1b425-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="1b425-101">Update-AzIotHub</span></span>

## <span data-ttu-id="1b425-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b425-102">SYNOPSIS</span></span>
<span data-ttu-id="1b425-103">Zaktualizuj centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1b425-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="1b425-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b425-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b425-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b425-105">DESCRIPTION</span></span>
<span data-ttu-id="1b425-106">Możesz zaktualizować właściwości znaczników IotHub.</span><span class="sxs-lookup"><span data-stu-id="1b425-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="1b425-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b425-107">EXAMPLES</span></span>

### <span data-ttu-id="1b425-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b425-108">Example 1</span></span>
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

<span data-ttu-id="1b425-109">Aktualizowanie znaczników Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1b425-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="1b425-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b425-110">PARAMETERS</span></span>

### <span data-ttu-id="1b425-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b425-111">-DefaultProfile</span></span>
<span data-ttu-id="1b425-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b425-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b425-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b425-113">-Name</span></span>
<span data-ttu-id="1b425-114">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="1b425-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1b425-115">-Resetowanie</span><span class="sxs-lookup"><span data-stu-id="1b425-115">-Reset</span></span>
<span data-ttu-id="1b425-116">Resetuj Tagi IoTHub</span><span class="sxs-lookup"><span data-stu-id="1b425-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="1b425-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b425-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b425-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1b425-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1b425-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b425-119">-Tag</span></span>
<span data-ttu-id="1b425-120">Kolekcja tagów IoTHub</span><span class="sxs-lookup"><span data-stu-id="1b425-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="1b425-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b425-121">-Confirm</span></span>
<span data-ttu-id="1b425-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b425-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b425-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b425-123">-WhatIf</span></span>
<span data-ttu-id="1b425-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b425-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b425-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b425-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b425-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b425-126">CommonParameters</span></span>
<span data-ttu-id="1b425-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b425-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b425-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b425-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b425-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b425-129">INPUTS</span></span>

### <span data-ttu-id="1b425-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1b425-130">System.String</span></span>

## <span data-ttu-id="1b425-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b425-131">OUTPUTS</span></span>

### <span data-ttu-id="1b425-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1b425-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="1b425-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b425-133">NOTES</span></span>

## <span data-ttu-id="1b425-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b425-134">RELATED LINKS</span></span>
