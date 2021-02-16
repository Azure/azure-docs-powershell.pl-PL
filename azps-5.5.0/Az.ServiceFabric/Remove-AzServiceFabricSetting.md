---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183435"
---
# <span data-ttu-id="b57af-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b57af-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b57af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b57af-102">SYNOPSIS</span></span>
<span data-ttu-id="b57af-103">Usuń jedno lub wiele ustawień usługi Fabric z klastrów.</span><span class="sxs-lookup"><span data-stu-id="b57af-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="b57af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b57af-104">SYNTAX</span></span>

### <span data-ttu-id="b57af-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b57af-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b57af-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b57af-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b57af-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b57af-107">DESCRIPTION</span></span>
<span data-ttu-id="b57af-108">Użyj **ustawienia Remove-AzServiceFabricSetting,** aby usunąć ustawienia usługi Fabric z klastru.</span><span class="sxs-lookup"><span data-stu-id="b57af-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="b57af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b57af-109">EXAMPLES</span></span>

### <span data-ttu-id="b57af-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b57af-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="b57af-111">To polecenie spowoduje usunięcie ustawień "MaxCursors" w sekcji "EseStore".</span><span class="sxs-lookup"><span data-stu-id="b57af-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="b57af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b57af-112">PARAMETERS</span></span>

### <span data-ttu-id="b57af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57af-113">-DefaultProfile</span></span>
<span data-ttu-id="b57af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b57af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57af-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b57af-115">-Name</span></span>
<span data-ttu-id="b57af-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="b57af-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57af-117">- Parametr</span><span class="sxs-lookup"><span data-stu-id="b57af-117">-Parameter</span></span>
<span data-ttu-id="b57af-118">Nazwa parametru ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="b57af-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b57af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57af-119">-ResourceGroupName</span></span>
<span data-ttu-id="b57af-120">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b57af-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57af-121">— Sekcja</span><span class="sxs-lookup"><span data-stu-id="b57af-121">-Section</span></span>
<span data-ttu-id="b57af-122">Nazwa sekcji ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="b57af-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b57af-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b57af-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="b57af-124">Tablica ustawień materiału</span><span class="sxs-lookup"><span data-stu-id="b57af-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b57af-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b57af-125">-Confirm</span></span>
<span data-ttu-id="b57af-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b57af-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b57af-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b57af-127">-WhatIf</span></span>
<span data-ttu-id="b57af-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b57af-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b57af-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b57af-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b57af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57af-130">CommonParameters</span></span>
<span data-ttu-id="b57af-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57af-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b57af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57af-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b57af-133">INPUTS</span></span>

### <span data-ttu-id="b57af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b57af-134">System.String</span></span>

### <span data-ttu-id="b57af-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="b57af-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b57af-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b57af-136">OUTPUTS</span></span>

### <span data-ttu-id="b57af-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b57af-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b57af-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b57af-138">NOTES</span></span>

## <span data-ttu-id="b57af-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b57af-139">RELATED LINKS</span></span>
