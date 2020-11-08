---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 4bbca5286af5b9a0fe616134b8e9e816bd9eb68f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049454"
---
# <span data-ttu-id="f4915-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f4915-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="f4915-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4915-102">SYNOPSIS</span></span>
<span data-ttu-id="f4915-103">Usuwa aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="f4915-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4915-104">SYNTAX</span></span>

### <span data-ttu-id="f4915-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4915-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4915-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4915-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4915-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4915-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4915-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f4915-108">DESCRIPTION</span></span>
<span data-ttu-id="f4915-109">Usuwa istniejącą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="f4915-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4915-110">EXAMPLES</span></span>

### <span data-ttu-id="f4915-111">Przykład 1 Usuwanie i aplikacja Centralna z IoT</span><span class="sxs-lookup"><span data-stu-id="f4915-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="f4915-112">Usuwa dostarczoną aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="f4915-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4915-113">PARAMETERS</span></span>

### <span data-ttu-id="f4915-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4915-114">-AsJob</span></span>
<span data-ttu-id="f4915-115">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="f4915-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f4915-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4915-116">-DefaultProfile</span></span>
<span data-ttu-id="f4915-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4915-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4915-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4915-118">-InputObject</span></span>
<span data-ttu-id="f4915-119">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4915-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4915-120">-Name</span></span>
<span data-ttu-id="f4915-121">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4915-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4915-122">-PassThru</span></span>
<span data-ttu-id="f4915-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f4915-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f4915-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4915-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4915-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4915-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4915-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4915-126">-ResourceId</span></span>
<span data-ttu-id="f4915-127">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="f4915-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4915-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4915-128">-Confirm</span></span>
<span data-ttu-id="f4915-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4915-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4915-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4915-130">-WhatIf</span></span>
<span data-ttu-id="f4915-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4915-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4915-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4915-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4915-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4915-133">CommonParameters</span></span>
<span data-ttu-id="f4915-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4915-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4915-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4915-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4915-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4915-136">INPUTS</span></span>

### <span data-ttu-id="f4915-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f4915-137">System.String</span></span>

### <span data-ttu-id="f4915-138">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f4915-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="f4915-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4915-139">OUTPUTS</span></span>

### <span data-ttu-id="f4915-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4915-140">System.Boolean</span></span>

## <span data-ttu-id="f4915-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4915-141">NOTES</span></span>

## <span data-ttu-id="f4915-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4915-142">RELATED LINKS</span></span>
