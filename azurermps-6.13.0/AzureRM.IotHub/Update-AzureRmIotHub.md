---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552795"
---
# <span data-ttu-id="e2d12-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="e2d12-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="e2d12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2d12-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d12-103">Zaktualizuj centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e2d12-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2d12-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2d12-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d12-106">Możesz zaktualizować właściwości znaczników IotHub.</span><span class="sxs-lookup"><span data-stu-id="e2d12-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="e2d12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2d12-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2d12-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="e2d12-109">Dodaj " @tags " do znacznika centrum usługi Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="e2d12-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="e2d12-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2d12-110">PARAMETERS</span></span>

### <span data-ttu-id="e2d12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d12-111">-DefaultProfile</span></span>
<span data-ttu-id="e2d12-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d12-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2d12-113">-Name</span></span>
<span data-ttu-id="e2d12-114">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="e2d12-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e2d12-115">-Resetowanie</span><span class="sxs-lookup"><span data-stu-id="e2d12-115">-Reset</span></span>
<span data-ttu-id="e2d12-116">Resetuj Tagi IoTHub</span><span class="sxs-lookup"><span data-stu-id="e2d12-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="e2d12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d12-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2d12-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e2d12-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e2d12-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2d12-119">-Tag</span></span>
<span data-ttu-id="e2d12-120">Kolekcja tagów IoTHub</span><span class="sxs-lookup"><span data-stu-id="e2d12-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="e2d12-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2d12-121">-Confirm</span></span>
<span data-ttu-id="e2d12-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d12-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d12-123">-WhatIf</span></span>
<span data-ttu-id="e2d12-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d12-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d12-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2d12-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d12-126">CommonParameters</span></span>
<span data-ttu-id="e2d12-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d12-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d12-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d12-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2d12-129">INPUTS</span></span>

### <span data-ttu-id="e2d12-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d12-130">System.String</span></span>

## <span data-ttu-id="e2d12-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2d12-131">OUTPUTS</span></span>

### <span data-ttu-id="e2d12-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2d12-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e2d12-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2d12-133">NOTES</span></span>

## <span data-ttu-id="e2d12-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2d12-134">RELATED LINKS</span></span>
