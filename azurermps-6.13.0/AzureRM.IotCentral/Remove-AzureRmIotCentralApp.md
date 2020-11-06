---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554083"
---
# <span data-ttu-id="dca6d-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="dca6d-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="dca6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dca6d-102">SYNOPSIS</span></span>
<span data-ttu-id="dca6d-103">Usuwa aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dca6d-104">SYNTAX</span></span>

### <span data-ttu-id="dca6d-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dca6d-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca6d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca6d-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca6d-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca6d-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca6d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dca6d-108">DESCRIPTION</span></span>
<span data-ttu-id="dca6d-109">Usuwa istniejącą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="dca6d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dca6d-110">EXAMPLES</span></span>

### <span data-ttu-id="dca6d-111">Przykład 1 Usuwanie i aplikacja Centralna z IoT</span><span class="sxs-lookup"><span data-stu-id="dca6d-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="dca6d-112">Usuwa dostarczoną aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="dca6d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dca6d-113">PARAMETERS</span></span>

### <span data-ttu-id="dca6d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dca6d-114">-AsJob</span></span>
<span data-ttu-id="dca6d-115">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="dca6d-115">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca6d-116">-DefaultProfile</span></span>
<span data-ttu-id="dca6d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dca6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dca6d-118">-InputObject</span></span>
<span data-ttu-id="dca6d-119">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dca6d-120">-Name</span></span>
<span data-ttu-id="dca6d-121">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca6d-122">-PassThru</span></span>
<span data-ttu-id="dca6d-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dca6d-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="dca6d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dca6d-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dca6d-126">-ResourceId</span></span>
<span data-ttu-id="dca6d-127">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="dca6d-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dca6d-128">-Confirm</span></span>
<span data-ttu-id="dca6d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dca6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca6d-130">-WhatIf</span></span>
<span data-ttu-id="dca6d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dca6d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca6d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dca6d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca6d-133">CommonParameters</span></span>
<span data-ttu-id="dca6d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca6d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca6d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dca6d-136">INPUTS</span></span>

### <span data-ttu-id="dca6d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dca6d-137">System.String</span></span>
### <span data-ttu-id="dca6d-138">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="dca6d-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="dca6d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dca6d-139">OUTPUTS</span></span>

### <span data-ttu-id="dca6d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dca6d-140">System.Boolean</span></span>
## <span data-ttu-id="dca6d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dca6d-141">NOTES</span></span>

## <span data-ttu-id="dca6d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dca6d-142">RELATED LINKS</span></span>
