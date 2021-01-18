---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503441"
---
# <span data-ttu-id="9ef94-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9ef94-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="9ef94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ef94-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef94-103">Usuwa aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="9ef94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ef94-104">SYNTAX</span></span>

### <span data-ttu-id="9ef94-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ef94-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef94-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef94-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef94-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef94-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef94-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ef94-108">DESCRIPTION</span></span>
<span data-ttu-id="9ef94-109">Usuwa istniejącą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="9ef94-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ef94-110">EXAMPLES</span></span>

### <span data-ttu-id="9ef94-111">Przykład 1 Usuwanie i aplikacja Centralna z IoT</span><span class="sxs-lookup"><span data-stu-id="9ef94-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="9ef94-112">Usuwa dostarczoną aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="9ef94-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ef94-113">PARAMETERS</span></span>

### <span data-ttu-id="9ef94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ef94-114">-AsJob</span></span>
<span data-ttu-id="9ef94-115">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="9ef94-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="9ef94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef94-116">-DefaultProfile</span></span>
<span data-ttu-id="9ef94-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef94-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ef94-118">-InputObject</span></span>
<span data-ttu-id="9ef94-119">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="9ef94-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ef94-120">-Name</span></span>
<span data-ttu-id="9ef94-121">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="9ef94-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ef94-122">-PassThru</span></span>
<span data-ttu-id="9ef94-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9ef94-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ef94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef94-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ef94-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ef94-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="9ef94-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef94-126">-ResourceId</span></span>
<span data-ttu-id="9ef94-127">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="9ef94-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="9ef94-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ef94-128">-Confirm</span></span>
<span data-ttu-id="9ef94-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef94-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef94-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef94-130">-WhatIf</span></span>
<span data-ttu-id="9ef94-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef94-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef94-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ef94-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef94-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef94-133">CommonParameters</span></span>
<span data-ttu-id="9ef94-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef94-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef94-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ef94-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef94-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ef94-136">INPUTS</span></span>

### <span data-ttu-id="9ef94-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef94-137">System.String</span></span>

### <span data-ttu-id="9ef94-138">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9ef94-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="9ef94-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ef94-139">OUTPUTS</span></span>

### <span data-ttu-id="9ef94-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ef94-140">System.Boolean</span></span>

## <span data-ttu-id="9ef94-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ef94-141">NOTES</span></span>

## <span data-ttu-id="9ef94-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ef94-142">RELATED LINKS</span></span>
